# Web with Python questions

## Software design

### Clean code

#### Point out 5 suggestions, how to format an SQL query!

  1. *Descriptive related but different database and table names*
  2. *Keywords and expressions are aligned into separate columns*
  3. *Indented new line after every logical step*
  4. *Query parameters indented to create a block like body*
  5. *Commas are at the end of the line*
  
#### What layers can you name in a simple web application?

  - *View*
  - *Application service*
  - *Database*
  - *Domain*

### Error handling
#### What error can occur, when an array does not have an element on the requested index?

*IndexError*

#### What is the “finally” block, and how would you use it?

*The finally-block contains statements to execute after the try-block and catch-block(s) execute, but before the statements following the try...catch...finally-block. The finally-block executes regardless of whether an exception is thrown. Also, if an exception is thrown, the statements in the finally-block execute even if no catch-block handles the exception.*

#### Why should we catch special exception types?

*Exception handling is important because it helps maintain the normal, desired flow of the program even when unexpected events occur. If exceptions are not handled, programs may crash or requests may fail.*

### Security
#### What is SQL injection? How to protect an application against it?

*SQL injection is a type of injection attack. Injection attacks occur when maliciously crafted inputs are submitted by an attacker, causing an application to perform an unintended action. Because of the ubiquity of SQL databases, SQL injection is one of the most common types of attack on the internet.*

*Developers can prevent SQL Injection vulnerabilities in web applications by utilizing parameterized database queries with bound, typed parameters and careful use of parameterized stored procedures in the database.*

#### What is XSS? How to protect an application against it?

*Cross-site scripting (also known as XSS) is a web security vulnerability that allows an attacker to compromise the interactions that users have with a vulnerable application. It allows an attacker to circumvent the same origin policy, which is designed to segregate different websites from each other.*

*In general, effectively preventing XSS vulnerabilities is likely to involve a combination of the following measures:*
- *Filter input on arrival.*
- *Encode data on output.*
- *Use appropriate response headers.*
- *Content Security Policy.*

#### How to properly store passwords?

*You have to hash them and then store the outcome in a database.*

#### What is HTTPS?

*Hypertext transfer protocol secure (HTTPS) is the secure version of HTTP, which is the primary protocol used to send data between a web browser and a website. HTTPS is encrypted in order to increase security of data transfer.* 

#### What is encryption and decryption?

*Encryption is the process of converting normal message (plaintext) into meaningless message (Ciphertext).*

*Decryption is the process of converting meaningless message (Ciphertext) into its original form (Plaintext).*

#### What is hashing?

*Hashing is the process of converting a given key into another value. A hash function is used to generate the new value according to a mathematical algorithm. The result of a hash function is known as a hash value or simply, a hash.*

#### What is the difference between encryption and hashing? When would you use which?

*Encryption is a two-way function; what is encrypted can be decrypted with the proper key. Hashing, however, is a one-way function that scrambles plain text to produce a unique message digest. With a properly designed algorithm, there is no way to reverse the hashing process to reveal the original password.*

*Hashing:<br>
Ideal way to store passwords, as hashes are inherently one-way in their nature.(+ salt)*

*Encryption:<br>
Ideal for sending secure messages.*

#### What encryption methods do you know?

*The 4 common encryption methods:*

1. *Advanced Encryption Standard (AES)*
2. *Rivest-Shamir-Adleman (RSA)*
3. *Triple Data Encryption Standard (TripleDES)*
4. *Twofish*

#### What hashing methods do you know?

*Secure Hash Algorithm (SHA)*

#### How/where would you store sensitive data (like db password, API key, ...) of your application?

*The best would be to have a separate file with secrets encrypted. This file should be stored on some area which is not accessible by the application server.*

## Computer science

### Algorithms

#### What is the difference between Stack and Queue data structure?

| *STACKS* | *QUEUES* |
|:-:|:-:|
| *Stacks are based on the LIFO( Last in First out) principle, i.e., the element inserted at the last, is the first element to come out of the list.* | *Queues are based on the FIFO (First in First out) principle, i.e., the element inserted at the first, is the first element to come out of the list.* |
| *Insert operation is called push operation.* | *Insert operation is called enqueue operation.* |
| *Delete operation is called pop operation.* | *Delete operation is called dequeue operation.* |
| *In stacks we maintain only one pointer to access the list, called the top (last element).* | *In queues we maintain two pointers to access the list (first/last position).* |

#### What is BubbleSort? Describe the main logic of this sorting algorithm.

*Bubble Sort is a simple algorithm which is used to sort a given set of n elements provided in form of an array with n number of elements. Bubble Sort compares all the element one by one and sort them based on their values.*

*Following are the steps involved in bubble sort(for sorting a given array in ascending order):*
1. *Starting with the first element(index = 0), compare the current element with the next element of the array.*
2. *If the current element is greater than the next element of the array, swap them.*
3. *If the current element is less than the next element, move to the next element. Repeat Step 1.*

#### Explain the process of finding the maximum and minimum value in a list of numbers!

*Moving along the collection (iterate). Set the first as highest/lowest. Then comparing each next element with the firts and replace it with the first accordingly.*

#### Explain the process of calculating the average value in an array of numbers!

*Adding each element value together and dividing it with the the total element count.*

#### What is Big O complexity? Explain time and space complexity!

*Big O notation is a mathematical notation that describes the limiting behavior of a function when the argument tends towards a particular value or infinity.*

*The time complexity of an algorithm is the amount of time taken by the algorithm to complete its process as a function of its input length, n. The time complexity of an algorithm is commonly expressed using asymptotic notations.*

*The space complexity of an algorithm is the amount of space (or memory) taken by the algorithm to run as a function of its input length, n. Space complexity includes both auxiliary space and space used by the input.*

#### Explain the process of calculating the average value in a list of numbers!

*Sum all of the data values and divide by the number of nodes in the list.*

### Procedural
#### How the CASE condition works in SQL?

*The CASE statement goes through conditions and returns a value when the first condition is met (like an IF-THEN-ELSE statement). So, once a condition is true, it will stop reading and return the result. If no conditions are true, it returns the value in the ELSE clause.*

*If there is no ELSE part and no conditions are true, it returns NULL.*

#### How the switch-case condition works in JavaScript?

*The switch statement is used to perform different actions based on different conditions.*

*This is how it works:*

- *The switch expression is evaluated once.*
- *The value of the expression is compared with the values of each case.*
- *If there is a match, the associated block of code is executed.*
- *If there is no match, the default code block is executed.*

#### How to achieve a switch-case-like structure in Python?
```Python
def week(i):
        switcher={
                0:'Sunday',
                1:'Monday',
                2:'Tuesday',
                3:'Wednesday',
                4:'Thursday',
                5:'Friday',
                6:'Saturday'
             }
         return switcher.get(i,"Invalid day of week")
```

#### Explain variable scoping in Python!

*Scope resolution via LEGB rule:*
*In Python, the LEGB rule is used to decide the order in which the namespaces are to be searched for scope resolution.*
*The scopes are listed below in terms of hierarchy(highest to lowest/narrowest to broadest):*

*Local(L): Defined inside function/class*
*Enclosed(E): Defined inside enclosing functions(Nested function concept)*
*Global(G): Defined at the uppermost level*
*Built-in(B): Reserved names in Python builtin modules*

#### What’s the difference between const and var in JavaScript?

*Var variables can be updated and re-declared within its scope; const variables can neither be updated nor re-declared. They are all hoisted to the top of their scope. But while var variables are initialized with undefined ,const variables are not initialized.*

#### How the list comprehension looks like in Python?
```Python
h_letters = [ letter for letter in 'human' ]
print( h_letters)
```
*When we run the program, the output will be:

['h', 'u', 'm', 'a', 'n']*



#### How the “ternary expression” looks like in Python?
```Python
<expression1> if <condition> else <expression2>
```
  
*This example will print whether a number is odd or even:
    n = 5 <br>
    print("Even") if n % 2 == 0 else print("Odd")*



#### How the ternary expression looks like in JavaScript?

*with if/else:*
```Javascript
if (person.age >= 16) {
  person.driver = 'Yes';
} else {
  person.driver = 'No';
}
with tenary expression:
person.driver = person.age >=16 ? 'Yes' : 'No';
```
#### How to import a function from another module in Python?

```Python
from a import b, c
```

#### How to import a function from another module in JavaScript?

```Javascript
import "my-module.js";
    import myModule from "my-module.js";
    import {reallyReallyLongModuleMemberName as shortName} from "my-module.js";
```

### Functional
#### What is recursion?
#### Write a recursive function which calculates the Fibonacci numbers!
#### How to store a function in a variable in Python?
#### List the ways of defining a callable logical unit in JavaScript!
#### What is an event listener? How to attach one?
#### How to trigger an event in JavaScript?
#### What is a callback function? Tell some examples of its usage.
#### What is a Python decorator? How does it work? Tell some examples of its usage.
#### What is the difference between synchronous and asynchronous execution?

## Programming languages

### SQL

#### How can you connect your application to a database server? What are the possible ways?
#### When do you use the DISTINCT keyword in SQL?
#### Talk about the behavior/goal of these base SQL clauses: WHERE, GROUP BY, HAVING, ORDER BY?
#### What are aggregate functions in SQL? Give 3 examples.
#### What kind of JOIN types do you know in SQL? Could you give examples?
#### What are the constraints in sql?
#### What is a cursor in SQL? Why would you use one?
#### What are database indexes? When to use?
#### What are database transactions? When to use?
#### What kind of database relations do you know? How to define them?
#### You have a table with an “address” field which contains data like “3525, Miskolc, Régiposta 9.” (postcode, city, street name and address). How would you query all records related to Miskolc?
#### How would you keep track of what kind of data has changed after an UPDATE or DELETE operation in a table?

### HTML & CSS

#### What’s the difference between XML, XHTML and HTML?
#### How to include a JavaScript file in a webpage?
#### How to include a CSS file in a webpage?
#### How to select an element using its id in CSS?
#### How to select elements using their class in CSS?
#### How to select elements which have the ‘alpha’ and ‘beta’ classes in CSS?
#### How to select all list items in all ordered lists on the page in CSS?
#### How to select elements using their attributes in CSS?
#### What are UX and UI?
#### Please list some points that an application should fulfill to have good UX.
#### What is XML, XSLT, DTD?
#### What is the difference between HTML and XML?

### Javascript

#### What is javascript?
#### When to use AJAX? Bring examples of its usage.
#### What is DOM and how to manipulate it from Javascript?
#### What are events and how/why to use them in Javascript?
#### What is event bubbling/capturing? How would you use it?
#### What is JSON and how do we use it?

## Software engineering

### Version control

#### What type of branching strategy would you use?
#### What would you do if you find a bug on the production code (master branch)?
#### How can you move changes from one branch to another in GIT?
#### How does a VCS help with code reviews?
#### What is your favorite git command? Why?
#### What does remote/local mean in Git? 

### DevOps

#### Why is it good to use a package manager software?
#### Why is it good to use a virtual environment for a project?

### Networks

#### What kind of HTTP status codes do you know?
#### What is a API?
#### What is REST API?
#### What is JSON? When to use?
#### What is TCP/IP? What layers does it define, what are they responsible for?
#### What’s the difference between TCP and UDP?
#### How does an HTTP Request look like? What are the most relevant HTTP header fields?
#### How does an HTTP Response look like? What are the most relevant HTTP header fields?
#### What is DNS? How does it work?
#### What is a web server?
#### Explain the client-server architecture.
#### What would you use a session for?
#### What would you use a cookie for?

## Software Development Methodologies

#### What kind of software development methodologies do you know? What are the main features of these?
#### What are the SCRUM roles?
#### What are the SCRUM ceremonies?
#### What are the SCRUM artifacts?
#### What is the main goal of a retrospective meeting?
#### Explain, when would you recommend to use the waterfall methodology?
