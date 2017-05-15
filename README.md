# FSND Interview Dry-Run

### Question 1
What is the most influential book or blog post you’ve read regarding web development?

Link to blog:http://sixrevisions.com/web-development/tips-on-how-to-code-web-designs-better/
This is my one of my favourite blog that I read when I was learning HTML and CSS. My first website was a fully responsive website that I made during my first internship as a Web developer. This Blog help me a lot during my internship.


### Question 2
Tell me about a web application you have built. Why did you choose to build it? What did you learn? What challenges did you face and how did you overcome them?

A few months back I had to submit a project in my college. I choose to build employee attendance and Tracking system because I thought it will be so much easier if attendance is marked by computer at the specific time.This project not only marked their attendance but also show locations of their mobile phones provided by the company. Such that it will be much easier to monitor employee. Attendance is started automatically by computer and based on employee location, attendance is marked.

I learn a lot during the development of this project like how to use API to get android phone location, use threading so that every android device is tracked simultaneously.I face difficulty in using threading and tracking every device simultaneously And I overcome it by reading how the thread works all over the internet. I use QThreads in my web application  

### Question 3
Write a function that takes a list of strings and returns a single string that is an HTML unordered list `(<ul>...</ul>)` of those strings. You should include a brief explanation of your code. Then, what would you have to consider if the original list was provided by user input?

```python
def unordered_list(strings):
  # opening unordered list tag
  lst = '<ul>'

  # iterate over strings
  for elem in strings:
    # append list item tag with contents of one element in strings
    lst += '<li>%s</li>' % elem

  # append closing unordered list tag
  lst += '</ul>'
  return lst

```

If the original list is supplied by user input, the function should check if the input is a list, and if the list contains strings.

### Question 4
List 2-3 attacks that web applications are vulnerable to. How do these attacks work? How can we prevent those attacks?

DDoS(Distributed Denial of Service) attacks are common to web applications. The attacker spams the web server with requests until it can no longer serve content. There is no known protection against this kind of attack, but the more robust the web server is, the more traffic it can handle before being overloaded.

A SQL Injection attack is a form of attack that comes from user input that has not been checked to see that it is valid. The objective is to fool the database system into running malicious code that will reveal sensitive information or otherwise compromise the server.To prevent this one can use you can use SQL parameters.SQL parameters are values that are added to an SQL query at execution time, in a controlled manner.

Brute force attacks are used to gain access to password-protected sections and content. Utilities like fail2ban can automatically configure a firewall to deny access from IP addresses after a certain number of failed attempts.

### Question 5
Here is some starter code for a Flask Web Application. Expand on that and include a route that simulates rolling two dice and returns the result in JSON. You should include a brief explanation of your code.

```python
from flask import Flask
app = Flask(__name__)

import json
import random


@app.route('/')
def hello_world():
  return 'Hello World!'

# Route takes one argument, the number of sides on the die
@app.route('/roll_dice/<int:sides>/json')
def roll_dice(sides):
  """Return the result of two dice with user-specified number of sides
  being rolled as a json object"""

  # Assign the result of the die roll
  die1 = random.randint(1,sides)
  die2 = random.randint(1,sides)

  # Return the results of the dice rolled as json string, sorted by key
  return json.dumps({'die1': die1, 'die2': die2}, sort_keys=True)

if __name__ == '__main__':
  app.debug = True
  app.run()

```

I've added the functionality to roll two dice and return the result as a json string. I've included the ability to pass the number of sides the dice have to the function since it wasn't specified and expands the functionality. The result of each die roll is assigned to a variable. The function returns the results of json.dumps(), sorted by key.

### Question 6
If you were to start your full-stack developer position today, what would be your goals a year from now? 

I will be eager to learn and enhance my skills as much as possible,to work on a bigger project and to be part of highly reputed company.
