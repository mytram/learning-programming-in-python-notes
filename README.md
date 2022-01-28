# Learn Programming in Python

## Tutoring notes

- Keep sessions short, 15 to 20 minutes each. Use a timer
- Repeat the key concepts over and over again
- Effective use of technologies
  - Navigation
  - Shortcuts 
  - Research information, e.g. Python documentation
  - Terminology
- Use a real programming editor as opposed to an online one
- Focus on the understanding of the problems in code practice instead of the solution
- Many great excercises from [https://pynative.com/](https://pynative.com/)
- (Simple programming prlblems)[https://adriann.github.io/programming_problems.html]

### Friday, 28 Janurary 2022

From [Simple programming prlblems](https://adriann.github.io/programming_problems.html)

#### 7 Write a program that prints a multiplication table for numbers up to 12

#### 8 Write a program that prints all prime numbers up to 1000 or any other number

### Thursday, 27 Janurary 2022

From [Simple programming prlblems](https://adriann.github.io/programming_problems.html)

#### 6 Write a program that asks the user for a number n and gives them the possibility to choose between computing the sum and computing the product of 1,…,n.

- Use `str(input())` to receive the user's choice of calculation

### Wednesday, 26 Janurary 2022

From [Simple programming prlblems](https://adriann.github.io/programming_problems.html)

#### 4. Write a program that asks the user for a number n and prints the sum of the numbers 1 to n

The student independently finished the task after many days of practisng this same problem. In fact, this problem is not easy becasue it has many learning points, which I will describe as the comments below. 

```
n = int(input()) # Ask the user to enter a number. String input need to be converted to an integer

x = 0 # Create a variable to accumulate the sum and assign an initial value of 0 to it
      # Each time, when a variable is assigned a value, the previous value is overwritten, or gone. 

# `range(n+1)` creates a sequence between 0 and n, inclusively

for e in range(n+1): # Each, e is assigned to the next value from the range
  x = x + e          # Accumulating: the x on the right is the sum of the previous elements from the range, 
                     # add the current element `e` to the sum and assigne it to `x`. After that, `x` has the 
                     # the sum of all of the elements till now. 
                     # Repeat with the next element from the range. 
 
print(x)
```

#### 5. Modify the previous program such that only multiples of three or five are considered in the sum, e.g. 3, 5, 6, 9, 10, 12, 15 for n=17

The student modified the previous programme to use `%` (modulo) to check divisibility and `or` to solve the problem. Initially, the student missed the equality comparison in checking if a number was divisible by `3` or `5`. 

### Tuesday, 25 Janurary 2022

Away 

### Monday, 24 January 2022

Away

### Sunday, 23 January 2022

Away

### Saturday, 22 January 2022

### Friday, 21 January 2022

Repeat 4. 

### Thursday, 20 January 2022

Repeat 4. 

### Wednesday, 19 Janurary 2022

Repeat 4. 

### Tuesday, 18 January 2022

Repeat 4. 

### Monday, 17 January 2022

This is hard for a beginner. I turned to (Simple programming problems)[https://adriann.github.io/programming_problems.html] to reinforce the learning:

- vVriables
- Assignment 
- The `range` function
- `for` loop
- `if` and `else`

#### Redo the fibonacci sequence 

```
ns = [1, 2, 3, 4, 5]

length = len(n) # The parentheses are the same as those in Math, which he probably has not studied.
value = ns[length - 1] # the last element

```

```
ns = [1, 1]
i = 0
while i < 10:
  length = len(ns)
  last = length - 1
  last_but_one = length - 2
  new_element = ns[last] + ns[last_but_one]
  ns.append(new_element)
 
print(ns)
```

#### Negative indexes

You can use `ns[-1]` and `ns[-2]` to get the last and the last but one. The programme becomes much shorter. An effective programmer needs to know the language well.

```
while i < 10:
  ns.append(ns[-1] + ns[-2])
```

#### Make function fibonacci_sequence(n), where n is the number of the sequence

```
def fibonacci_sequence(n):
  if n < 0: 
    return None # won't work. Illegal
  if n == 0: 
    return []
  if n == 1: 
    return [1]
  if n == 2: 
    return [1, 1]
  
  ns = ....
  
  return ns

print("Enter the number of the Fibonnaci sequence to generate")

... 

print(fibonacci_sequence(n))

```

### Sunday, 16 January 2022

- Introduce the phrase - invocation. In Python, the syntax of invoking a function or method is `()`, e.g. `len(seq)`
- Refresh how to get the length of a list, the last index of a list
- Reaffirm how to refer to the element of a list by an index
- Introduce `range(start, stop, [step])`. The actual implementation involves classes and it is quite complicated for this stage.
  - `range(10)` is the short form of `range(0, 10, 1)`, which generates a list, `0 <= i < 10`, where `i` is incremented by `1` (step)
  - We can see this by `list(range(10)`, `list(range(0, 10, 1))`, and also try `list(range(0, 10, 2)`. 

#### Print characters from a string that are present at an even index number

Previously, we use `index % 2 == 0` to check the oddity. We can use `range(start, stop, [step])`. 

```
s = str(input()) # Convert input as str

for index := range(0, len(s), 2): 
  print(s[index])
```

### Saturday, 15 January 2022

#### Types, objects, and methods

A type is a collection of values that share the same operations. Integers share arthmetics. 

There is another category of types, called objects, whose operations are associated with them. Strings (`str`) are an example. 

```
x = "Wy do cats meow?"

n = x.count("o")

print(n) # 2
```

#### Documentation 

Use google to search how to convert a string to all uppercase `str.uppercase()`

#### strings are immutable and `list.append`

#### Generate the Fibonacci sequence

Complete the following programme

```
ns = [1, 1]
i = 0 
while i < 10:
  # Get the length of n
  # The index of the last element of n 
  # The index of the last but one element of n
  # The new element is the sum of the last element and the last but one
  ns.append(new_element)

print(ns)
```

#### Conclusion

- The student was still confused between the index of a list and the element of a list. He was able to get the value of an element using an index. 
- The lesson lasted for almost an hour. It was too long. Too ambitious. I should have left the programming exercise to the next lesson. Tomorrow we will redo the excercise.

### Friday, 14 Janurary 2022

#### Write a function to check if the input is a panlindrome or not

- Introduct `True` and `False`
- Reinforce that `return` interupts a function. Ask how many times the `while` loop runs if the input is `hello`. The answer is only once. 

```
def palindrome(s):
  left = 0
  right = len(s) - 1
  
  while right > left: # Jeremy put this condition down all by himself. Impressive. Well done!
    if s[right] != s[left]:
      return False
    left = left + 1
    right = right - 1
  return True  
```

#### Conclusion

- The student was really happy to see his code solved a real problem. He modified it to accept a user input and tried a few times. 

### 12-13 January 20222

- Functions are likened to algebric functions. 


### Before 12 January 2022

I did not keep notes from the beginning. Here are we quickly covered in about ten days

- Introduce to use a programming editor on day 1. I chose the most popular Visual Studio Code, though I am a long term Emacs user and recently a doom/emacs adoptor
- Use the terminal from VSC to execute programmes from command line
- Variables are likened to boxes that you can place a value in it. This is not a perfect analogy since the old value just disappears. One day, the students will challenge the analogy if not straighaway
- Integer numbers and strings are most common values we put in a variable
- `if-else`. Later `if-elif-else` as a short form of nested `if-else-if-else`
- The confusion between `=` and `==` will last for a while. Repeat, repeat, repeat
- Introduct lists, which is a list of variables, `len()` 
- Use `for` loop over lists 
- List indexes. This topic needs to be repeated over and over again
- Introduce functions and arguments
- Introduce `while`, `True` and `False`
- Help set up autoformatting in VSC in front of the student and explain
- Help set up auto-save in VSC after a few days in front of the student and explain. Initially, the student will forget to save the file over and over again, obviously
