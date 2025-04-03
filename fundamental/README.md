# Fundamentals of the Web

## 1. What is the Web?

The **web** (World Wide Web, or WWW) is a system of interlinked hypertext documents and multimedia content accessed through the internet. It allows users to browse websites, interact with services, and access various resources like text, images, videos, and more.

- The web operates on a client-server model, where **clients** (such as browsers) send requests for resources and **servers** respond with those resources.

## 2. What is HTTP?
> [!NOTE]
> b4 talking about http u should learn about *protocols*. **Protocols** are some rules that a client and a server talk to each other.


**HTTP** stands for **HyperText Transfer Protocol**. It is the protocol used to transfer data over the web. HTTP defines how messages are formatted and transmitted, and how web servers and browsers should respond to various commands.

- HTTP is a **stateless** protocol, meaning that each request is independent and does not retain information about previous requests.
- HTTP requests and responses are used for client-server communication.

## 3. What is an HTTP Request?

An **HTTP request** is made by a client (usually a browser) to ask a server for a resource (such as a webpage, image, or file). It typically consists of:

- **Request Line**: Includes the HTTP method (GET, POST, etc.) and the path of the requested resource (e.g., `/index.html`).
- **Headers**: Provide additional information about the request, such as content type or the type of browser making the request.
- **Body**: (Optional) Contains data sent to the server, typically used with methods like POST for submitting forms.

### Example HTTP Request:
```http
GET /index.html HTTP/1.1
Host: www.example.com
Accept: text/html
```
### HTTP request methods

#### GET
**The GET** method is used to request data from the server. It's the most common method, typically used when you open a webpage.

##### Example:
```http
GET /home.html HTTP/1.1
Host: www.example.com
```
This request asks the server to retrieve the home.html page.

#### POST
**The POST** method is used to send data to the server, typically to create or submit data. For example, when you submit a form.

##### Example:
```http
POST /submit-form HTTP/1.1
Host: www.example.com
Content-Type: application/x-www-form-urlencoded
Content-Length: 45

name=JohnDoe&email=john@example.com
```
This sends form data to the server to create or update a resource (like submitting a contact form).

## 4. What is an HTTP Response?
An **HTTP response** is the server's reply to an HTTP request. It contains:

**Status Code:** Indicates the result of the request (e.g., `200 OK`, `404 Not Found`, `500 Internal Server Error`).

**Headers:** Provide metadata about the response (e.g., content type, content length).


**Body:** Contains the content requested, such as HTML, images, JSON, or other resources.

### Example HTTP Response:
```http
HTTP/1.1 200 OK
Content-Type: text/html; charset=UTF-8

<html>
  <body>
    <h1>Welcome to the website!</h1>
  </body>
</html>
```
## 5. What is a Web Server?
A **web server** is a system or software that hosts web content and serves it to clients. It listens for incoming HTTP requests, retrieves the requested resources, and sends back the appropriate HTTP response.

Popular web servers include:

- Apache HTTP Server

- Nginx

- Microsoft IIS

## 6. What is DNS (Domain Name System)?
**DNS** stands for Domain Name System. It is a system that translates human-readable domain names (e.g., `www.example.com`) into machine-readable IP addresses (e.g., `192.0.2.1`). When you type a domain name into a browser, DNS helps your browser locate the web server hosting the website.

## 7. What is a Browser?
**A browser** is a client-side application that allows users to view web pages and interact with web content. It sends HTTP requests to web servers and displays the HTTP responses (e.g., HTML, images, etc.) for the user to see.

Examples of popular browsers:

- Google Chrome

- Mozilla Firefox

- Safari

- Microsoft Edge

## 8. What is HTML (HyperText Markup Language)?
**HTML** is the standard markup language used to create web pages. It structures content by using elements like headings, paragraphs, images, and links. HTML defines the structure of a web page, while CSS and JavaScript define its style and behavior.

### Example HTML:
```html
    <!DOCTYPE html>
    <html>
    <head>
        <title>My Web Page</title>
    </head>
    <body>
        <h1>Welcome to my web page</h1>
        <p>This is a paragraph of text.</p>
    </body>
    </html>
```

## 9. What is CSS (Cascading Style Sheets)?
**CSS** is a style sheet language used to describe the look and formatting of a web page. It controls the appearance of HTML elements, such as their colors, fonts, layouts, and positioning.

### Example CSS:
```css
h1 {
  color: blue;
  font-size: 24px;
}

p {
  color: gray;
  font-family: Arial, sans-serif;
}
```

## 10. What is JavaScript?
**JavaScript** is a programming language used to make web pages interactive. It is primarily executed on the client side (in the browser) and allows for dynamic content, form validation, animations, and more.

### Example JavaScript:
```js
document.getElementById("demo").innerHTML = "Hello, World!";
```
## 11. Web Development Overview
**Web development** involves creating websites and web applications. It is typically divided into two parts:

- **Frontend**: The part of the web that users interact with, including HTML, CSS, and JavaScript.

- **Backend:** The server-side logic, databases, and server management that power the frontend. Technologies like PHP, Node.js, Python, Ruby, and databases like MySQL or MongoDB are commonly used for backend development.

> [!IMPORTANT]
> here we are learning **backend**.