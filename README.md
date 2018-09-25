# BlackHack: Creating Your Own Web Application

BlackHack Tutorial on Web Application Development using Flask!
___
## Installing Requirements

#### Getting a Terminal
You are going to need a terminal to use during this tutorial for running your web app. If you are using mac or linux you should already have a terminal installed on your computer. If running Windows I would recommend either [Git Bash](https://git-scm.com/downloads) or installing [Ubuntu for Windows](https://tutorials.ubuntu.com/tutorial/tutorial-ubuntu-on-windows#0).

#### Installing Python
To check if you have python you can run the following command in your terminal:
```shell
python --version
```
If you don't have Python installed you can install it using instructions [here](https://realpython.com/installing-python/).

#### Installing Pip
The next thing you are going to want to have is pip installed. This is pythons package manager and is going to allow us to install the different packages we will need.
To check if you have pip run the following command in your terminal:
```shell
pip --version
 ```
 If it's not installed you can follow the instruction [here](https://pip.pypa.io/en/stable/installing/).

 #### Installing Virtualenv
 The last thing we want to install is virtualenv. Virtualenv allows you to install python packages in isolated environments versus through your whole system.
 To check if you have virtualenv run the following command in your terminal:
 ```shell
virtualenv --version
 ```
 If it's not installed you can follow the instructions [here](https://virtualenv.pypa.io/en/stable/installation/).

___

## Base Template Code

```
<!-- base.html -->

<!DOCTYPE html>
<html lang="en">
  <head>
    <title>{% block title %}{% endblock %}</title>
    <!-- Bootstrap core CSS -->
    <link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" rel="stylesheet">
    <!-- Custom styles for this template -->
    <link href="https://getbootstrap.com/examples/jumbotron-narrow/jumbotron-narrow.css" rel="stylesheet">
  </head>
  <body>
    <div class="container">
      <div class="header clearfix">
        <nav>
          <ul class="nav nav-pills pull-right">
            <li role="presentation"><a href="/">Home</a></li>
            <li role="presentation"><a href="/about">About</a></li>
          </ul>
        </nav>
      </div>
      {% block body %}
      {% endblock %}
      <footer class="footer">
        <p>© 2018 Your Name Here</p>
      </footer>
    </div> <!-- /container -->
  </body>
</html>
```

```
<!-- index.html-->

{% extends "base.html" %}
{% block title %}Home{% endblock %}
{% block body %}
<div class="jumbotron">
  <h1>Flask Is Awesome</h1>
  <p class="lead">Replace me!</p>
</div>
{% endblock %}
```

___

## Documentation

If you want to read more about flask and some of the stuff we talked about here are some links to the documentation.
* [Python](https://docs.python.org/3/)
* [Virtualenv](https://virtualenv.pypa.io/en/stable/)
* [Flask](http://flask.pocoo.org/docs/1.0/)
