# Learn Flask
## Introduction to Flask<a name="introduction"></a>
#### TOPICS
* [Introduction to Flask](#introduction)
* [Jinja2 Templates and Forms](#jinja2)
* [Databases in Flask](#databases)
* [Accounts and Authentication](#authentication)
* [Deploying an Application with Heroku](#heroku)
### Python Flask Framework
Flask is a popular Python framework for developing web applications. It comes with minimal built-in functionalities and requirements, making it simple to get started and flexible to use. The developer has the liberty to customize most aspects of the app, including database integration, accounts and authentication, and more.
### Creating Flask App Object
The Python `flask` module contains all the classes and functions needed for building a Flask app. The `Flask` class can be imported to create the main application object. It takes the name of the app as an argument.
```python
# Import Flask class
from flask import Flask
 
 
# Create Flask object
app = Flask(__name__)
```
### Running Flask App
A Flask app can be run by exporting the `FLASK_APP` environment variable and running `flask run` in the terminal.
```
$ export FLASK_APP=app.py
$ flask run
```
### Creating a Route
Routes in a Flask app can be created by defining a view function and associating a URL with it using the `route()` decorator. Routes specify how the Flask app handles requests it receives, such as what to display on the webpage at a certain URL.
```python
@app.route('/')
def hello_world():
    return 'Hello, World!'
 
# Output: The text `Hello, World!` is displayed at the URL path '/'
```
### Returning HTML From Route
In a Flask app, HTML can be returned from a view function to be rendered on a webpage. The HTML can be returned as a string.
```python
@app.route('/')
def hello_world():
    return '<h1>Hello, World!</h1>'
 
# Output: The text `Hello, World!` is displayed as a level 1 heading at the URL path '/'
```
### Variable Rules
Variable rules allow a Flask app to respond to dynamic URLs. Variable sections of a URL can be indicated by angular brackets and an optional converter: `<converter:variable_name>`. These variable parts will then be passed to the view function as arguments.
```python
# Responds to `/page/1`, `/page/20`, etc.
@app.route('/page/<int:pg_num>')
def content(pg_num):
    return f'<h1>Displaying results for page {pg_num}</h1>'
```
## Jinja2 Templates and Forms <a name="jinja2"></a>
### Flask Templates
Flask uses templates to expand the functionality of a web application while maintaining a simple and organized file structure. Templates are enabled using the Jinja2 template engine and allow data to be shared and processed before being turned in to content and sent back to the client.
### render_template Function
The `render_template()` function renders HTML files for display in the web browser using the Jinja2 template engine. Its sole positional argument is the name of the template to be rendered. Keyword arguments can be added to support application variables within the template.
```python
@app.route('/')
def index():
    return render_template("index.html")
```
where `render_template` processes template files in the “templates” directory. The “templates” directory located inside the running application directory.\
├── app_dir │ ├── templates │ │ ├── my_template.html │ ├── app.py
### Template Variables
Template variables are representations of application data that are used inside templates. Created using keyword arguments in `render_template`, template variables are substituted into a template when using expression delimiters `{{ }}`

Used in Jinja templates, expression delimiters `{{ }}` surround expressions such as variables to be identified by the template engine.
```python
return render_template('my_template.html', template_var1=flask_var1, template_var2=flask_var2)
 
## The template variables are substituted into "my_template.html" using the following format
## {{ template_var1 }} and {{ template_var2 }}
```
### Template Variable Filters
### Template if Statements
### Template for Loops
### Template Inheritance
### Flask Web Forms
### request Object
### url_for Function
### FlaskForm Class
### WTForm Fields
### Form Validation
### redirect() Function
