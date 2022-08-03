# OPP

## what is it

- it's a programming paradigm : is a style of programming, a way of think about software concept of objects.
- this system apply on many languages.
- oop is one of many programming paradigms 
- we was using procedural programming the way of function to function implementation.

------------

## Example

objects in college management program

- Student

  - name

  - subjects

  - email

  - ID

  - courses

  - grades

  - class

    ---

  - set_gpa()

  - succeeded()

  - send_email(content)

  - set_grades_hidden()

  - calculate_gpa()

  ----

## contains?

- Data eg(name, subjects,...)
- operations or method eg(succeeded(), send_email(content), set_grades_hidden(), calculate_gpa())
- why public, private! can you modify the student GPA?


---

# classes in Python

Every thing in python is a class eg(int, float, list, str, set, ...) , so how to know the type of it?

```python
name = "mohamed"
print(type(name))
# The output will be
# >> <class 'str'>
```

----

## First Code

```python
class Student:
  def __init__(self, name):
	#so what is __init__() do?
```

### __ init __()? 

- this is init method is the method which is called when the class is created like in c++ we create the **`int main().`**
- int this dunder method we create or initialize all the initial parameters for this class.

######when we will use it?

- this is used when you want to input a parameters to a class like input the name of student to class directly.
- used when you want do make sure that you have defined class parameters to talk to all other methods.

----

```python
class Student:
  def __init__(self, name):
    self.name = name # what do you think this do?
```

### self?

- this  **`self`**  is used to make the class parameter defined for all other class member or method (function)
- we can name it any thing not just self, but is used like this from python community and all other codes on the Internet, so just use it.

----

```python
class Student:
  def __init__(self, name, student_id):
    self.name = name
    self.student_id = student_id
    self.__gpa = None
    
 def set_gpa(self, value):
  	if type(value) is not str:
      print("Invalid GPA")
      return 0
    
    if value<4 and value>0:
      self.__gpa = value
    else:
        print("Invalid GPA")
    return 1

student1 = Student("mohamed","20112323")
student.set_gpa(3.4)
```

- in this code we have defined name and the student id, but what is the **`self.__gpa = None`**, here we set the variable gpa to be private as it cannot be accessed directly  because you need a to check it.
- ​