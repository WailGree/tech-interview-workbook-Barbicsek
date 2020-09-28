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

*Scope resolution via LEGB rule: <br>*
*In Python, the LEGB rule is used to decide the order in which the namespaces are to be searched for scope resolution. <br>*
*The scopes are listed below in terms of hierarchy(highest to lowest/narrowest to broadest): <br>*

*Local(L): Defined inside function/class <br>*
*Enclosed(E): Defined inside enclosing functions(Nested function concept) <br>*
*Global(G): Defined at the uppermost level <br>*
*Built-in(B): Reserved names in Python builtin modules* 

#### What’s the difference between const and var in JavaScript?

*Var variables can be updated and re-declared within its scope; const variables can neither be updated nor re-declared. They are all hoisted to the top of their scope. But while var variables are initialized with undefined ,const variables are not initialized.*

#### How the list comprehension looks like in Python?
```Python
h_letters = [ letter for letter in 'human' ]
```
*print( h_letters)<br>*

*When we run the program, the output will be:<br>*        

*['h', 'u', 'm', 'a', 'n']*



#### How the “ternary expression” looks like in Python?
```Python
<expression1> if <condition> else <expression2>
```

  
*This example will print whether a number is odd or even: <br>*
    *n = 5 <br>*
    *print("Even") if n % 2 == 0 else print("Odd")*




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

*The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called as recursive function. Using recursive algorithm, certain problems can be solved quite easily.*

#### Write a recursive function which calculates the Fibonacci numbers!

```Python
 function fibo(limit, a=0, b=1) {
        if (b >= limit) {
            return
        }
        let c = a + b;
        console.log(c);
        return fibo(limit, b, c)
    }
    
    fibo(30);
```

#### How to store a function in a variable in Python?

```Python
def my_function():
  print(20)
function_variable = my_function
print(function_variable)
```

#### List the ways of defining a callable logical unit in JavaScript!

  - *arrow function*
  ```Javascript
    const foo = (arg1, arg2) => {
        ...
    };
 ```
  - *concise method syntax:*
  ```Javascript
    let obj = {
        myMethod(arg1, arg2) {
            ...
        }
    };
```

#### What is an event listener? How to attach one?

*The EventListener interface represents an object that can handle an event dispatched by an EventTarget object.*

```Javascript
const buttonElement = document.getElementById('btn');

buttonElement.addEventListener('click', function (event) {
  alert('Element clicked through function!');
});
```

#### How to trigger an event in JavaScript?

*Event listeners have a target, which they listen for. It can be triggered by:*
  - *mouse actions*
  - *keyboard actions*
  - *content load (or change) actions*

#### What is a callback function? Tell some examples of its usage.

*In JavaScript, functions are objects. Because of this, functions can take functions as arguments, and can be returned by other functions. Functions that do this are called higher-order functions. Any function that is passed as an argument is called a callback function.*

```
function doHomework(subject, callback) {
  alert(`Starting my ${subject} homework.`);
  callback();
}
function alertFinished(){
  alert('Finished my homework');
}
doHomework('math', alertFinished);
```

#### What is a Python decorator? How does it work? Tell some examples of its usage.

*A decorator is a design pattern in Python that allows a user to add new functionality to an existing object without modifying its structure. Decorators are usually called before the definition of a function you want to decorate.*

```
def smart_divide(func):
    def inner(a, b):
        print("I am going to divide", a, "and", b)
        if b == 0:
            print("Whoops! cannot divide")
            return

        return func(a, b)
    return inner


@smart_divide
def divide(a, b):
    print(a/b)
``` 

#### What is the difference between synchronous and asynchronous execution?

*When you execute something synchronously, you wait for it to finish before moving on to another task. When you execute something asynchronously, you can move on to another task before it finishes.*

## Programming languages

### SQL

#### How can you connect your application to a database server? What are the possible ways?
#### When do you use the DISTINCT keyword in SQL?

*The SELECT DISTINCT statement is used to return only distinct (different) values.*

*Inside a table, a column often contains many duplicate values; and sometimes you only want to list the different (distinct) values.*

#### Talk about the behavior/goal of these base SQL clauses: WHERE, GROUP BY, HAVING, ORDER BY?

- *WHERE:* <br>

  *The WHERE clause is used to filter records.  The WHERE clause is not only used in SELECT statement, it is also used in UPDATE, DELETE statement.*<br>
- *GROUP BY:* <br>

  *The GROUP BY statement groups rows that have the same values into summary rows, like "find the number of customers in each country.The GROUP BY statement is      often used with aggregate functions (COUNT, MAX, MIN, SUM, AVG) to group the result-set by one or more columns.*
- *HAVING:* <br>

  *A HAVING clause in SQL specifies that an SQL SELECT statement should only return rows where aggregate values meet the specified conditions. It was added to the    SQL language because the WHERE keyword could not be used with aggregate functions.*
- *ORDER BY:* <br>

  *The ORDER BY keyword is used to sort the result-set in ascending or descending order.The ORDER BY keyword sorts the records in ascending order by default. To      sort the records in descending order, use the DESC keyword.*
  
#### What are aggregate functions in SQL? Give 3 examples.

*In database management an aggregate function is a function where the values of multiple rows are grouped together as input on certain criteria to form a single value of more significant meaning.*

1) *Count()*
2) *Sum()*
3) *Avg()*

#### What kind of JOIN types do you know in SQL? Could you give examples?

*Here are the different types of the JOINs in SQL:*

- *(INNER) JOIN: Returns records that have matching values in both tables*
    ``` 
    SELECT Employee.EmpID, Employee.EmpFname, Employee.EmpLname, Projects.ProjectID, Projects.ProjectName
    FROM Employee
    INNER JOIN Projects 
    ON Employee.EmpID=Projects.EmpID;
    ```  
- *LEFT (OUTER) JOIN: Returns all records from the left table, and the matched records from the right table*
     ``` 
    SELECT Employee.EmpFname, Employee.EmpLname, Projects.ProjectID, Projects.ProjectName
    FROM Employee
    LEFT JOIN
    ON Employee.EmpID = Projects.EmpID ;
     ``` 
- *RIGHT (OUTER) JOIN: Returns all records from the right table, and the matched records from the left table*
    ``` 
    SELECT Employee.EmpFname, Employee.EmpLname, Projects.ProjectID, Projects.ProjectName
    FROM Employee
    RIGHT JOIN
    ON Employee.EmpID = Projects.EmpID;
    ``` 
- *FULL (OUTER) JOIN: Returns all records when there is a match in either left or right table*
    ``` 
    SELECT Employee.EmpFname, Employee.EmpLname, Projects.ProjectID
    FROM Employee
    FULL JOIN Projects
    ON Employee.EmpID = Projects.EmpID;
    ``` 
    
#### What are the constraints in sql?

*SQL constraints are used to specify rules for data in a table.Constraints can be specified when the table is created with the CREATE TABLE statement, or after the table is created with the ALTER TABLE statement.*

*The following constraints are commonly used in SQL:*

- *NOT NULL - Ensures that a column cannot have a NULL value*
- *UNIQUE - Ensures that all values in a column are different*
- *PRIMARY KEY - A combination of a NOT NULL and UNIQUE. Uniquely identifies each row in a table*
- *FOREIGN KEY - Uniquely identifies a row/record in another table*
- *CHECK - Ensures that all values in a column satisfies a specific condition*
- *DEFAULT - Sets a default value for a column when no value is specified*
- *INDEX - Used to create and retrieve data from the database very quickly*

#### What is a cursor in SQL? Why would you use one?

*A cursor is a temporary work area created in the system memory when a SQL statement is executed.<br> 
A cursor contains information on a select statement and the rows of data accessed by it.<br>
This temporary work area is used to store the data retrieved from the database, and manipulate this data. A cursor can hold more than one row, but can process only one row at a time. The set of rows the cursor holds is called the active set.*

#### What are database indexes? When to use?

*A database index allows a query to efficiently retrieve data from a database.  Indexes are related to specific tables and consist of one or more keys.  A table can have more than one index built from it.  The keys are a fancy term for the values we want to look up in the index.  The keys are based on the tables’ columns.  By comparing keys to the index it is possible to find one or more database records with the same value.*

#### What are database transactions? When to use?

*A database transaction symbolizes a unit of work performed within a database management system (or similar system) against a database, and treated in a coherent and reliable way independent of other transactions. A transaction generally represents any change in a database.*

#### What kind of database relations do you know? How to define them?

*There are 3 types of relationships in relational database design. They are:*

- *One-to-One:*

  *This is not a common relationship type, as the data stored in table B could just have easily been stored in table A. However, there are some valid reasons for   using this relationship type. A one-to-one relationship  can be used for security purposes, to divide a large table, and various other specific purposes.*
  
- *One-to-Many (or Many-to-One):*

  *This is the most common relationship type. In this type of relationship, a row in table A can have many matching rows in table B, but a row in table B can have    only one matching row in table A.*
  
- *Many-to-Many:*

  *In a many-to-many relationship, a row in table A can have many matching rows in table B, and vice versa*

  *A many-to-many relationship could be thought of as two one-to-many relationships, linked by an intermediary table.*

  *The intermediary table is typically referred to as a “junction table” (also as a “cross-reference table”). This table is used to link the other two tables       together. It does this by having two fields that reference the primary key of each of the other two tables.*

#### You have a table with an “address” field which contains data like “3525, Miskolc, Régiposta 9.” (postcode, city, street name and address). How would you query all records related to Miskolc?

```SQL
SELECT * FROM table
WHERE city = 'Miskolc';
```

#### How would you keep track of what kind of data has changed after an UPDATE or DELETE operation in a table?

*I would create a person_log table and create a trigger on that will insert a row into person_log table whenever the table/s row/s get updated/deletes/added.*

### HTML & CSS

#### What’s the difference between XML, XHTML and HTML?

- *HTML:* 

  * HTML is the HyperText Markup Language, which is designed to create structured documents and provide for semantic meaning behind the documents.*

- *XML:*

  * XML is the Extensible Markup Language, which provides rules for creating, structuring, and encoding documents. It's programming language-agnostic - all of the    major programming languages provide mechanisms for reading and writing XML documents, either as part of the core or in external libraries.*

- *XHTML:*

  *XHTML is an XML-based HTML. It serves the same function as HTML, but with the same rules as XML documents. These rules deal with the structure of the markup.*

#### How to include a JavaScript file in a webpage?

*Using the script tag in .html file:*
```HTML
<script type="text/javascript" src="path-to-javascript-file.js"></script>
```
#### How to include a CSS file in a webpage?

*Using the link tag in .html file:*
```HTML
<link rel="stylesheet" type="text/css" href="stylesheet.css"/>
```

#### How to select an element using its id in CSS?

*You have to use the hashtag(#) + the element id name:***
```CSS
#elementIdName {
    /*code;*/
}
```

#### How to select elements using their class in CSS?

*You have to use the dot(.) + the element class name:*
```CSS
.elementClassName {
    /*code;*/
}
```
#### How to select elements which have the ‘alpha’ and ‘beta’ classes in CSS?

*You have to define in css file with dot classname dot classname:*
```CSS
.alpha.beta{color:yellow;}
/*here you can reach the beta class*/
```
#### How to select all list items in all ordered lists on the page in CSS?

*You can reach by using the ordered tag which is < ol >:*
```CSS
ol {
 /*code;*/
}
```
#### How to select elements using their attributes in CSS?

*The [attribute=value] selector is used to select elements with the specified attribute and value.*
```CSS
a[target=_blank] {
  background-color: yellow;
}
```

#### What are UX and UI?

- *UI(User Interface Design):*

  *Simply put, user interface (UI) is anything a user may interact with to use a digital product or service. This includes everything from screens and                touchscreens, keyboards, sounds, and even lights. To understand the evolution of UI, however, it’s helpful to learn a bit more about its history and how it has   evolved into best practices and a profession.*
  
- *UX(User Experience Design):*

  *User experience, or UX, evolved as a result of the improvements to UI. Once there was something for users to interact with, their experience, whether positive,   negative, or neutral, changed how users felt about those interactions.*

#### Please list some points that an application should fulfill to have good UX.

  - *Meet the users' needs*
  - *Have a clear hierarchy*
  - *Consistency*
  - *Understand accessibility*
  - *Usability*

#### What is XML, XSLT, DTD?

- *XML:*

  *XML is a software- and hardware-independent tool for storing and transporting data.*

- *XSLT:*

  *XSLT (eXtensible Stylesheet Language Transformations) is the recommended style sheet language for XML.With XSLT you can transform an XML document into HTML.*
  
- *DTD:*

  *A DTD is a Document Type Definition.A DTD defines the structure and the legal elements and attributes of an XML document.*
  
#### What is the difference between HTML and XML?

*KEY DIFFERENCE:*

- *XML is abbreviation for eXtensible Markup Language whereas HTML stands for Hypertext Markup Language.*
- *XML mainly focuses on transfer of data while HTML is focused on presentation of the data.*
- *XML is content driven‭‬‬‬‬‬‬‬‬‬‬‬‬‬‬‬ whereas HTML is format driven‭‬‬‬‬‬‬‬.*
- *XML is Case sensitive while HTML is Case insensitive.*
- *XML provides namespaces support while HTML doesn't provide namespaces support.*
- *XML is strict for closing tag while HTML is not strict.*
- *XML tags are extensible whereas HTML has limited tags.*
- *XML tags are not predefined whereas HTML has predefined tags.*

### Javascript

#### What is javascript?

*JavaScript was initially created to “make web pages alive”.*

*The programs in this language are called scripts. They can be written right in a web page’s HTML and run automatically as the page loads.*

*Scripts are provided and executed as plain text. They don’t need special preparation or compilation to run.*

*In this aspect, JavaScript is very different from another language called Java.*

*For instance, in-browser JavaScript is able to:*

- *Add new HTML to the page, change the existing content, modify styles.*
- *React to user actions, run on mouse clicks, pointer movements, key presses.*
- *Send requests over the network to remote servers, download and upload files (so-called AJAX and COMET technologies).*
- *Get and set cookies, ask questions to the visitor, show messages.*
- *Remember the data on the client-side (“local storage”).*


#### When to use AJAX? Bring examples of its usage.

*AJAX = Asynchronous JavaScript And XML.*

*AJAX is not a programming language. AJAX just uses a combination of:*

- *A browser built-in XMLHttpRequest object (to request data from a web server)*
- *JavaScript and HTML DOM (to display or use the data)*

*AJAX allows web pages to be updated asynchronously by exchanging data with a web server behind the scenes. This means that it is possible to update parts of a web page, without reloading the whole page.*

#### What is DOM and how to manipulate it from Javascript?

*DOM - Document Object Model DOM is representative displaying for the according html document, and those objects can be modified.<br>*
  - *Creating, removing or replacing an element*
  - *Modifying an element's text and/or HTML content*
  - *Getting an element content and working with it*

```Javascript
let element = document.querySelector('selector')
```
/* You can use it to get the element from the DOM and save
it as a variable, and manipulate it.  */

#### What are events and how/why to use them in Javascript?

*JavaScript's interaction with HTML is handled through events that occur when the user or the browser manipulates a page.*

*When the page loads, it is called an event. When the user clicks a button, that click too is an event. Other examples include events like pressing any key, closing a window, resizing a window, etc.*

*Developers can use these events to execute JavaScript coded responses, which cause buttons to close windows, messages to be displayed to users, data to be validated, and virtually any other type of response imaginable.*

*Events are a part of the Document Object Model (DOM) Level 3 and every HTML element contains a set of events which can trigger JavaScript Code.*

```Javascript
let btn = document.querySelector('button');
btn.addEventListener('click',function(event) {
  }
);
```

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
