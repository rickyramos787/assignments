### 1. Literals
  -  5
  -  2.5
  -  3
  -  6.0
  -  True
  -  True
  -  HelloWorld
  -  blablabla
  -  54
  -  59.0
  -  1
  -  -2 2 512
### 2. Data Type
  -  <class 'str'>
  -  TypeError
  -  <class 'float">
  -  <class 'str'>
  -  <class 'int'>
  -  <class 'bool'>
  -  <class 'str'>
### 3. Operator precedence
  
  a) 20 + 5 * 2 ** 3 / -4 // 2 % 6 - 1
  
  b) Order of Operations
    
    Step 1: Exponent
        2 ** 3 = 8
    Expression becomes: 20 + 5  * 8 / -4 // 2 % 6 - 1
    
    Step 2: Unary minus
        -4 remains -4
    
    Step 3: Multiply, Divide, Floor Divide, Modulus (from left to right)
      -  Multiply 
          5 * 8 = 40
    Expression becomes: 20 + 40 / -4 // 2 % 6 - 1
      -  Division
          40 / -4 = -10.0
    Expression becomes: 20 + -10.0 // 2 % 6 -1      
      -  Floor Division
          -10.0 // 2 = -5.0
    Expression becomes: 20 + -5.0 % 6 - 1
      -  Modulus
          -5.0 % 6 = 1.0
    Expression becomes: 20 + 1.0 - 1
      -  Addition and  Subtraction
          20 + 1.0 = 21.0
          21.0 - 1 = 20.0
  
  c) Verify Answer with Python
  ```python  
  20 + 5 * 2 ** 3 / -4 // 2 % 6 - 1
  ```
  Final Output = 20.0

  ## Challenges
  -  Remembering that ** evaluates right to left
  -  Handling negative modulus rules
  -  Keeping track of float vs integer division
  -  Understanding operator precedence order
  -  Remembering that strings cannot be added to integers
  -  Not mixing up unary and binary minus
