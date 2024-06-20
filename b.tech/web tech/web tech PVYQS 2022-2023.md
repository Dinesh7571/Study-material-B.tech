# PYQP 2022-2023

**1. Attempt all questions in brief.**
**2 x 10 = 20**



**(a) Explain the concept of client and server. Also describe how a Web Server is different from a normal server.**

A client is a computer system or software application that requests services or resources from another computer system known as a server. The server is designed to process requests and deliver the necessary services or resources back to the client.

A Web Server specifically serves web pages to clients using the HTTP or HTTPS protocols, whereas a normal server might handle different types of requests and services such as file storage, database management, or email processing.

**(b) Differentiate between HTTP and HTTPS.**

| Feature | HTTP (HyperText Transfer Protocol) | HTTPS (HyperText Transfer Protocol Secure) |
| ----- | ----- | ----- |
| Security | Not secure, data is transmitted in plain text | Secure, data is encrypted using SSL/TLS |
| Port Number | 80 | 443 |
| URL Prefix | http:// | https:// |
| Data Integrity | No integrity checks | Ensures data integrity through encryption |
| Use Case | Suitable for non-sensitive data | Suitable for sensitive data like login, payment |
**(c) Differentiate between internet and WWW.**

| Aspect | Internet | WWW (World Wide Web) |
| ----- | ----- | ----- |
| Definition | Global network of interconnected computers | Collection of web pages and resources accessible via the internet |
| Protocols | Uses various protocols like TCP/IP, FTP, etc. | Primarily uses HTTP/HTTPS |
| Scope | Includes all types of communication and data transfer | Specifically refers to web-based information sharing |
| Services | Email, file transfer, VoIP, etc. | Websites, web applications, online content |
**(d) Compare Internet services with protocols.**

| Internet Service | Protocol |
| ----- | ----- |
| Email | SMTP, IMAP, POP3 |
| Web Browsing | HTTP, HTTPS |
| File Transfer | FTP, SFTP |
| Remote Access | SSH, Telnet |
| Instant Messaging | XMPP, SIP |
**(e) Discuss the history of WWW in brief.**

The World Wide Web (WWW) was invented by Tim Berners-Lee in 1989 while working at CERN. The first website was launched in 1991, which explained the concept and usage of the web. The introduction of web browsers like Mosaic in 1993 made the web more accessible, leading to its rapid growth. The WWW Consortium (W3C) was founded in 1994 to develop web standards. Since then, the web has evolved with advancements in web technologies, leading to the rich and interactive experiences we have today.

**(f) Compare Java Class and Interface.**

| Feature | Java Class | Java Interface |
| ----- | ----- | ----- |
| Definition | A blueprint for creating objects that define state and behavior | A reference type in Java, used to specify methods that a class must implement |
| Methods | Can have both defined and abstract methods | Can only have abstract methods (Java 8+ allows default and static methods) |
| Variables | Can have instance variables | Can have only static final constants |
| Inheritance | Supports single inheritance | Supports multiple inheritance (a class can implement multiple interfaces) |
| Instantiation | Can be instantiated directly | Cannot be instantiated |
**(g) Write a Simple program in Java to create an Applet able to display “Hello World” message upon execution.**

```java
import java.applet.Applet;
import java.awt.Graphics;

public class HelloWorldApplet extends Applet {
    public void paint(Graphics g) {
        g.drawString("Hello World", 20, 20);
    }
}
```
To run this, you need to use an HTML file:

```html
<!DOCTYPE html>
<html>
    <body>
        <applet code="HelloWorldApplet.class" width="300" height="300">
        </applet>
    </body>
</html>
```
**(h) Differentiate between threads created by Thread class and Runnable interface.**

| Aspect | Thread Class | Runnable Interface |
| ----- | ----- | ----- |
| Inheritance | Extends Thread class | Implements Runnable interface |
| Multiple Inheritance | Cannot extend another class | Can implement multiple interfaces |
| Code Reusability | Less reusable as it ties to a specific Thread subclass | More reusable, can be shared across different threads |
| Implementation | public class MyThread extends Thread { public void run() { /* code */ } } | public class MyRunnable implements Runnable { public void run() { /* code */ } } |
**(i) Describe classes and objects in Java. Describe the relationship with a suitable real-world example.**

Classes in Java are blueprints for creating objects. They define the properties (attributes) and behaviors (methods) that the objects created from the class will have. An object is an instance of a class, containing real values instead of variables.

Example:

```java
public class Car {
    // Attributes
    String color;
    String model;
    int year;

    // Constructor
    public Car(String color, String model, int year) {
        this.color = color;
        this.model = model;
        this.year = year;
    }

    // Methods
    public void displayInfo() {
        System.out.println("Car: " + model + ", Color: " + color + ", Year: " + year);
    }
}

public class Main {
    public static void main(String[] args) {
        // Creating an object of Car class
        Car car1 = new Car("Red", "Toyota", 2020);
        car1.displayInfo();
    }
}
```
In this example, `Car` is a class with attributes `color`, `model`, and `year`. The `car1` object is an instance of the `Car` class with specific values for these attributes.

**(j) Discuss the concept of layouts and their types in AWT. Differentiate between Border Layout and Flow Layout.**

Layouts in AWT (Abstract Window Toolkit) manage the size and position of components in a container. They help in organizing the graphical user interface.

| Layout Type | Description |
| ----- | ----- |
| BorderLayout | Divides the container into five regions: North, South, East, West, and Center |
| FlowLayout | Arranges components in a left-to-right flow, much like lines of text in a paragraph |
| GridLayout | Divides the container into a grid of equally sized cells |
| CardLayout | Allows switching between different panels (like cards in a stack) |
| Feature | BorderLayout | FlowLayout |
| ----- | ----- | ----- |
| Arrangement | Components are placed in five regions: North, South, East, West, Center | Components are placed in a row, wrapping to the next line when necessary |
| Resizing | Regions resize according to the container's size | Components keep their preferred size, arranged sequentially |
| Use Case | Suitable for complex layouts with defined regions | Suitable for simple, sequential arrangement of components |


## SECTION -B


**2. Attempt any three of the following: 10x3=30**

**(a) Illustrate the concept of multi-threading. Write a code in Java to create three threads having name Red, Blue and Green. Justify why should we use run() method instead of start() to launch a Thread.**



### ANSWER:   
**Concept of Multi-threading:**

Multi-threading is a programming concept where multiple threads are spawned by a process to perform different tasks concurrently. Threads are lightweight processes that share the same memory space and resources, enabling efficient CPU utilization and better performance for multi-tasking applications. Multi-threading is commonly used in applications where multiple tasks need to be performed simultaneously, such as in web servers, gaming, and real-time simulations.

**Java Code to Create Three Threads:**

```java
class ColorThread extends Thread {
    public ColorThread(String name) {
        super(name);
    }

    @Override
    public void run() {
        System.out.println("Thread " + getName() + " is running.");
    }

    public static void main(String[] args) {
        ColorThread redThread = new ColorThread("Red");
        ColorThread blueThread = new ColorThread("Blue");
        ColorThread greenThread = new ColorThread("Green");

        // Starting the threads
        redThread.start();
        blueThread.start();
        greenThread.start();
    }
}
```
**Why use start() method instead of run() method to launch a Thread:**

- `**start()**` ** method:**
    - When you call the `start()`  method, a new thread is created and the `run()`  method is executed in this new thread.
    - This allows multiple threads to run concurrently and take advantage of multi-core processors.
    - The `start()`  method ensures that the thread scheduling mechanism of the Java Virtual Machine (JVM) is used to manage the threads.
- `**run()**` ** method:**
    - When you call the `run()`  method directly, no new thread is created. Instead, the `run()`  method is executed in the current thread.
    - This means that the code will be executed sequentially within the same thread that called the `run()`  method, not concurrently.
    - This defeats the purpose of multi-threading as it does not create a new thread of execution.
In summary, using the `start()` method is essential for achieving true multi-threading, where tasks are executed concurrently. Calling the `run()` method directly will not create a new thread, and thus will not leverage the benefits of multi-threading



**(b) Discuss the applications of XML. Also compare XSD and DTD.**



### ANSWER:   
**Applications of XML (Extensible Markup Language):**

- **Data Storage:** XML is often used for storing data in a structured format.
- **Data Exchange:** It facilitates the exchange of data between different systems and platforms.
- **Configuration Files:** XML files are commonly used for configuration settings in various software applications.
- **Web Services:** XML is used in SOAP-based web services for message formatting.
**Comparison between XSD (XML Schema Definition) and DTD (Document Type Definition):**

**Table**

| Feature | XSD | DTD |
| ----- | ----- | ----- |
| Language | Written in XML | Not written in XML, has its own syntax |
| Data Types | Supports data types | Does not support data types |
| Namespaces | Supports namespaces | Does not support namespaces |
| Extensibility | More extensible due to being written in XML | Less extensible |
| Validation | Provides stronger validation capabilities | Offers basic validation |
XML is widely used due to its flexibility, extensibility, and platform-independent nature. XSD provides more robust validation and structure definition compared to DTD, making it the preferred choice for defining XML schemas.



**(c) Describe <form> tag and its attributes. Also differentiate GET and POST methods.**



### ANSWER:   
**Description of **`<form>`** Tag:** The `<form>` tag in HTML is used to create an HTML form for user input. It can contain form elements like text fields, checkboxes, radio-buttons, submit buttons, etc.

**Attributes of **`<form>`** Tag:**

- **action:** Specifies where to send the form-data when a form is submitted.
- **method:** Defines the HTTP method (GET or POST) to be used when submitting the form.
- **enctype:** Specifies how the form-data should be encoded when submitting it to the server (used only with POST).
**GET vs POST Methods:**

**Table**

| Feature | GET | POST |
| ----- | ----- | ----- |
| Data Visibility | Data is visible in the URL | Data is not displayed in the URL |
| Data Limit | Limited amount of data can be sent | Large amounts of data can be sent |
| Security | Less secure, data exposed in URL | More secure, data not exposed |
| Idempotent | Yes (repeating safe) | No (repeating may cause changes) |
| Use Case | Retrieving data | Sending data that affects server state |
The GET method is suitable for non-sensitive data and can be bookmarked, while POST is used for sensitive data and when a significant amount of data needs to be transferred.



**(d) Illustrate Java Beans and their properties in detail.**



### ANSWER:   
**Java Beans:** Java Beans are reusable software components for Java that can be manipulated visually in a builder tool. They are classes that encapsulate many objects into a single object (the bean).

**Properties of Java Beans:**

- **Properties:** A Java Bean property is a named attribute that can be accessed by the user of the object. There are two types of properties: simple and indexed.
- **Methods:** Java Beans have getter and setter methods for accessing properties.
- **Events:** Beans use event handling models to communicate with other components.
- **Introspection:** This allows analysis to understand the capabilities of a bean.
- **Customization:** The appearance and behavior can be customized.
- **Persistence:** Beans can be serialized, allowing their features to be saved and restored later.
Here’s an example of a simple Java Bean with one property called `text`:

**Java**

```java
public class TextBean implements java.io.Serializable {
    private String text;

    public TextBean() {
        text = "default";
    }

    public String getText() {
        return text;
    }

    public void setText(String newText) {
        text = newText;
    }
}
```


This bean has a property `text` with its getter and setter methods, following the naming convention that allows introspection to work correctly



**(e) Explain the implicit and explicit objects in JSP. Describe request, response and session objects in detail.**



### ANSWER:   
**Implicit Objects in JSP:** Implicit objects in JSP are pre-defined variables that provide access to the Java servlet environment. They are created automatically and do not require explicit declaration.

**Explicit Objects in JSP:** Explicit objects are those that you define yourself. They can be JavaBeans, database connections, or any other objects that you instantiate using JSP tags or scriptlets.

**Detailed Description of Request, Response, and Session Objects:**

- **Request Object:** Represents the client’s request to the server. It can be used to retrieve form data, query strings, and HTTP headers.
    - **Methods:** `getParameter()` , `getAttribute()` , `getHeader()` , etc.
- **Response Object:** Represents the server’s response to the client. It is used to send content or redirect the client to another resource.
    - **Methods:** `setContentType()` , `addCookie()` , `sendRedirect()` , etc.
- **Session Object:** Used to track client sessions between multiple requests. It can store user data for the duration of a session.
    - **Methods:** `getAttribute()` , `setAttribute()` , `invalidate()` , etc.
These objects are fundamental for handling HTTP requests and responses in JSP and managing session data.



## **SECTION C**
**3. Attempt any one part of the following: 10x1=10**

**(a) Outline the differences between Encapsulation and Abstraction. Illustrate with suitable example.**



### ANSWER:   
**Differences between Encapsulation and Abstraction:**

**Table**

| Feature | Encapsulation | Abstraction |
| ----- | ----- | ----- |
| Concept | Hiding the internal state and requiring all interaction to be performed through an object’s methods | Hiding complex implementation details and showing only the necessary features of an object |
| Purpose | To control the access to the internal state of the object | To reduce complexity and increase efficiency |
| Implementation | <p></p><p>Using private variables and public methods</p> | Using abstract classes and interfaces |
**Example:**

Consider a car as an example:

- **Encapsulation:** The internal mechanics of the car (engine, gearbox, etc.) are hidden from the driver. The driver interacts with the car through interfaces like the steering wheel, pedals, and gear stick.
**Java**

```java
public class Car {
    private String engineStatus;

    public void startEngine() {
        engineStatus = "Running";
    }

    public void stopEngine() {
        engineStatus = "Stopped";
    }
}
```


- **Abstraction:** The concept of a car itself is an abstraction. You know you can drive it, but you don’t need to know how the engine works to operate it.
**Java**



```java
public abstract class Vehicle {
    public abstract void start();
    public abstract void stop();
}

public class Car extends Vehicle {
    @Override
    public void start() {
        // Start the car
    }

    @Override
    public void stop() {
        // Stop the car
    }
}
```


In this example, `Car` class encapsulates the `engineStatus` field, while `Vehicle` abstracts the concept of a vehicle with start and stop functionalities.



**(b) Describe method overriding in Java. Compare method overriding and method overloading with suitable example.**





### ANSWER:   


**Method Overriding in Java:** Method overriding occurs when a subclass provides a specific implementation for a method that is already provided by its parent class or interface. The method must have the same name, return type, and parameters.

**Example of Method Overriding:**

**Java**

```java
class Animal {
    public void sound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    @Override
    public void sound() {
        System.out.println("Dog barks");
    }
}
```


**Comparison between Method Overriding and Method Overloading:**

**Table**

| Feature | Method Overriding | <p></p><p></p><p>Method Overloading</p> |
| ----- | ----- | ----- |
| Purpose | To provide a specific implementation in the subclass | To provide multiple methods with the same name but different parameters |
| Parameters | Must have the same parameters | Must have different parameters |
| Return Type | Must have the same return type | Can have different return types |
| Scope | Occurs between superclass and deruived class | Occurs within the same class |
**Example of Method Overloading:**

**Java**

```java
class MathOperation {
    public int multiply(int a, int b) {
        return a * b;
    }

    // Overloaded method with different parameters
    public int multiply(int a, int b, int c) {
        return a * b * c;
    }
}
```




In the example, `Dog` overrides the `sound()` method from `Animal`, while `MathOperation` overloads the `multiply()` method to handle different numbers of arguments.



**4. Attempt any one part of the following:** 

**(a) Describe frames in HTML. Write markup to create a web page that contains three vertical columns, having background color as red, blue, green respectively.** 



### ANSWER:   
**Frames in HTML:**

Frames in HTML are used to divide the browser window into multiple sections, each of which can load a separate HTML document. This allows for the simultaneous display of multiple web pages within a single browser window. Frames are defined using the `<frameset>` element, and individual frames are created using the `<frame>` element. Frames can be laid out in various configurations, such as rows or columns.

**Note:** The use of frames is generally discouraged in modern web design due to usability and accessibility issues, and they have been deprecated in HTML5. Instead, CSS and JavaScript are recommended for creating layouts. However, here is an example using the traditional frameset approach.

**HTML Markup to Create a Web Page with Three Vertical Columns:**

```html
<!DOCTYPE html>

<html>
<head>
    <title>Three Vertical Columns</title>
</head>

    <frameset cols="33%,33%,34%">
        <frame src="red.html" name="redFrame" />
        <frame src="blue.html" name="blueFrame" />
        <frame src="green.html" name="greenFrame" />
    </frameset>

</html>
```
Create three separate HTML files (`red.html`, `blue.html`, and `green.html`) with the following content:

**red.html:**

```html
htmlCopy code<!DOCTYPE html>
<html>
<head>
    <title>Red Frame</title>
    <style>
        body {
            background-color: red;
            margin: 0;
            height: 100%;
        }
    </style>
</head>
<body>
</body>
</html>
```
**blue.html:**

```html
<!DOCTYPE html>
<html>
<head>
    <title>Blue Frame</title>
    <style>
        body {
            background-color: blue;
            margin: 0;
            height: 100%;
        }
    </style>
</head>
<body>
</body>
</html>
```
**green.html:**

```html
<!DOCTYPE html>
<html>
<head>
    <title>Green Frame</title>
    <style>
        body {
            background-color: green;
            margin: 0;
                        height: 100%;
        }
    </style>
</head>
<body>
</body>
</html>
```
**Explanation:**

1. **Main HTML File (**`**index.html**` **):**
    - The `<frameset>`  element is used to divide the window into three vertical columns using the `cols`  attribute, which specifies the width of each column as a percentage.
    - Each `<frame>`  element within the `<frameset>`  specifies a separate HTML file to be loaded into the frame.
2. **Individual Frame HTML Files (**`**red.html**` **, **`**blue.html**` **, **`**green.html**` **):**
    - Each of these files sets the background color of the `body`  element to red, blue, and green respectively, creating the desired colored columns.


**(b) Design a self-describing XML DTD for storing email data.**



### ANSWER:   
self-describing XML DTD for storing email data:

**XML**

```xml
<!DOCTYPE email [
<!ELEMENT email (sender, recipient, subject, body)>
<!ELEMENT sender (#PCDATA)>
<!ELEMENT recipient (#PCDATA)>
<!ELEMENT subject (#PCDATA)>
<!ELEMENT body (#PCDATA)>
]>
```
This DTD defines an `email` element that contains `sender`, `recipient`, `subject`, and `body` elements. Each of these elements can contain parsed character data (`#PCDATA`), which means they can include text.

**5. Attempt any one part of the following:**

 **(a) Discuss about Math and Date Objects in JavaScript. Write a program in JavaScript to display digital clock showing HH:MM:SS.**



### ANSWER:   
 **Math Object in JavaScript:**

The Math object in JavaScript is a built-in object that has properties and methods for mathematical constants and functions. It's not a function object, and all its properties and methods are static. This means you don't need to create an instance of the Math object, and you can use its properties and methods directly.

**Common Methods of Math Object:**

- `Math.abs(x)` : Returns the absolute value of a number.
- `Math.ceil(x)` : Rounds a number up to the nearest integer.
- `Math.floor(x)` : Rounds a number down to the nearest integer.
- `Math.round(x)` : Rounds a number to the nearest integer.
- `Math.max(x, y, z, ..., n)` : Returns the largest of zero or more numbers.
- `Math.min(x, y, z, ..., n)` : Returns the smallest of zero or more numbers.
- `Math.random()` : Returns a pseudo-random number between 0 and 1.
- `Math.pow(x, y)` : Returns `x`  to the power of `y` .
- `Math.sqrt(x)` : Returns the square root of `x` .
**Date Object in JavaScript:**

The Date object in JavaScript is used to work with dates and times. It provides methods for getting and setting the year, month, day, hour, minute, second, and millisecond. You can create a Date object using the `new Date()` constructor.

**Common Methods of Date Object:**

- `getDate()` : Returns the day of the month (1-31).
- `getDay()` : Returns the day of the week (0-6).
- `getFullYear()` : Returns the year (4 digits).
- `getHours()` : Returns the hour (0-23).
- `getMinutes()` : Returns the minutes (0-59).
- `getSeconds()` : Returns the seconds (0-59).
- `getMilliseconds()` : Returns the milliseconds (0-999).
- `getTime()` : Returns the number of milliseconds since January 1, 1970.
- `setDate()` : Sets the day of the month.
- `setFullYear()` : Sets the year.
**JavaScript Program to Display Digital Clock (HH:MM**

**):**

```html
<!DOCTYPE html>
<html>
<head>
    <title>Digital Clock</title>
</head>
<body>
    <div id="clock"></div>

    <script>
        function updateClock() {
            const now = new Date();
            let hours = now.getHours();
            let minutes = now.getMinutes();
            let seconds = now.getSeconds();

            // Add leading zeros to hours, minutes, and seconds if they are less than 10
            hours = hours < 10 ? '0' + hours : hours;
            minutes = minutes < 10 ? '0' + minutes : minutes;
            seconds = seconds < 10 ? '0' + seconds : seconds;

            const timeString = hours + ':' + minutes + ':' + seconds;
            document.getElementById('clock').innerText = timeString;
        }

        // Update the clock every second
        setInterval(updateClock, 1000);

        // Initialize the clock when the page loads
        updateClock();
    </script>
</body>
</html>
```
**Explanation:**

1. **HTML Structure**: The `div`  element with the `id="clock"`  is where the current time will be displayed.
2. **JavaScript Function**:
    - The `updateClock`  function gets the current date and time using the `Date`  object.
    - It extracts the hours, minutes, and seconds from the current time.
    - It formats hours, minutes, and seconds to always display two digits (by adding a leading zero if necessary).
    - It updates the text content of the `div`  with `id="clock"`  to show the formatted time.
3. **setInterval Function**: The `setInterval`  function calls `updateClock`  every 1000 milliseconds (1 second) to update the clock.
4. **Initial Call**: The `updateClock`  function is called once when the page loads to initialize the clock immediately.
 

**(b) Discuss about Java Socket programming. Write a program in Java to create client and Server using Socket, Server Socket class.**



### ANSWER:   
**Java Socket Programming:** Java Socket programming is used for communication between applications running on different JREs. Java provides two classes, `Socket` and `ServerSocket`, which implement client-side and server-side communication respectively.

**Server Program using ServerSocket:**

**Java**

```java
import java.io.*;
import java.net.*;

public class Server {
    public static void main(String[] args) {
        try {
            ServerSocket serverSocket = new ServerSocket(6666);
            System.out.println("Server started, waiting for a client...");
            
            Socket socket = serverSocket.accept(); //establishes connection
            System.out.println("Client connected.");
            
            DataInputStream dis = new DataInputStream(socket.getInputStream());
            String message = (String)dis.readUTF();
            System.out.println("Message from client: " + message);
            
            serverSocket.close();
        } catch(Exception e) {
            System.out.println(e);
        }
    }
}
```


**Client Program using Socket:**

**Java**

```java
import java.io.*;
import java.net.*;

public class Client {
    public static void main(String[] args) {
        try {
            Socket socket = new Socket("localhost", 6666);
            
            DataOutputStream dout = new DataOutputStream(socket.getOutputStream());
            dout.writeUTF("Hello Server");
            dout.flush();
            dout.close();
            
            socket.close();
        } catch(Exception e) {
            System.out.println(e);
        }
    }
}
```


**6. Attempt any one part of the following:**

 **(a) Describe about JDBC drivers and different types of JDBC drivers. Write a java code to fetch and print the data from EMP_Table. Table name: EMPLOYEE Column Name: ID, EMP_NAME, EMP_DEPT, EMP_SAL** 



### ANSWER:   
**JDBC Drivers:** JDBC (Java Database Connectivity) drivers are used to connect Java applications to a database. There are four types of JDBC drivers:

1. **Type 1: JDBC-ODBC Bridge Driver** - It converts JDBC method calls into ODBC function calls. It is not recommended for production use.
2. **Type 2: Native-API Driver** - This driver uses client-side libraries of the database. It is faster than Type 1 but not portable.
3. **Type 3: Network Protocol Driver** - This driver sends the JDBC method call to a server-side component, which then sends the call to the database. It is fully written in Java.
4. **Type 4: Thin Driver** - This driver converts JDBC calls directly into the network protocol used by DBMSs directly; thus, it is very portable and fast.
**Java Code to Fetch Data from EMPLOYEE Table:**

**Java**

```java
import java.sql.*;

public class EmployeeData {
    public static void main(String[] args) {
        try {
            // Load the JDBC driver
            Class.forName("com.mysql.jdbc.Driver");
            
            // Establish a connection
            Connection con = DriverManager.getConnection(
                "jdbc:mysql://localhost:3306/yourdatabase", "username", "password");
            
            // Create a statement
            
            Statement stmt = con.createStatement();
            
            // Execute the query
            ResultSet rs = stmt.executeQuery("SELECT * FROM EMPLOYEE");
            
            // Process the result set
            while(rs.next()) {
                System.out.println("ID: " + rs.getInt("ID") + ", Name: " + rs.getString("EMP_NAME") +
                                   ", Department: " + rs.getString("EMP_DEPT") + ", Salary: " + rs.getFloat("EMP_SAL"));
            }
            
            // Close the connection
            con.close();
        } catch(Exception e) {
            System.out.println(e);
        }
    }
}
```




**(b) Compare following:**

 **1) Stateful Session bean and Stateless Session bean** 

** 2) Statement and Prepared Statement**



### ANSWER:   
**1) Stateful Session Bean vs Stateless Session Bean:**

- **Stateful Session Bean:**
    - Maintains state across method calls and transactions.
    - Each client has its own instance of a stateful bean.
    - Suitable for conversational state with a particular client.
- **Stateless Session Bean:**
    - Does not maintain any state between method calls.
    - Instances can be pooled and reused by any client.
    - More scalable due to the pooling capability.
**2) Statement vs PreparedStatement:**

- **Statement:**
    - Used for executing a simple SQL query without parameters.
    - Each time it is executed, the SQL query is compiled.
    - Can be less efficient if executing the same SQL query multiple times.
- **PreparedStatement:**
    - Used for executing precompiled SQL queries with or without parameters.
    - The SQL query is compiled only once, which makes it more efficient for repeated execution.
    - Helps prevent SQL injection attacks due to its parameterized query feature.


**7. Attempt any one part of the following:** 

**(a) Describe Java Servlets. Write Index.html to input some details (name, age, Message) from user. Also write a Servlet to fetch and display the data upon the submission of request.** 



### ANSWER:   
**Java Servlets:** Java Servlets are server-side programs that handle client requests and return a response. They run in a servlet container, can process incoming requests, produce responses, and can maintain state across multiple requests.

**Index.html (HTML Form):**

**HTML**

```html
<!DOCTYPE html>
<html>
<head>
<title>User Details Form</title>
</head>
<body>
<form action="UserDataServlet" method="post">
    Name: <input type="text" name="name"><br>
    Age: <input type="text" name="age"><br>
    Message: <textarea name="message"></textarea><br>
    <input type="submit" value="Submit">
</form>
</body>
</html>
```


**UserDataServlet (Java Servlet):**

**Java**

```java
import java.io.*;
import javax.servlet.*;
import javax.servlet.http.*;

public class UserDataServlet extends HttpServlet {
    protected void doPost(HttpServletRequest request, HttpServletResponse response)
    throws ServletException, IOException {
        response.setContentType("text/html");
        PrintWriter out = response.getWriter();
        
        String name = request.getParameter("name");
        String age = request.getParameter("age");
        String message = request.getParameter("message");
        
        out.println("<html><body>");
        out.println("<h1>User Details Submitted:</h1>");
        out.println("<p>Name: " + name + "</p>");
        out.println("<p>Age: " + age + "</p>");
        out.println("<p>Message: " + message + "</p>");
        out.println("</body></html>");
        
        out.close();
    }
}
```


**(b) Compare Servlet and JSP. Justify why Servlets perform faster in comparison to JSP. Explain the Life cycle of JSP with suitable diagram.**



### ANSWER:   
**Servlet vs JSP:**

- **Servlet:**
    - Java program that runs on the server-side.
    - More control over the content and can manage complex tasks.
    - Faster execution after the first request because it’s compiled to bytecode.
- **JSP (JavaServer Pages):**
    - HTML-like pages embedded with Java code snippets.
    - Easier to write and maintain for web page content.
    - Initially slower because it compiles into a Servlet on the first request.
**Performance Justification:** Servlets are generally faster than JSP because:

- Servlet code is written in Java and compiled to bytecode, which runs directly on the JVM.
- JSP files are first translated into Servlets by the server during runtime, which adds an initial overhead.
**Life Cycle of JSP:**

1. **Translation:** The JSP file is translated into a Servlet by the web container.
2. **Compilation:** The generated Servlet is compiled into bytecode.
3. **Initialization:** The `init`  method is called to initialize the Servlet instance.
4. **Execution:** The `service`  method is called to process requests and generate responses.
5. **Cleanup:** The `destroy`  method is called before the Servlet instance is removed.


