### 1. My First Code
### a.
```python
print("All the world's a stage,")
print("And all the men and women merely players:")
print("They have their exits and their entrances;")
print("And one man in his time plays many parts,")
print("His acts being seven ages.")
```
### b.
```python
print("All the world's a stage, \nAnd all the men and women merely players: \nThey have their exits and their entrances; \nAnd one man in his time plays many parts, \nHis acts being seven ages.")
```
### c.
```python
print("127","0","0","1",sep=".")
```
The ```sep``` argument changes the separator between the printed values. By default, ```print()``` uses a space as the separator. In this case, ```sep="."``` replaces the space with a period and gives us an output of ```127.0.0.1```.
### d.
  -  ```flush=True``` is used when you need immediate output. Example: countdown timer, progress updates, logging into real-time systems.
  -  ```flush=False``` is the default and  is used when immediate output is not necessary. Example: Normal scripts where buffering is fine.
### e.
The ```end``` argument triggers the flush behavior when it contains a new line ```"\n"```. When a new line is printed, Python flushes the output buffer automatically.
### Challenges
  -  Understanding how ```sep``` changes the output format
  -  Learning how ```\n``` works inside strings
  -  Understanding when ```flush=True``` is necessary
  -  Remembering the difference between  multiple ```print()``` statements and using escape characters
