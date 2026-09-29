# Python_Assignment
# NAME: THIRUMALAI V
# REG NO: 212223040229

# PROGRAM:

## 1. Print All Prime Numbers Between a Range

**Question:**
Print all prime numbers between the given input range.

**Example Input:**

```text
20 50
```

**Code:**

```python
a, b = map(int, input().split())

for n in range(a, b + 1):
    if n < 2:
        continue

    prime = True

    for i in range(2, n):
        if n % i == 0:
            prime = False
            break

    if prime:
        print(n)
```

**Output:**

```text
23
29
31
37
41
43
47
```

---

## 2. Factorial Using Recursion

**Question:**
Find the factorial of a number using recursion.

**Example Input:**

```text
5
```

**Code:**

```python
def factorial(n):
    if n == 0 or n == 1:
        return 1

    return n * factorial(n - 1)


n = int(input())

print(factorial(n))
```

**Output:**

```text
120
```

---

## 3. Square of Numbers Using Lambda

**Question:**
Find the square of each number using a lambda function.

**Example Input:**

```text
2 3 4 5
```

**Code:**

```python
numbers = list(map(int, input().split()))

square = lambda x: x * x

for n in numbers:
    print(square(n))
```

**Output:**

```text
4
9
16
25
```

---

## 4. Find the Second Largest Element in a List

**Question:**
Find the second largest element in a list.

**Example Input:**

```text
10 5 20 8 20 15
```

**Code:**

```python
numbers = list(map(int, input().split()))

numbers = list(set(numbers))
numbers.sort()

print(numbers[-2])
```

**Output:**

```text
15
```

---

## 5. Count Frequency of Characters in a String

**Question:**
Count the frequency of each character in a string.

**Example Input:**

```text
hello
```

**Code:**

```python
s = input()

freq = {}

for ch in s:
    freq[ch] = freq.get(ch, 0) + 1

print(freq)
```

**Output:**

```text
{'h': 1, 'e': 1, 'l': 2, 'o': 1}
```

---

## 6. Calculate Area of a Circle Using Math Library

**Question:**
Calculate the area of a circle using the `math` library.

**Example Input:**

```text
5
```

**Code:**

```python
import math

r = float(input())

area = math.pi * r * r

print(area)
```

**Output:**

```text
78.53981633974483
```

---

## 7. Reverse a String Without Using Built-in Reverse

**Question:**
Reverse a string without using the built-in `reverse()` function.

**Example Input:**

```text
hello
```

**Code:**

```python
s = input()

result = ""

for i in range(len(s) - 1, -1, -1):
    result += s[i]

print(result)
```

**Output:**

```text
olleh
```

---

## 8. Remove Duplicates from a List

**Question:**
Remove duplicate elements from a list.

**Example Input:**

```text
1 2 2 3 4 4 5
```

**Code:**

```python
numbers = list(map(int, input().split()))

result = []

for n in numbers:
    if n not in result:
        result.append(n)

print(result)
```

**Output:**

```text
[1, 2, 3, 4, 5]
```

---

## 9. Merge Two Dictionaries

**Question:**
Merge two dictionaries into a single dictionary.

**Code:**

```python
d1 = {'a': 10, 'b': 20}
d2 = {'c': 30, 'd': 40}

d1.update(d2)

print(d1)
```

**Output:**

```text
{'a': 10, 'b': 20, 'c': 30, 'd': 40}
```

---

## 10. Fibonacci Series Using Recursion

**Question:**
Print the Fibonacci series using recursion.

**Example Input:**

```text
7
```

**Code:**

```python
def fibonacci(n):
    if n <= 1:
        return n

    return fibonacci(n - 1) + fibonacci(n - 2)


n = int(input())

for i in range(n):
    print(fibonacci(i), end=" ")
```

**Output:**

```text
0 1 1 2 3 5 8
```



# NumPy-Assignment
# Question 1 - Student Marks Array  
## The marks obtained by five students in a subject are given as [78, 65, 89, 56, 92]. Create a NumPy array and display the array along with its basic properties.
## Code
```
import numpy as np

marks = np.array([78, 65, 89, 56, 92])

print("Marks:", marks)
print("Dimensions:", marks.ndim)
print("Shape:", marks.shape)
print("Size:", marks.size)
print("Data type:", marks.dtype)
```
## Output
<img width="1065" height="272" alt="image" src="https://github.com/user-attachments/assets/92cb98cb-1935-4fe7-b53e-df16f9457fde" />

# Question 2 - Student Marks Access  
## The marks of five students are stored in a NumPy array as [72, 85, 64, 90, 76]. Write a program to access and display specific student marks using NumPy indexing and slicing.

## Code
```
import numpy as np

marks = np.array([72, 85, 64, 90, 76])

print("All marks:", marks)
print("First student:", marks[0])
print("Third student:", marks[2])
print("Last student:", marks[-1])
print("First three students:", marks[0:3])
print("Second to fourth students:", marks[1:4])
```
## Output
<img width="1015" height="292" alt="image" src="https://github.com/user-attachments/assets/e3078b81-abe6-4a2d-a946-49f4a8f41067" />


# Question 3 - Subject-wise Marks  
## The marks obtained by five students in three subjects are given below. Create a NumPy array to represent the data and reshape it into an appropriate matrix format.  [78, 85, 90, 65, 72, 80, 88, 91, 84, 56, 62, 70, 95, 89, 92] 

# Code
```
import numpy as np

marks = np.array([
    78, 85, 90, 65, 72,
    80, 88, 91, 84, 56,
    62, 70, 95, 89, 92
])

matrix = marks.reshape(5, 3)

print("Subject-wise marks:")
print(matrix)
```
# Output
<img width="1017" height="325" alt="image" src="https://github.com/user-attachments/assets/8352ddd4-b9f4-462f-afea-802451fd533b" />



# Question 4- Internal and External Marks  
## The internal and external examination marks of five students are stored in two NumPy arrays. Write a program to calculate the final marks of each student using NumPy array operations.  

## Code
```
import numpy as np

internal = np.array([25, 28, 22, 24, 27])
external = np.array([65, 60, 70, 58, 68])

final_marks = internal + external

print("Internal marks:", internal)
print("External marks:", external)
print("Final marks:", final_marks)
```
## Output
<img width="1027" height="247" alt="image" src="https://github.com/user-attachments/assets/52b7f561-8f0e-42d0-8646-661e83b952b5" />


# Question 5- Pass Percentage Analysis  
## The marks obtained by five students are [45, 78, 56, 32, 91]. Using NumPy Boolean masking, identify the students who have secured 50 marks or above. 

## Code
```
import numpy as np

marks = np.array([45, 78, 56, 32, 91])

passed = marks >= 50

print("All marks:", marks)
print("Pass condition:", passed)
print("Students scoring 50 or above:", marks[passed])
```
## Output
<img width="1017" height="233" alt="image" src="https://github.com/user-attachments/assets/ac78dbe3-8e1a-4103-a1ba-36940fc81e2a" />

# Question 6 - Average Marks  
## The marks of five students in three subjects are represented using a NumPy matrix. Write a program to calculate the average marks of each student.

## Code
```
import numpy as np

marks = np.array([
    [78, 85, 90],
    [65, 72, 80],
    [88, 91, 84],
    [56, 62, 70],
    [95, 89, 92]
])

average = np.mean(marks, axis=1)

print("Student marks:")
print(marks)
print("Average marks of each student:", average)
```
## Output
<img width="1016" height="380" alt="image" src="https://github.com/user-attachments/assets/9c183758-6504-489a-8e5d-9dd8058fb325" />

# Question 7 - Class Performance Statistics  
## The marks obtained by five students are [67, 82, 91, 74, 58]. Using NumPy statistical functions, determine the total, average, highest, lowest, and standard deviation of the marks.  

## Code
```
import numpy as np

marks = np.array([67, 82, 91, 74, 58])

print("Marks:", marks)
print("Total:", np.sum(marks))
print("Average:", np.mean(marks))
print("Highest marks:", np.max(marks))
print("Lowest marks:", np.min(marks))
print("Standard deviation:", round(np.std(marks), 2))
```
## Output
<img width="1023" height="292" alt="image" src="https://github.com/user-attachments/assets/957b41f3-4613-4134-bce0-98e6513f5b9b" />


# Question 8 - Subject-wise Performance  
## The marks of five students in three subjects are stored in a NumPy matrix. Write a program to calculate the total marks obtained in each subject using an appropriate axis operation.  

## Code
```
import numpy as np

marks = np.array([
    [78, 85, 90],
    [65, 72, 80],
    [88, 91, 84],
    [56, 62, 70],
    [95, 89, 92]
])

subject_total = np.sum(marks, axis=0)

print("Student marks:")
print(marks)
print("Total marks in each subject:", subject_total)
```
## Output
<img width="1011" height="391" alt="image" src="https://github.com/user-attachments/assets/e3a2acd5-4bd7-49b8-b667-3787ad740d78" />


# Question 9 -Student-wise Performance  
## The marks of five students in three subjects are stored in a NumPy matrix. Write a program to calculate the total marks obtained by each student using an appropriate axis operation. 

## Code
```
import numpy as np

marks = np.array([
    [78, 85, 90],
    [65, 72, 80],
    [88, 91, 84],
    [56, 62, 70],
    [95, 89, 92]
])

student_total = np.sum(marks, axis=1)

print("Student marks:")
print(marks)
print("Total marks of each student:", student_total)
```
## Output
<img width="1027" height="392" alt="image" src="https://github.com/user-attachments/assets/a1d406b7-2bc1-4bd7-a469-f1fff580f012" />


# Question 10-Student Ranking  
## The total marks obtained by five students are [245, 278, 219, 290, 256]. Use NumPy sorting and indexing operations to arrange the marks in order and determine the ranking of the students.

## Code
```
import numpy as np

marks = np.array([245, 278, 219, 290, 256])

sorted_marks = np.sort(marks)[::-1]
ranking = np.argsort(marks)[::-1]

print("Original marks:", marks)
print("Marks in descending order:", sorted_marks)
print("Student positions by rank (1-based):", ranking + 1)

for i in range(len(ranking)):
    student = ranking[i] + 1
    print("Rank", i + 1, "- Student", student,
          "- Marks:", marks[ranking[i]])
```
## Output
<img width="1020" height="402" alt="image" src="https://github.com/user-attachments/assets/2f4185a7-f362-425b-83da-a83eb3a633b5" />

# Question 11 - Duplicate Marks Analysis  
## The marks obtained by five students are [85, 92, 85, 76, 92]. Use NumPy functions to identify the unique marks obtained by the students. 

## Code
```
import numpy as np

marks = np.array([85, 92, 85, 76, 92])

unique_marks = np.unique(marks)

print("Original marks:", marks)
print("Unique marks:", unique_marks)
```
## Output
<img width="1027" height="198" alt="image" src="https://github.com/user-attachments/assets/eef92e77-bbf4-4560-92fe-35147c20f3f7" />

# Question 12- Missing Marks  
## The marks of five students are represented as [78, 85, np.nan, 92, 67], where np.nan represents a missing mark. Write a NumPy program to calculate the average marks without considering the missing value. 

## Code
```
import numpy as np

marks = np.array([78, 85, np.nan, 92, 67])

average = np.nanmean(marks)

print("Marks:", marks)
print("Average without missing marks:", average)
```
## Output
<img width="1023" height="215" alt="image" src="https://github.com/user-attachments/assets/dc305c66-e03a-4e7f-8227-4951d6802ba1" />

# Question 13- Grade Classification  
## The marks obtained by five students are [95, 82, 74, 61, 45]. Using NumPy conditional operations, classify the students into appropriate grade categories based on their marks.  

## Code
```
import numpy as np

marks = np.array([95, 82, 74, 61, 45])

grades = np.select(
    [
        marks >= 90,
        marks >= 80,
        marks >= 70,
        marks >= 60
    ],
    ["A", "B", "C", "D"],
    default="Fail"
)

print("Marks:", marks)
print("Grades:", grades)
```
## Output
<img width="1028" height="342" alt="image" src="https://github.com/user-attachments/assets/b659e088-b599-48bb-ae91-be7bd90aec2a" />

# Question 14- Random Marks Generation  
## Generate marks for five students using NumPy's random number generation functionality. Perform basic statistical analysis on the generated marks.

## Code
```
import numpy as np

np.random.seed(42)

marks = np.random.randint(0, 101, size=5)

print("Random marks:", marks)
print("Total marks:", np.sum(marks))
print("Average marks:", np.mean(marks))
print("Highest marks:", np.max(marks))
print("Lowest marks:", np.min(marks))
```
## Output
<img width="1025" height="290" alt="image" src="https://github.com/user-attachments/assets/43af6092-4ca3-402f-b81b-6ac43b9ebe01" />

# Question 15-Student Performance Analysis  
## The marks of five students in three subjects are stored in a NumPy array. Develop a program to perform a complete student performance analysis by calculating the total  marks, average marks, highest marks, lowest marks, and identifying students who perform above the class average.

## Code
```
import numpy as np

marks = np.array([
    [78, 85, 90],
    [65, 72, 80],
    [88, 91, 84],
    [56, 62, 70],
    [95, 89, 92]
])

total = np.sum(marks, axis=1)
average = np.mean(marks, axis=1)
highest = np.max(marks, axis=1)
lowest = np.min(marks, axis=1)

class_average = np.mean(average)

above_average = np.where(average > class_average)[0] + 1

print("Student marks:")
print(marks)
print("Total marks:", total)
print("Average marks:", np.round(average, 2))
print("Highest marks:", highest)
print("Lowest marks:", lowest)
print("Class average:", round(class_average, 2))
print("Students above class average:", above_average)
```
## Output
<img width="1032" height="658" alt="image" src="https://github.com/user-attachments/assets/64c192a3-6644-4d81-a844-77cd4c39e6f6" />



## PYTHON_FUNCTIONS_CODING

## 1. Calculator Using Function

**Question:**
Write a function `calculate(a, b, operation)` that performs addition, subtraction, multiplication, or division based on the supplied operation.

**Example Input:**

```text
10
5
+
```

**Code:**

```python
def calculate(a, b, operation):
    if operation == "+":
        return a + b

    elif operation == "-":
        return a - b

    elif operation == "*":
        return a * b

    elif operation == "/":
        return a / b

    else:
        return "Invalid operation"


a = int(input())
b = int(input())
operation = input()

print(calculate(a, b, operation))
```

**Output:**

```text
15
```

---

## 2. Sum of Numbers Using `*args`

**Question:**
Write a function `sum_numbers(*args)` that accepts any number of arguments and returns their sum.

**Example Input:**

```text
10 20 30 40
```

**Code:**

```python
def sum_numbers(*args):
    total = 0

    for n in args:
        total += n

    return total


numbers = list(map(int, input().split()))

print(sum_numbers(*numbers))
```

**Output:**

```text
100
```

---

## 3. Employee Information Using `**kwargs`

**Question:**
Write a function `employee(**args)` that accepts employee information such as name, ID, department and salary, then displays the information.

**Code:**

```python
def employee(**args):
    for key, value in args.items():
        print(key, ":", value)


employee(
    name="Gayathri",
    ID=101,
    department="Testing",
    salary=50000
)
```

**Output:**

```text
name : Gayathri
ID : 101
department : Testing
salary : 50000
```

---

## 4. Remove Duplicates While Preserving Order

**Question:**
Write a function `remove_duplicates(lst)` that returns a list containing only unique elements while preserving their original order.

**Example Input:**

```text
1 2 2 3 4 3 5 1
```

**Code:**

```python
def remove_duplicates(lst):
    result = []

    for item in lst:
        if item not in result:
            result.append(item)

    return result


numbers = list(map(int, input().split()))

print(remove_duplicates(numbers))
```

**Output:**

```text
[1, 2, 3, 4, 5]
```

---

## 5. Sort List of Tuples Using Lambda

**Question:**
Using a lambda function, sort a list of tuples based on the second element.

**Example Input:**

```text
[(1, 5), (2, 3), (4, 1)]
```

**Code:**

```python
numbers = [(1, 5), (2, 3), (4, 1)]

result = sorted(numbers, key=lambda x: x[1])

print(result)
```

**Output:**

```text
[(4, 1), (2, 3), (1, 5)]
```
