# PYQP  2021-22 WEB TECHNOLOGY

1Q.

(a) **Explain Thread and how many ways to create thread in Java?** 

A thread in Java is a path of execution within a program. You can create a thread in Java mainly in two ways:

1. By extending the Thread  class.
2. By implementing the Runnable  interface.


(b) **Describe the life cycle of an Applet.** 

An applet has four main states:

1. Initialization (init)
2. Starting (start)
3. Stopping (stop)
4. Destruction (destroy)


(c) **Describe the advantages of CSS.**

 CSS (Cascading Style Sheets) offers several advantages:

- Separation of content from presentation.
- Improved page loading speed.
- Reusability across multiple pages.
- Greater styling control.


(d) **Create Object in JavaScript.** 

In JavaScript, you can create an object using object literal syntax:

**JavaScript**

```javascript
var obj = { property1: value1, property2: value2 };
```


(e) **Differentiate between HTML and XML.** 

HTML is designed for displaying data with focus on how data looks, while XML is designed for carrying data with focus on what data is.



(f) **Illustrate ResultSetMetaData Interface in JDBC.** 

`ResultSetMetaData` is an interface that allows you to get information about the types and properties of the columns in a `ResultSet`.



(g) **Outline Implicit Objects in JSP.**

 Implicit objects in JSP are pre-created objects that provide access to various objects like `request`, `response`, `session`, etc.



(h) **Identify the Dissimilarities between web server and Application server.**

 A web server handles HTTP requests and serves static content, whereas an application server provides business logic to application programs through various protocols.



(i) **Explain the Directory structure of a web application.** 

A web application directory structure typically includes:

- A `WEB-INF`  directory containing configuration files like `web.xml` .
- A `classes`  directory for compiled Java classes.
- A `lib`  directory for JAR files.


(j) **Describe the characteristics of JavaBeans.** 

JavaBeans are reusable software components that follow certain conventions:

- Properties are accessible using getters and setters.
- They are serializable.
- They have a zero-argument constructor.
### 
**2(a)** **Illustrate the features of Java Programming Language.**

** ANSWER:** 

 Java is a widely-used programming language with several key features:

- **Object-Oriented**: Everything in Java is an object which helps in making a modular approach and code reusability.
- **Platform-Independent**: Java code can run on all platforms that have the Java Virtual Machine (JVM).
- **Simple**: Java is designed to be easy to learn and use effectively.
- **Secure**: It provides a secure platform through its runtime environment and use of bytecode.
- **Architecture-Neutral**: Java’s compiler generates an architecture-neutral object file format, making the compiled code executable on many processors.
- **Portable**: Being architecture-neutral and having no implementation-dependent aspects makes Java portable.
- **Robust**: It emphasizes error checking and runtime checking.
- **Multithreaded**: Java supports multithreaded programming, which allows you to write programs that can perform many tasks simultaneously.
- **Interpreted**: Java byte code is translated on the fly to native machine instructions and is not stored anywhere.
- **High Performance**: With the use of Just-In-Time compilers, Java enables high performance.
- **Distributed**: Java is designed for the distributed environment of the internet.
- **Dynamic**: It is considered to be more dynamic than C or C++ since it is designed to adapt to an evolving environment.
These features make Java a powerful, efficient, and popular language for a wide range of programming tasks.



### 2(b) **Create a CSS rule that makes all the text 2 times larger than the base font of the system.**
** ANSWER: **

You can use the following CSS rule:

**CSS**

```css
body {
    font-size: 2em;
}
```


This sets the font size to 2 times the base font size of the system.

**Integration of CSS on a web page:** You can integrate CSS into a web page in three ways:

1. Inline - by using the `style`  attribute inside HTML elements.
2. Internal - by using a `<style>`  block in the `<head>`  section.
3. External - by linking to an external CSS file with the `<link>`  tag.
You

### 2(c) Explain the working of AJAX along with its applications. Mention a suitable example
**ANSWER:**

** **AJAX stands for Asynchronous JavaScript and XML. It is a technique for creating fast and dynamic web pages. AJAX allows web pages to be updated asynchronously by exchanging small amounts of data with the server behind the scenes. This means that it is possible to update parts of a web page, without reloading the whole page.

**Applications of AJAX:**

- Auto-completing form fields
- Refreshing the page content dynamically
- Submitting forms without page refresh
- Loading scripts on the fly
**Example:** 

A common example of AJAX is the search suggestion feature found in many search engines. As you type a query, a request is sent to the server with each keystroke, and the server returns a list of suggestions that is dynamically displayed in a dropdown below the search bar.

You

(d) Define the advantages of servlet over CGI? Explain with an example in details

Copilot

### 2(d) **Define the advantages of servlet over CGI?**
** ANSWER:**

** **Servlets have several advantages over CGI (Common Gateway Interface):

- **Performance**: Servlets execute within the web server’s process, eliminating the overhead of creating a new process for each request as in CGI.
- **Scalability**: Servlets can handle multiple requests concurrently using threads, making them more scalable than CGI scripts which require one process per request.
- **Portability**: Servlets are written in Java and are platform-independent, unlike CGI scripts which may be platform-specific.
- **Efficiency**: Servlets remain in memory between requests, reducing the time needed to handle subsequent requests.
**Example:**

 Consider a web application that requires form data processing. With CGI, each form submission would spawn a new process on the server to handle the request, which can be resource-intensive and slow. In contrast, a servlet can handle multiple form submissions concurrently using threads, leading to better performance and a more efficient use of server resources.



### 2(e) Describe how to use Beans in JSP? Explain with an example.
**ANSWER: **

JavaBeans are reusable components that can be integrated into JSP pages. You can use them to encapsulate many objects into a single object (the bean), then access them using the simpler dot notation.

**Using Beans in JSP:**

1. Define a JavaBean class.
2. Use the `<jsp:useBean>`  tag to declare the bean within your JSP page.
3. Set properties of the bean using `<jsp:setProperty>`  tag.
4. Get properties of the bean using `<jsp:getProperty>`  tag.
**Example:**

 Suppose you have a `User` bean with `name` and `email` properties.

JavaBean class:

**Java**

```java
public class User {
    private String name;
    private String email;

    // Getter for name
    public String getName() {
        return name;
    }

    // Setter for name
    public void setName(String name) {
        this.name = name;
    }

    // Getter for email
    public String getEmail() {
        return email;
    }

    // Setter for email
    public void setEmail(String email) {
        this.email = email;
    }
}
```


JSP page:

```jsp
<jsp:useBean id="user" class="com.example.User" />
<jsp:setProperty name="user" property="name" value="John Doe" />
<jsp:setProperty name="user" property="email" value="john@example.com" />

Name: <jsp:getProperty name="user" property="name" />
Email: <jsp:getProperty name="user" property="email" />
```
This code snippet creates a `User` bean, sets its `name` and `email`, and then retrieves these properties to display them on the web page.



### 3(a) Outline the differences between procedural and object-oriented programming languages
**ANSWER:**

****

| Aspect | Procedural Programming | Object-Oriented Programming |
| ----- | ----- | ----- |
| **Approach** | Linear and top-down | Divides the problem into objects and integrates data and behavior |
| **Focus** | Functions and procedures | Objects that contain both data and methods |
| **Data & Functions** | Separate; data is passed to functions | Encapsulated; objects have methods to operate on their own data |
| **Design** | Based on the concept of procedure calls | Based on the concept of objects and classes |
| **Reusability** | Limited; mainly through functions | High; through mechanisms like inheritance and polymorphism |
| **Modularity** | Achieved through functional decomposition | Achieved through the design of object classes |
| **Examples** | C, Fortran, Pascal | Java, C++, Python |


### 3(b) Illustrate Inheritance. Why multiple inheritance is not possible in java? How to implement multiple inheritance in java?
**ANSWER:**

**Inheritance** is a fundamental concept of object-oriented programming that allows a class to inherit properties and methods from another class. In Java, classes can inherit from one superclass only (single inheritance), which prevents certain issues like the Diamond Problem that can occur with multiple inheritance.

**Multiple Inheritance** is not supported in Java through classes because it can lead to ambiguity if two parent classes have methods with the same name. To avoid such complexity, Java doesn’t allow multiple inheritance through classes.

**Implementing Multiple Inheritance in Java:** Although Java doesn’t support multiple inheritance through classes, it allows a form of multiple inheritance through interfaces. A class can implement multiple interfaces, which can contain default methods since Java 8.

Example:

**Java**

```java
interface InterfaceA {
    void methodA();
}

interface InterfaceB {
    void methodB();
}

class MyClass implements InterfaceA, InterfaceB {
    public void methodA() {
        // Implementation of methodA
    }

    public void methodB() {
        // Implementation of methodB
    }
}
```


In this example, `MyClass` implements two interfaces, `InterfaceA` and `InterfaceB`, thus achieving a form of multiple inheritance.

You

### 4(a) Create an HTML code to create a web page that contains the user registration form with following details user name, user date of birth, user address, user gender, user email id, user mobile number
**ANSWER:**

****

```html
<!DOCTYPE html>
<html>
<head>
    <title>User Registration Form</title>
</head>
<body>
    <h2>User Registration Form</h2>
    <form action="/submit-form" method="post">
        <label for="username">User Name:</label><br>
        <input type="text" id="username" name="username"><br>

        <label for="dob">Date of Birth:</label><br>
        <input type="date" id="dob" name="dob"><br>

        <label for="address">Address:</label><br>
        <input type="text" id="address" name="address"><br>

        <label for="gender">Gender:</label><br>
        <input type="radio" id="male" name="gender" value="male">
        <label for="male">Male</label><br>
        <input type="radio" id="female" name="gender" value="female">
        <label for="female">Female</label><br>

        <label for="email">Email ID:</label><br>
        <input type="email" id="email" name="email"><br>

        <label for="mobile">Mobile Number:</label><br>
        <input type="tel" id="mobile" name="mobile"><br>

        <input type="submit" value="Register">
    </form> 
</body>
</html>
```




### 4(b) Design a XML DTD for self describing weather report having following details: Date, location, temperature range (Location describes city, state and its country. Country code is unique and not left blank. Temperature range describes high and low temp. in Fahrenheit or Celsius) 
**ANSWER:**

**XML**

```xml
<!DOCTYPE weatherReport [
<!ELEMENT weatherReport (date, location, temperatureRange)>
<!ELEMENT date (#PCDATA)>
<!ELEMENT location (city, state, country)>
<!ELEMENT city (#PCDATA)>
<!ELEMENT state (#PCDATA)>
<!ELEMENT country (countryName, countryCode)>
<!ELEMENT countryName (#PCDATA)>
<!ELEMENT countryCode (#PCDATA)>
<!ATTLIST countryCode code CDATA #REQUIRED>
<!ELEMENT temperatureRange (high, low)>
<!ELEMENT high (#PCDATA)>
<!ELEMENT low (#PCDATA)>
<!ATTLIST temperatureRange unit (Fahrenheit|Celsius) "Celsius">
]>
<weatherReport>
    <date>2024-06-18</date>
    <location>
        <city>Deoria</city>
        <state>Uttar Pradesh</state>
        <country>
            <countryName>India</countryName>
            <countryCode code="IN"></countryCode>
        </country>
    </location>
    <temperatureRange unit="Celsius">
        <high>35</high>
        <low>22</low>
    </temperatureRange>
</weatherReport>
```


This DTD defines the structure for a weather report XML document that includes date, location (with city, state, and country details), and temperature range (with high and low temperatures). The `countryCode` attribute is required and cannot be left blank.



### 5(a) Design a JavaScript program to display the current day and time in the following format. Today is : Monday. Current time is : 11 AM : 50 : 58
ANSWER:

```
<!DOCTYPE html>
<html>
<head>
    <title>Current Day and Time</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
        }
    </style>
</head>
<body>
    <h1>Today is: <span id="day"></span></h1>
    <h2>Current time is: <span id="time"></span></h2>

    <script>
        function updateTime() {
            const days = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"];
            const now = new Date();

            const day = days[now.getDay()];
            const hours24 = now.getHours();
            const hours12 = hours24 % 12 || 12;
            const minutes = now.getMinutes().toString().padStart(2, '0');
            const seconds = now.getSeconds().toString().padStart(2, '0');
            const ampm = hours24 >= 12 ? 'PM' : 'AM';

            document.getElementById('day').textContent = day;
            document.getElementById('time').textContent = `${hours12} ${ampm} : ${minutes} : ${seconds}`;
        }

        setInterval(updateTime, 1000);
        updateTime();
    </script>
</body>
</html>
```


### 5(b) Create a Java program to find out the IP address of your machine
**ANSWER:**

**Java**

```java
import java.net.InetAddress;

public class IPAddressFinder {
    public static void main(String[] args) {
        try {
            InetAddress ip = InetAddress.getLocalHost();
            System.out.println("Your IP address is: " + ip.getHostAddress());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```


This program uses the `InetAddress` class from the `java.net` package to get the local host’s IP address and prints it to the console. Just run this program in your Java environment, and it will display your machine’s IP address.



### 6(a) Define JDBC. Explain the Drivers used in JDBC. Create a JDBC Program for Update and display the record of employees using prepared statement.
**ANSWER:**

**JDBC (Java Database Connectivity)** is an API in Java that allows you to connect to a database, execute queries and update statements, and retrieve results. It provides methods for querying and updating data in a database, and is oriented towards relational databases.

The four types of JDBC drivers are:

1. **Type 1**: JDBC-ODBC bridge driver
2. **Type 2**: Native-API/partly Java driver
3. **Type 3**: Network Protocol/all-Java driver
4. **Type 4**: Thin driver/pure Java driver
Here’s a simplified JDBC program using a prepared statement to update and display employee records:

```java
import java.sql.*;

public class EmployeeJDBC {
    public static void main(String[] args) {
        String url = "jdbc:mysql://localhost:3306/yourDatabase";
        String user = "yourUsername";
        String password = "yourPassword";

        try {
            Connection conn = DriverManager.getConnection(url, user, password);
            PreparedStatement pstmt = conn.prepareStatement("UPDATE employees SET salary = ? WHERE id = ?");
            pstmt.setDouble(1, 50000); // Set salary
            pstmt.setInt(2, 1); // Set employee ID
            pstmt.executeUpdate();

            pstmt = conn.prepareStatement("SELECT * FROM employees");
            ResultSet rs = pstmt.executeQuery();
            while (rs.next()) {
                System.out.println("ID: " + rs.getInt("id") + ", Name: " + rs.getString("name") + ", Salary: " + rs.getDouble("salary"));
            }
        } catch (SQLException e) {
            e.printStackTrace();
        }
    }
}
```
Replace `yourDatabase`, `yourUsername`, and `yourPassword` with your actual database details. This program updates the salary of an employee with ID 1 and then retrieves all employee records to display them.



### 6(b) Illustrate Java Bean. Explain characteristics of java Bean. Give example.
**ANSWER:**

**Java Beans** are reusable software components for Java that can be manipulated visually in a builder tool. They are classes that encapsulate many objects into a single object (the bean).

Characteristics of Java Beans include:

1. **Introspection**: Allows a builder tool to analyze how a bean works.
2. **Customization**: Can be customized using property editors.
3. **Events**: Can send and receive events.
4. **Properties**: Can have properties that can be read and written.
5. **Persistence**: The state of a bean can be saved and restored.
Here’s an example of a simple Java Bean:

**Java**

```java
public class EmployeeBean {
    private String name;
    private int age;

    public EmployeeBean() { }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }
}
```
This `EmployeeBean` has two properties: `name` and `age`, with getters and setters for each, following the Java Bean naming conventions.

### 
### 7(a)  Illustrate why the session is required in web applications. Mention all the session tracking techniques in servlet with their pros and cons. Also give example of each
**ANSWER:**

Sessions are required in web applications to maintain state across multiple requests from the same user. Since HTTP is stateless, sessions help to recognize users across different requests.

Session tracking techniques in servlets include:

1. **Cookies**:
    - Pros: Simple to use; persistent data storage.
    - Cons: Client-side; can be disabled; limited storage.
    - Example: `response.addCookie(new Cookie("user", "John Doe"));` 
2. **URL Rewriting**:
    - Pros: Works if cookies are disabled.
    - Cons: Can be cumbersome; less secure as data is exposed in URL.
    - Example: `response.encodeURL("http://www.example.com");` 
3. **Hidden Form Fields**:
    - Pros: Useful for sending data along with form submissions.
    - Cons: Only works with form submission; data exposure.
    - Example: `<input type="hidden" name="sessionID" value="12345">` 
4. **HTTP Session**:
    - Pros: Server-side; not dependent on client’s browser settings.
    - Cons: Can be lost if the user closes the browser.
    - Example: `HttpSession session = request.getSession(); session.setAttribute("user", "John Doe");` 
Each technique has its use cases depending on the application’s requirements and the desired level of persistence and security.



### 7(b) Describe Servlet. Explain types of Servlet. Give an example of HttpServlet. Write steps to execute the servlet
**ANSWER:** 

**Servlet** is a Java programming language class used to extend the capabilities of servers that host applications accessed by means of a request-response programming model.

Types of Servlet include:

1. **Generic Servlet**: Extends the `javax.servlet.GenericServlet`  class and defines a generic, protocol-independent servlet.
2. **HttpServlet**: Extends the `javax.servlet.http.HttpServlet`  class and is designed for HTTP-specific services.
Here’s an example of an `HttpServlet`:

```java
import javax.servlet.http.*;
import java.io.*;

public class HelloServlet extends HttpServlet {
    protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
        response.setContentType("text/html");
        PrintWriter out = response.getWriter();
        out.println("<h1>Hello, World!</h1>");
    }
}
```
To execute this servlet:

1. Write the servlet code in a `.java`  file.
2. Compile the servlet code and place the `.class`  file in your server’s classpath.
3. Configure the servlet in your web application’s `web.xml`  file or use annotations in the servlet code for configuration.
4. Start your web server (e.g., Apache Tomcat).
5. Access the servlet via a browser or HTTP client using the configured URL mapping.


