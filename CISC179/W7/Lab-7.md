# OOP in Python

## 1. Extending Stack Class Behavior
```python
class Stack:
    def __init__(self):
        self.__stk = []

    def push(self, val):
        self.__stk.append(val)

    def pop(self):
        val = self.__stk[-1]
        del self.__stk[-1]
        return val


class CountingStack(Stack):
    def __init__(self):
        Stack.__init__(self)
        self.__counter = 0

    def get_counter(self):
        return self.__counter

    def pop(self):
        self.__counter += 1
        return Stack.pop(self)


stk = CountingStack()
for i in range(100):
    stk.push(i)
    stk.pop()
print(stk.get_counter())
```

## 2a. Implementing a Queue Class From Scratch (Intermediate Difficulty)
```python
class QueueError(Exception):
    pass


class Queue:
    def __init__(self):
        self.__queue = []

    def put(self, elem):
        self.__queue.insert(0, elem)

    def get(self):
        if len(self.__queue) == 0:
            raise QueueError
        return self.__queue.pop()


que = Queue()
que.put(1)
que.put("dog")
que.put(False)
try:
    for i in range(4):
        print(que.get())
except:
    print("Queue error")
```

## 2b. Extending a Queue Class Capability
```python
class QueueError(Exception):
    pass


class Queue:
    def __init__(self):
        self.__queue = []

    def put(self, elem):
        self.__queue.insert(0, elem)

    def get(self):
        if len(self.__queue) == 0:
            raise QueueError
        return self.__queue.pop()


class SuperQueue(Queue):
    def isempty(self):
        try:
            item = self.get()
            self.put(item)
            return False
        except QueueError:
            return True


que = SuperQueue()
que.put(1)
que.put("dog")
que.put(False)
for i in range(4):
    if not que.isempty():
        print(que.get())
    else:
        print("Queue empty")
```

# 3. Timer Class
```python
def two_digits(val):
    if val < 10:
        return "0" + str(val)
    return str(val)


class Timer:
    def __init__(self, hours=0, minutes=0, seconds=0):
        self.__hours = hours
        self.__minutes = minutes
        self.__seconds = seconds

    def __str__(self):
        return f"{two_digits(self.__hours)}:{two_digits(self.__minutes)}:{two_digits(self.__seconds)}"

    def next_second(self):
        self.__seconds += 1

        if self.__seconds > 59:
            self.__seconds = 0
            self.__minutes += 1

        if self.__minutes > 59:
            self.__minutes = 0
            self.__hours += 1

        if self.__hours > 23:
            self.__hours = 0

    def prev_second(self):
        self.__seconds -= 1

        if self.__seconds < 0:
            self.__seconds = 59
            self.__minutes -= 1

        if self.__minutes < 0:
            self.__minutes = 59
            self.__hours -= 1

        if self.__hours < 0:
            self.__hours = 23


timer = Timer(23, 59, 59)
print(timer)
timer.next_second()
print(timer)
timer.prev_second()
print(timer)
```

