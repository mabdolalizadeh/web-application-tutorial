# 🐍 Flask Mini Guide
## 🔍 What is Flask?
**Flask** is a lightweight web framework written in Python.
It lets you build websites, APIs, and web apps quickly using just Python code.
### Why Flask?
- Simple to use
- Great for beginners
- No need to know backend technologies right away

You write Python code, and *Flask* turns it into a working website.

## ⚙️ How to Install Flask
In your terminal or command prompt, type:
```bash
pip install Flask
```
Make sure **Python** is installed before running this.

## ▶️ How to Run a Flask App
1) Create a file (e.g., `app.py`)
2) Paste this code:
    ```python
    from flask import Flask

    app = Flask(__name__)

    @app.route("/")
    def home():
        return "Hello, Flask!"

    if __name__ == "__main__":
        app.run(debug=True)
    ```

3) Run the app:
    ```bash
    python app.py
    ```
4) Open your browser and go to:
    ```arduino
    http://localhost:5000/
    ```
You’ll see: `Hello, Flask!`

> [!WARNING]
> its just a simple app to show how it works. we can do lots of things with flask. just wait.

## 🛣️ Route – Making Webpages with Python
```python
@app.route("/about")
def about():
    return "This is the About Page"
```
- A route connects a URL (like `/about`) to a function.
- Flask runs the function when someone visits the route.

> [!NOTE]
> can u remember `path` in URL? `route` is that :)

## 🖼️ Render Template – Show HTML Pages
1) Create a file: `templates/index.html`
    ```html
    <!DOCTYPE html>
    <html>
    <body>
        <h1>Hello, {{ name }}!</h1>
    </body>
    </html>
    ```
2) Render it in your app:
    ```python
    from flask import render_template

    @app.route("/hello")
    def hello():
        return render_template("index.html", name="Student")
    ```
- `render_template()` loads HTML and fills in variables like `{{ name }}`.

## 📥 Request – Get Data from a Form
In `form.html`:
```html
<form method="POST">
  <input name="username" placeholder="Enter your name">
  <input type="submit">
</form>
```
In `app.py`:
```python
from flask import request

@app.route("/submit", methods=["GET", "POST"])
def submit():
    if request.method == "POST":
        username = request.form["username"]
        return f"Hello, {username}!"
    return render_template("form.html")
```
- `request.form["username"]` gets the value from the form input.

## 🔀 Redirect – Jump to Another Page
```python
from flask import redirect, url_for

@app.route("/login")
def login():
    return redirect(url_for("home"))
```
- **Redirect** sends the user to a different route (in this case, `/`).


## ✅ Full Example for Practice
```python
from flask import Flask, render_template, request, redirect, url_for

app = Flask(__name__)

@app.route("/")
def home():
    return "Welcome to the Homepage!"

@app.route("/form", methods=["GET", "POST"])
def form():
    if request.method == "POST":
        name = request.form["name"]
        return redirect(url_for("greet", username=name))
    return render_template("form.html")

@app.route("/greet/<username>")
def greet(username):
    return f"Hello, {username}!"

if __name__ == "__main__":
    app.run(debug=True) # debug=True turn on debug mode
```
`templates/form.html`:
```html
<form method="POST">
  <input name="name" placeholder="Your name">
  <input type="submit">
</form>
```
<br>

# Tasks
- make a simple flask app:
  - that has a template (u can download it) 
  - use redirect in it
  - use variable to render template
  - check requests
- **optional**:
  - its so good if you learn about *what is deploy?* and ***deploy*** ur app.