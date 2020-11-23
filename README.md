# Machine Learning, Data Science and Deep Learning with Pythonn

My person notes for the [Machine Learning, Data Science and Deep Learning with Python course by Frank Kane on Udemy](https://www.udemy.com/course/data-science-and-machine-learning-with-python-hands-on/) 

## Getting Started

1. [Install Anaconda Individual Edition](https://www.anaconda.com/products/individual)
2. Reopen a terminal window and run the following terminal commands 
	- `conda install pydotplus`
	- `conda install tensorflow`
3. [Download course materials](http://sundog-education.com/machine-learning)
	3.1 In terminal navigate to the location of the unzipped course materials folder and run `jupyter notebook`
	3.2 This will open a browser tab with the url http://localhost:8888/tree with the script files and accompanying data 

## Python Basics

### Python 101

In terminal navigate to the [MLCourse](/MLCourse) directory , run `jupyter notebook` and click on [Python101.ipynb](http://localhost:8888/notebooks/Python101.ipynb)

#### Python Syntax
- Whitespace matters in Python sort of like `{}` in JavaScript
- There is no `;` required to terminate the end of a linelike in JavaScript
- For loops and if else statements end with `:`
- Variables are declared without types similiar to JavaScript since it is a dynamically typed language

***Example**: Write a python program to create a list of numbers from 1 to 6 and then print whether that number is either even or odd*

```python
listOfNumbers = [1, 2, 3, 4, 5, 6]

for number in listOfNumbers:
    if (number % 2 == 0):
        print(number, "is even")
    else:
        print(number, "is odd")
        
print ("All done.")
```


#### Importing Modules

- Use the keyword `import` to import
- Can define an alias using the `as` keyword

***Example**: Import the numpy library and generate a list of 10 numbers with a mean of 25 and a standard deviation of 5*
```python
import numpy as np

A = np.random.normal(25.0, 5.0, 10)
print (A)
```

#### Lists
Python's version of JavaScript arrays

```python
x = [1, 2, 3, 4, 5, 6]
print(len(x)) # 6
x[:3]  			# [1, 2, 3]
x[3:]  			# [4, 5, 6]
x[-2:] 			# [5, 6]
x.extend([7,8]) # [1, 2, 3, 4, 5, 6, 7, 8]
x.append(9) 	# [1, 2, 3, 4, 5, 6, 7, 8, 9]

y = [10, 11, 12]
listOfLists = [x, y]
print(listOfLists) # [[1, 2, 3, 4, 5, 6, 7, 8, 9], [10, 11, 12]]

z = [3, 2, 1]
z.sort() 				# [1, 2, 3]
z.sort(reverse=True) 	# [3, 2, 1]
```

#### Tuples
Immutable lists used for functional programming or working with Apache Spark

```python
x = (1, 2, 3)
len(x) # 3

y = (4, 5, 6)
y[2] # 6

listOfTuples = [x, y]
listOfTuples # [(1, 2, 3), (4, 5, 6)]

(age, income) = "32,120000".split(',')
print(age) # 32
print(income) # 120000
```

#### Dictionaries
Similiar to objects in JavaScript also reffered to as a map or hash table in other languages

```python
captains = {}
captains["Enterprise"] = "Kirk"
captains["Enterprise D"] = "Picard"
captains["Deep Space Nine"] = "Sisko"
captains["Voyager"] = "Janeway"

print(captains["Voyager"]) 			# Janeway
print(captains.get("Enterprise")) 	# Kirk
print(captains.get("NX-01"))		# none

for ship in captains:
    print(ship + ": " + captains[ship])
    
# Enterprise: Kirk
# Enterprise D: Picard
# Deep Space Nine: Sisko
# Voyager: Janeway
```


### Types of Data

#### Numerical
- Represents some sort of quantitative measurement
	-  Heights of people, page load times, stockprices, etc.
- Discrete Data
	- Integerbased;oftencountsofsomeevent.  
		-  How many purchases did a customer make in a year?
		-   How many times did I flip “heads”?
- Continuous Data
	- Has an infinite number of possible values  
		- How much time did it take for a user to check out? 
		-  How much rain fell on a given day?

#### Categorical 
- Qualitative data that has no inherent mathematical meaning
	- Gender, Yes/no (binary data)
	- Race
	- State of Residence
	- Product Category, 
	- Political Party
- You can assign numbers to categories in order to represent them more compactly, but the numbers don’t have mathematical meaning

#### Ordinal
- A mixture of numerical and categorical
- Categorical data that has mathematical meaning
- Example: movie ratings on a 1-5 scale.
	- Ratings must be 1, 2, 3, 4, or 5
	- These values have mathematical meaning; 1 means it’s a worse movie than a 2.


