---
layout: default
permalink: /lecture/q3
---

# Quiz Review 

## Background 
This quiz is based on the topics covered in weeks 8 through 10. There are 3 sections — short answer questions, Python statements, and a programming problem. Students are allowed to use the Thonny IDE for __Section III only__. Please see the grading rubric for the programming problem. Scratch paper and a simple calculator are allowed.


## Section I (20 points)

**1.** How many times will the following loop run?

```python
lst = [10, 21, 78, 104, 67]

for x in lst:
    if x > 100:
        break
```



**2.** Given:

```python
def main():
    x = 20
    lst = [12, 21, 2]
    lst = func(x, lst)
    print("Value at index 1 is", lst[1])
    print("Value at index 2 is", lst[2])

def func(num1, number_list):
    num1 = 10
    number_list[1] = num1
    number_list[2] = num1 * 3
    return number_list

main()
```

What will be the output?


**3.** What will be the result of the following code?

```python
my_list = [1, 2, 3, 4, 5, 6, 7]
print(my_list[3:6])
```


**4.** What is the output of the following code?

```python
my_dictionary = {"a": 5, "b": 7}
my_dictionary["c"] = my_dictionary["a"] + my_dictionary["b"]
print(my_dictionary)
```


**5.** What will the following code output?

```python
my_list = [10, 20, 30, 40, 50, 60]
print(len(my_list))
```


**6.** Why will the following lines of code raise an error?
 
```python
my_dictionary = {"name": "Alice"}; 
print(my_dictionary[1])
```

**7.** What will be the output of the following code?

```python
my_list = [99, 35, 103]
my_list[1] = 42
print(my_list)
```



**8.** Which method would you use to get a list of all values in a dictionary?

* **A.** my_dictionary.keys()
* **B.** my_dictionary.values()
* **C.** my_dictionary.items()
* **D.** my_dictionary.get()


**9.** Write an expression that will correctly update the value of "score" to `92` in the following dictionary.

```python
student = {"name": "Alice", "score": 88, "grade": "B"}
```


**10.** Write an expression to add a new key-value pair "subject": "Math" to the dictionary `student`.

```python
student = {"name": "Alice", "score": 88, "grade": "B"}
```



## Section II (40 points)

Given the following dictionary and list:

```python
grades = {"Alice": 95, "Brian": 82, "Cathy": 74, "David": 63, "Ella": 88}
numbers = [14, 25, 36, 47, 5, 16]
```

Write Python statements to do the following:

* **a.** Update the dictionary by adding a new item with the key "Frank" and the value `85`.

* **b.** Write a for loop to print each key and its corresponding value in the dictionary.

* **c.** Print the value associated with the key "David".

* **d.** Update the value for the key "Cathy" to `80`.

* **e.** Print the average of the numbers in the `numbers` list.

* **f.** Get the _index_ location of `47` in the `numbers` list.

* **g.** Create a list of all the values in the dictionary `grades`.

* **h.** Find the sum of all the values in the dictionary `grades`.


## Section III (40 points)

Programming question:
* You can use the Thonny Python IDE for writing the program.

<br />
Write a program that prompts users to enter a sequence of 6 numbers separated by spaces. If the sequence length is not 6, display an appropriate message and exit.  Otherwise, create a dictionary that stores the count of numbers above or equal to the average and the count of numbers below the average of the input numbers.

<br />
Sample run:

```
Enter 6 numbers separated by spaces: 25 88 12 42 9 3
{'Above or equal to average': 2, 'Below average': 4}
```


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
  