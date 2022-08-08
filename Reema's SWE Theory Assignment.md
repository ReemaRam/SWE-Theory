# Reema's SWE Theory Assignment


## 1. How does Object Oriented Programming differ from Process Oriented Programming?

### Object-oriented programming 
Object-oriented programming (OOP) is known as a programming model which is based upon the concept of objects. These objects contain data in the form of attributes and code in the form of methods. OOP treats data as a significant element in the program development; it doesn't allow it to flow freely around the system. Also, in OOP there is a major emphasis on data rather than procedure (function). OOP allows for the decomposition of a problem into a number of entities called objects and then builds data and function around these objects. Data from an object can only be accessed by the function associated with that object. However, the function of one object can access the function of other objects. 

### Procedural (process) oriented programming 
In procedural (process) oriented programming (POP), large programs are divided into smaller programs which are known as functions. In POP, a program is written as a sequence of procedures or functions. Each procedure contains a set of instructions for performing a specific task. During program execution, each procedure can be called by the other procedures. To call a procedure, only the function name is written. A lot of attention is placed onto the development of functions therefore, little attention is paid towards the data that is being used by various functions. So, the main focus in POP is on procedure (process) and not on the data.

 ### Characteristics of both

In OOP some characterists include:

 - Data is hidden and can't be accessed by external function
 - There is an emphasis on data rather than procedure
 - Programs are divided into objects
 - Objects can communicate with each other through function

In POP some characteristics include:

 - Data moves freely around the system from function to function
 - Functions change the value of data at any time from any place
 - Large programs are divided into smaller programs; these are known as functions
 - Most of the functions share global data

### Pros and cons

Pros of OOP:

 - **Faster development**: Reuse enables faster development. OOP languages come with rich libraries of objects, and code developed during projects is also reusable in future projects.
 - **Lower cost of development**: Through the use of reusing software, it allows for costs to be cut. OOP languages come with rich libraries of objects, and code developed during projects is also reusable in future projects.
 - **Higher quality software**: More time and resources can be used in the verification of the software because of the faster development and lower cost of development in software.

Pros of POP:

 - POP is good for general-purpose programming
 - It is an easier way to keep track of program flow
 - It takes up little memory

Cons of OOP:

 - **High effort to create programs**: These programs do require a lot of effort and work to create. A lot of planning goes into an OOP well before any code is even written. In the initial stages, the planning was thought to be a waste of time. Also, programmers found themselves to be spending an increasing amount of time writing the program as they were so large.
 - **Speed**: OOP's are slower than other programs, mainly due to their size. Other aspects of OOP also demand more system resources, which in turn slows the program down further.

Cons of POP:

 - **No data security**: Global data can be accessed and changed by any procedure meaning there is no data security. 
 - **Real world application**: POP doesn't model real world problems because functions are action oriented.

### Key differences between OOP and POP:

 1. OOP is object-oriented whereas POP is structure oriented
 2. In OOP the program is divided into objects whereas in POP the program is divided into functions
 3. OOP is a bottom-up approach whereas POP is a top-down approach
 4. In OOP encapsulation is used to hide the data whereas there is no data hiding in POP
 5. Inheritance property is used in OOP but not in POP

 

## 2. What's polymorphism in OOP?

Polymorphism is a core concept of OOP. It describes situations in which something occurs in several different forms. Specifically in computer science, it describes the concept that one can access objects of different types through the same interface. Each type can provide its own independent implementation of this interface.

### Polymorphism in addition operator
In python programs, its known that '+' operator is used extensively and has many uses. For example in interger data types, '+' operator is used to perform arithmetic addition operation. See below.

    a1 = 9
    d2 = 12
    print(a1+d2)
    
    21
For string data types, '+' operator is used to perform concatenation. See below.

    str1 = "My name is"
    str2 = "Reema"
    print(str1+" "+str2)
    
    My name is Reema

So we can see in the two code examples above that a single operator '+' has been used to carry out different operations for different data types. This is one of the most simple instances of polymorphism in Python.

### Function Polymorphism in Python
There are some functions in python which are compatible to run with multiple data types.

One function is the `len()` function. It can run with many data types in python. See below an example.

    print(len("Polymorphism"))
    print(len("Python"))
    print(len({"Name": "Reema", "Gender": "Female"}))
    
    12
    6
    2

So, in the above examples we can see that many data types such as string, list, tuple, set, and dictionary can work with the `len()` function. However, we can see that it returns specific information about specific data types. See the diagram below for a visual representation. 

![Functional Polymorphism](https://cdn.programiz.com/sites/tutorial2program/files/func-polymorphism.png)

### Class Polymorphism in Python

The concept of polymorphism can be used while creating class methods as Python allows different classes to have methods with the same name. Later on, calling these methods can be generalised by disregarding the object that is being worked with. See a class example below.

    class Dolphin:
	    def__init__(self, name, gender):
		    self.name = name
		    self.gender = gender
		
		def intro(self):
			print(f"Hi, I'm {self.name} the {self.gender} dolphin.")

	    def make_sound(self):
		    print("Whistle")
	
	class Whale:
	    def__init__(self, name, gender):
		    self.name = name
		    self.gender = gender
		
		def intro(self):
			print(f"Hi, I'm {self.name} the {self.gender} whale.")

	    def make_sound(self):
		    print("Click")
	
	doplhinA: Dolphin("Sandy", "female")
	whaleA: Whale("Bill", "male")

	for sea_creature in (dolphinA, whaleA):
		sea_creature.make_sound()
		sea_creature.intro()
		sea_creature.make_sound()
		
		
		Whistle
		Hi, I'm Sandy the female dolphin.
		Whistle
		Click
		Hi, I'm Bill the male whale.
		Click
	
In the above example, two classes have been created `Dolphin` and `Whale`. They both have a similar structure and have the same method names `intro()` and `make_sound()`.  But you can see that there is no common superclass or any way to linked the classes together. These two different objects can be packed together into a tuple and be iterated through using a common `animal` variable. This is possible due to polymorphism. 

### Polymorphism and Inheritance
The child classes in python inherit methods and attributes from the parent class (this is common in other programming languages too). Certain methods and attributes can be redefined to fit specific child classes - this is known as **method overriding**. 

Polymorphism can allow programmers to access these overridden methods and attributes that have the same name as the parent class. See an example of this below.

    from chemistry import bonding
    
    class Bonds:
	    def __init__(self, name):
		    self.name = "Chemical Bonding"
			
		def show(self):
			print(self.name)
			
	class Covalent(Bonds):
		def __init__(self):
			self.name = "Covalent Bonds"
		def show(self):
			print(self.name)
			
	chem1 = Bonds()
	chem2 = Covalent()
	
	chem1.show()
	chem2.show()
	
	
	Chemical Bonding
	Covalent Bonds
  
In the above example, it is the version of a method that is executed that will be determined by the object that is used to invoke it. In a scenario where the object of a parent class is used to invoke the method, then the version in the parent class will be executed. However if an object of the subclass is used to invoke the method, then the version in the child class will be executed. In summary, it is the type of the object being referred to (not the type of the reference variable) that determines which version of an overridden method will be executed.

	


# 3. What's inheritance in OOP?

Inheritance allows use to define a class that inherits all methods and properties from another class.

**Parent class** = the class that is being inherited from

**Child class** = the class that inherits from another class

#### Python inheritance syntax:

    class parentClass:
	    {body}
	class childClass(parentClass):
		{body}

See below an example.

Firstly, a **parent class** is established.

    class Me(object):
	    def__init__(self, name, id):
		    self.name = name
		    self.id = id
		    
		def show(self):
			print(self.name, self.id)
			
	intro = Me("Reema", 264)
	intro.show()
	
	
	Reema 264

Secondly, a **child class** is established and inherits the properties of the parent class.

    class Intro(Me):
	    def Greet(self):
		    print("Hi there! Nice to meet you both.")
	Intro_response = Intro("Alexis", 119)
	Intro_response.show()
	Intro_response.Intro()
	
	
	Alexis 119
	Hi there! Nice to meet you both.

# 4. If you had to make a program that could vote for the top three funniest people in the office, how would you do that? How would you make it possible to vote on those people?

An online voting system can be created in python using a list data structure. See below a voting system that can be used to determine the top 3 funniest people in the office.

    def max_3(num):
	    first, second, third = sorted(num[:3], reverse=True)
	    try:
		    for number in num[3:]:
			    if number > first:
				    first, second, third = number, first, second
			    elif number > second:
				    second, third = number, second
			    elif number > third:
				    third = number
		    return [first, second, third]
    
    already_voted = []
    
    while len(already_voted) < 8:
	    votes = {}
	    voters = ["Aimee", "Ben", "Carrie", "Derrick", "Elvis"]
	    voter_name = input("What is your name? ")
	    
    # A loop will check whether all voters have voted
    if voter_name in already_voted or voter_name not in voters:
	    print("Sorry, you've already voted, you are unable to vote again.")
	    break
    else:
    print("You have been successfully registered.")
    funniest_person = input("Please choose who you vote for as the funniest person in the office! ")
    voter_name = []
    for candidates in votes:
	    if funniest_person in votes:
		    votes[funniest_person] += 1
    else:
		    votes[candidates] = 1
		    already_voted = already_voted.append(voter_name)
    print(max_3(votes.items()))
    
    
    
    Ben, Carrie, Elvis



# 5. What's the software development cycle?

### Summary

The software development cycle (SDLC) is a framework that defines tasks performed at each step in the software development process/timeline. The life cycle defines a methodology for improving the quality of software and the overall development process. SDLC is essentially the structure which is used by a development team within a software company. The main aim of the SDLC is to produce high quality software that exceeds customer expectations, meets deadlines and cost estimates.

### How does the SDLC work?

The SDLC outlines each task required to put together a software application. The cycle helps to reduce waste and increase the efficiency of the development process. There are different variations to a SDLC, depending on what company you work for and how they choose to structure it however, they generally all folllow the 7 phases of the SDLC. These phases have been outlined below.

**1. Planning**
In the **planning phase**, project leaders evaluate the terms of the project. This includes calculating any material costs and labour, creating a timetable with target goals, as well as creating the project's teams and leadership structure. This stage can also include feedback from stakeholders (stakeholders = anyone who stands to benefit from the application). 
The planning phase should clearly define the purpose and scope of the application. This can allow for the development team to effectively create the software. It also sets the boundaries to help keep the project from expanding or shifting from its original purpose.

**2. Define Requirements**
To some, this is considered as part of the planning phase. To define the requirements in the SDLC means to determine what the application is supposed to do and its requirements. For example, a game application would most likely require the ability to have multiple levels of difficulty. A social media application would require the ability to connect with a friend and/or family member. The requirements also include definding the resources needed to build the project. For example, a team might develop an x-ray software to scan bones. The x-ray is a requirement in the process.

**3. Design and Prototyping**
The **design phase** imitates the way a software application will work. Some aspects of the design phase include:

 - **Architecture**: specifies the programming language, industry practices, overall design, and use of any templates or boilerplate
 - **User Interface**: defines the ways customers interact with the software, and how the software responds to input
 - **Platforms**: defines the platforms on which the software will run i.e. Apple, Android, Linux etc
 - **Programming**: the programming language (in thorough detail) i.e. methods of solving problems and performing tasks in the application are specified here
 - **Communication**: defines the methods that the application can communicate with other assets, such as a central server
 - **Security**: defines the measures taken to secure the application; this may include SSL traffic (Secure Sockets Layer), encryption, password protection, face/ fingerprint identification

**Prototyping** is thought of as part of the design phase. A prototype is an early (test) version of the software in the iterative software development model. It demonstrates a basic idea of how the applications works and looks.  The prototype is usually shown to stakeholders where feedback is often welcome in order to improve the application. It's cheaper to make changes in the prototype phase than to rewrite code to make changes in the development phase.

**4. Software Development**
The software development (SD) phase is the actual writing of the program. Usually a larger project will be broken up and divided into smaller sections for several developers to work on whereas, a smaller project can be written by a few or even a single developer. An access control or source code management application is used in this phase; they help developers to track changes to the code. They also help ensure compatability between different team projects and target goals are being met. The coding process includes many other tasks. 

Many developers need to recap their skills or work as a team. It is critical that in this phase erros and glitches are found and fixed. It is usually the many tasks that hold up the development process, such as waiting for test results or compiling code in order for an application to run. The SDLC can anticipate these delays so that developers can take on other duties. 

Software developers appreciate instructions and explanations. Documentation can be a formal process, including writing a user guide for the application. On the other hand, it can also be informal. For example, it's normal for comments in the source code to be made; this is to explain why a developer used a certain procedure.

**5. Testing**
The testing phase is a very crucial part of the SDLC as it's important to test an application before making it available to users. Much of the testing can be automated, for example security testing. Other forms of testing can only be carried out in a specific environment. For example, creating a simulated production environment for complex deployments. 

The testing phase should ensure that each function works correctly. Different parts of the application should also be tested to work seamlessly together - performance test, to reduce any lags in processing. This phase therefore helps to reduce the number of bugs and glitches that users may encounter. Overall, the aim is to have a higher user satisfaction and a better usage rate.

**6. Deployment**
In the deployment phase, the application is made available to users. Many companies usually prefer to automate the deployment phase. This can be a download link on the company website. It could also be downloading an application on a smartphone. Deployment can also be complex. For example, there are instances of upgrading a company-wide database to a newly-developed application. 

**7. Operations and Maintenance**
In the **operation and maintenance** phase users will usually discover bugs that weren't found during testing. These errors need to be resolved, which can generate new development cycles. In addition to bug fixes, models like the **Iterative Development** plan for additional features in future releases. For each new release, a new development cycle can be launched.

## 6. What's the difference between agile and waterfall?

### Agile
The agile model was designed by developers to put customer needs first. This method focuses strongly on user experience and input. The agile method solves much of the problems of older applications that were very difficult to use. Furthermore, it makes the software highly responsive to customer feedback. Agile method seeks to release software cycles quickly, in order to keep up with trends and respond to a changing market. This requires a strong team with excellent communication. However, this can  lead to a project going off track by relying too heavily on customer feedback.

### Waterfall
The waterfall (WF) SDLC model is the class method of development. Essentially, this is similar to a sequential model. The software development activity is divided into different phases and each phase consists of a series of tasks and has different objectives. In waterfall, the development of one phase begins only when the previous phase has been successfully completed. 

### Differences between the two:

 1. WF is a linear sequential system of working that requires the team to complete each project phase before moving onto the next one whereas agile encourages the team to work simulatenously on different phases of the project.
 2. Agile is known for its flexibility whereas WF is a structured software development methodology.
 3. Agile allows changes in project development requirement whereas WF has no scope of changing the requirements once the project development starts.
 4. WF has a fixed timeline - the idea is that the start and finish of the project are already mapped out from the beginning. Agile on the other hand is a lot more flexible and accounts for experimenting with different directions. Unlike WF, the schedule adapts as the project progresses. 
 5.  WF does not involve the client or project owner during the process. Only in cases of specific check-ins or for deliverables do they get involved. This is because the course of the project is outlined from the start therefore incorporating client feedback is not an ongoing part of the process. On the contrary, client involvement is a fundamental part of agile. Business owners are expected to be involved and give feedback to the software development team as they progress through the various phases of the project.


## 7. What is a reduced function used for?

In python, the `reduce()` function allows you to reduce a list in a more concise way.

The `reduce()` function applies the `fn` function of two arguments cumulatively to the items of the list, from left to right, to reduce the list into a single value.

> **Note:** `reduce()` is not a builin function in Python. It belongs to the `functools` module.

To use this function, you need to import it from the `functools` module using the following statement at the top of the file:

    from functools import reduce

See below an example illustrating how to use the `reduce` function to calculate the sum of elements of the `points` list:

    from functools import reduce
    
    def sum(a, b):
	    print(f"a={a}, b={b}, {a} + {b} ={a+b}")
	    return a + b
    
    
    points = [75, 65, 80, 95, 50]
    total = reduce(sum, points)
    print(total)
    
    
    
    a=75, b=65, 75 + 65 = 140 
    a=140, b=80, 140 + 80 = 220 
    a=220, b=95, 220 + 95 = 315 
    a=315, b=50, 315 + 50 = 365  
    365
    
You can see in the above code that the `reduce` function cumulatively adds two elements of the list from left to right and reduces the whole list into a single value.  You can make this code more concise by using the **lambda expression** instead of defining the `sum` function. See below.

    from functools import reduce
    
    points = [75, 65, 80, 95, 50]
    
    total = reduce(lambda a, b: a + b, points)
    
    print(total)
    
    
    365
    

## 8. How does merge sort work?

Merge sort is one of the most famous sorting algorithms (alongside quick sort). It is a general-purpose sorting algorithm and is a classic example of a *divide-and-conquer* algorithm.

This is how it works:

An initial array (a list of objects of the same type, or different depending on the programming language you are using, with an associated index) is divided into two roughly equal parts. If the array has an odd number of elements, one of those "halves" is by one element larger than the other. 

The subarrays are continously divided into halves until you end up with arrays that have only one element each. You then combine the pairs of one-element arrays into two-element arrays, sorting them in the process. Then these sorted pairs are merged into n-element arrays, and so on until you end up with the initial array sorted.

Below is a visual representation:

![merge sort visualization](https://stackabuse.s3.amazonaws.com/media/merge-sort-in-python-1.png)

**Algorithm:**
1. Start
2. Declare array and left, right, and mid variable
3. Perform merge function
	a. mergesort(array, left, right)
	b. if left >= right
	c. return
	d. mid= (left+right)/2
	e. mergesort(array, left, mid)
	f. mergesort(array, mid+1, right)
	g. merge(array, left, mid, right)
4. Stop

See below the code representation:

- The base idea of the algorithm is to divide (sub)arrays into halves and sort them recursively. We want to keep doing this as much as possible i.e. until we end up with subarrays that have only one element:

def merge_sort(array, left_index, right_index):
	
    def merge_sort(array, left_index, right_index):
	    if = left_index >= right_index:
		    return

    middle = (left_index + right_index)//2
    merge_sort(array, left_index, middle)
    merge_sort(array, middle + 1, right_index)
    merge(array, left_index, right_index, middle)

By calling the merge method last, we make sure that all the divisions will happen before we start the sorting. `//` is used to make it clear that integer values for the indicies is what we want.

Now, the next step involves the actual merging part through a few steps:

 - Create copies of our arrays. The first array being the subarray from *[left_index, .., middle]* and the second from *[middle+1,...,right_index]*
 - We go through both copies (keeping track of pointers in both arrays), picking the smaller of the two elements we're currently looking at, and add them to our sorted array. Then, we move forward in whichever array we've chosen the element from, and forward in the sorted array regardless. 
 - If we run out of elements in one of our copies, simply add the remaining elements in the other copy to the sorted array.

Let's define a `merge` function:
  
    # Make copies of both arrays we're trying to merge
    def merge(array, left_index, right_index, middle):
    
	# The second parameter is non-inclusive, so it has to be increased by 1
	    left_copy = array[left_index:middle + 1]
	    right_copy = array[middle+1:right_index+1]
	    
	# Initial values for variables that are used to keep tracm of where we are in each array
	    left_copy_index = 0
	    right_copy_index = 0
	    sorted_index = left_index
	    
	    
	# Go through both copies until we run out of elements in one
	while left_copy_index < len(left_copy) and right_copy_index < len(right_copy):
	
	# If the left_copy has the smaller element, put it in the sorted part and then move forward in left_copy (by increasing the pointer)
	if left_copy[left_copy_index] <= right_copy[right_copy_index]:
	   array[sorted_index] = left_copy[left_copy_index]
	   left_copy_index = left_copy_index + 1
	else:
		array[sorted_index] = right_copy[right_copy_index]
		right_copy_index = right_copy_index + 1
	
	# Regardless of where the element is from, move forward in the sorted part
	sorted_index = sorted_index + 1
	
	# When we run out of elements in either left_copy or right_copy we go through the remaining elements and add them
	while left_copy_index < len(left_copy):
		array[sorted_index] = left_copy[left_copy_index]
		left_copy_index = left_copy_index + 1
		sorted_index = sorted_index + 1


    array = [33, 42, 9, 37, 8, 47, 5, 29, 49, 31, 4, 48, 16, 22, 26]
    merge_sort(array, 0, len(array) - 1)
    print(array)
    
    
    [4, 5, 8, 9, 16, 22, 26, 29, 31, 33, 37, 42, 47, 48, 49]
	   

# 9. Generators - Generator functions allow you to declare a function that behaves like an iterator, i.e. it can be used in a for loop. What is the use case?

A common use case of generators is work with data streams or large files like .csv files. These text files separate data into columns by using commas. The format is a common way to share data. You are also able to count the number of rows in a .csv file. See below.

    csv = csv_reader("large_csv.txt")
    row_count = 0
    
    for row in csv:
	    row_count += 1
	    
	print(f"Row count is {row_count}")

From the example, it's expected that `csv` is a list. To populate this list, `csv_reader()` opens a file and loads its contents into `csv`. The programme then iterates over the list and increments `row_count` for each row.

But what if the file was very large? Would this still work? We can assume that `csv_reader()` just opens the file and reads it into an array. See below.

    def csv_reader(file_name):
	    for row in open(file_name, "a"):
	    yeild row

# 10. Decorators - A page for useful (or potentially abusive?) decorator ideas. What is the return type of the decorator?

Decorators allow programmers to modify the behaviour of a function or class. They also allow programmers to wrap another function in order to extend the behaviour of the wrapped function, without permanently modifying it. 

In decorators, functions are taken as the argument into another function and then called inside the wrapper function. See below.

    def hello_decorator(func):
    
    	def innerA():
	    	print("Hey Emily, Shepstone, and Ali! This is before the function execution.")
	    	
	    	func()
	    	
	    	print("This is after the execution.")
	    
	    return innerA
	    
	    
	def func_to_be_used():
	print("This is inside the function!")
	
	func_to_be_used = hello_decorator(func_to_be_used)
	
	
	func_to_be_used()
	
	
	Hey Emily, Shepstone, and Ali! This is before the function execution.
	This is inside the function!
	This is after the execution.


## What if a function returns something or an argument is passed to the function?

In the above example, the functions didn't return anything so there was no issue however, a returned value may be required. See below an example.

    def hello_decorator(func):
	    def innerA(*args, **kwargs):
	    
		    print("before execution")
		    
		    returned_value = func(*args, **kwargs)
		    print("after execution")
		    
		    return returned_value
		   
		return innerA
		
		
	@hello_decorator
	def sum_two_num(a, b):
		print("inside the function")
		return a + b
		
	a, b = 9, 15
	
	print("sum =", sum_two_num(a, b))
	
	
	before execution
	inside the function
	after execution
	sum = 24
	