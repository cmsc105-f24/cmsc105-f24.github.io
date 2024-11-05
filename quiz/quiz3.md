---
layout: default
permalink: quiz/3
---

# Quiz 3

__Points Possible:__ 100

__Date:__ Thursday, November 7th 


## Background 
This quiz is based on the topics covered in weeks 8 through 10. There are 3 sections — short answer questions, Python statements, and a programming problem. Students are allowed to use the Thonny IDE for __Section III only__. Please see the grading rubric for the programming problem. Scratch paper and a simple calculator are allowed.

## Submission
* Submit a `quiz3.txt` file on Blackboard with your answers.
* Submit any Python code from the Thonny IDE on Blackboard.


## Section I (20 points)

**1.** How many times will the following loop run?

```python
lst = [10, 21, 78, -9, -8]

for x in lst:
    if x < 0:
        break
```

* **A.** 2
* **B.** 3
* **C.** 4
* **D.** 5


**2.** Given:

```python
def main():
    x = 12
    lst = [12, 21, 2]
    lst = func(x, lst)
    print("Value at index 0 is", lst[0])
    print("Value at index 1 is", lst[1])

def func(num1, number_list):
    num1 = 10
    number_list[0] = num1
    number_list[1] = num1 * 2
    return number_list

main()
```

What will be the output?

* **A.**
```	
Value at index 0 is 12
Value at index 1 is 21
```

* **B.**
```	
Value at index 0 is 10
Value at index 1 is 100
```

* **C.**	
```
Value at index 0 is 10
Value at index 1 is 20
```

* **D.**	
```
Value at index 0 is 10
Value at index 1 is 12
```

**3.** What will be the result of the following code?

```python
my_list = [1, 2, 3, 4, 5]
print(my_list[2:4])
```

* **A.** [1, 2]
* **B.** [2, 3, 4]
* **C.** [3, 4]
* **D.** [3, 4, 5]


**4.** What is the output of the following code?

```python
my_dict = {"a": 1, "b": 2}
my_dict["c"] = my_dict["a"] + my_dict["b"]
print(my_dict)
```

* **A.** {"a": 1, "b": 2, "c": 3}
* **B.** {"a": 1, "b": 2, "c": 2}
* **C.** {"a": 1, "b": 2}
* **D.** {"a": 1, "b": 2, "c": "ab"}


**5.** What will the following code output?

```python
my_list = [10, 20, 30, 40, 50]
print(len(my_list))
```

* **A.** 5
* **B.** 4
* **C.** 50
* **D.** 10


**6.** Which of the following lines of code will raise an error?

* **A.** 
```python
my_list = [1, 2, 3, 4]; 
my_list[2] = "Hello"
```

* **B.** 
```python
my_list = [1, 2, 3, 4]; 
my_list.append(5)
```

* **C.** 
```python
my_dict = {1: "a", 2: "b"}; 
my_dict[3] = "c"
```

* **D.**
```python
my_dict = {"name": "Alice"}; 
print(my_dict[1])
```

**7.** What will be the output of the following code?

```python
my_list = [1, 2, 3]
my_list[1] = 4
print(my_list)
```

* **A.** [1, 2, 3]
* **B.** [4, 2, 3]
* **C.** [1, 4, 3]
* **D.** [1, 2, 4]


**8.** Which method would you use to get a list of all values in a dictionary?

* **A.** dict.keys()
* **B.** dict.values()
* **C.** dict.items()
* **D.** dict.get()


**9.** Write an expression that will correctly update the value of "age" to 26 in the dictionary.

```python
person = {"name": "John", "age": 25, "city": "New York"}
```


**10.** Write an expression to add a new key-value pair "country": "USA" to the dictionary `person`.

```python
person = {"name": "John", "age": 30, "city": "New York"}
```



## Section II (40 points)

Given the following dictionary and list:

```python
d = {"Alona":100, "Bob":78, "Charlie":89, "Eva":55, "John":66}
lst = [12, 32, 33, 5, 7, 8]
```

Write Python statements to do the following:

* **a.** Update the dictionary by adding a new item with key as "Jack" and value as `90`.

* **b.** Write a for loop to print the keys and values in dictionary.

* **c.** Print value corresponding to the key "John"

* **d.** Update the value corresponding to "Eva" to `60`.

* **e.** Print the average of numbers in `lst`.

* **f.** Get the _index_ location of `5` in `lst`.

* **g.** Create a list of values in dictionary `d`.

* **h.** Find the sum of values in dictionary `d`.


## Section III (40 points)

Programming question:
* You can use the Thonny Python IDE for writing the program.

<br />
Write a program that prompts users to enter a sequence of 5 numbers separated by spaces. If the sequence length is not 5, display an appropriate message and exit. Otherwise, create and print a dictionary containing the count of positive and negative numbers.

<br />
Sample run:

```
Enter 5 numbers separated by spaces: 12 2 -11 -3 3
{'Positive': 2, 'Negative': 3}
```

* Save your program as `numbers.py` and attach it to Blackboard.

### Grading Rubric for Section III:

<table>
    <tr>
        <td>Grading</td>
        <td>Points Possible</td>
    </tr>
    <tr>
        <td>Appropriate header and comments</td>
        <td>5</td>
    </tr>
    <tr>
        <td>Input</td>
        <td>10</td>
    </tr>
    <tr>
        <td>Computation</td>
        <td>15</td>
    </tr>
    <tr>
        <td>Print output</td>
        <td>10</td>
    </tr>
</table>



