# PROJECT TITLE: Express Mail
#### Video Demo:  < https://youtu.be/FYNzyv_XARE>
#### Description:


# CS50 Final Project - Express Mail

The project is an email application where users can compose mails, send, view and also receive mails. The implementation is fairly simple, to keep the interraction between users using mails. I wanted to make a project like this to expand my knowledge of Flask and of techniques like dynamic messaging and automatic refreshing of the inbox for new mails, databased authentications, etc.

Technologies used:

- flask
- jinja2
- sessions
- sqlite3
- other small libraries or packages

## How the application works?

The idea is simple. The user can register for a new account. During registration you need to enter these fields:

- Email
- password
- Confirm Password: it is checked to match, must be at least 8 Characters     long and is hashed after checks are done

once a user registers for an account, he is redirected to the login page where he is now required to login inorder to access the contents inside his account. this includes the inbox, compose, sent, and logout.

a user can compose mail and send to a known address assuming the friend's email address. he can also receive mails form the fiend and vice versa.

this application has two sections

## first section
1. login
    this is a login form where a user is required to type in his email and password for the application to verify and grant him access to his emailing window.

2. Register
    this register form allows the a new user to create an email account by typing in the email as username and a password which is posted in the database as a hash and stored for later login.

## Second section
1. inbox
    this window is displayed by default when a user is logged in. it displays current received emails and a button on the right to view an email.

2. compose
    this window provides a form in which a user can type in the receivers email address, the subject of the email he is composing and the body of the email which holds the content of the email being composed.

3. sent
    the send window displays the sent mails of the user allowing him to view the contents he has already sent to another user at any given time.

4. logout
    this tab has only one purpose and its purpose id to close the users session and render a login templete.


### Routing

Each route checks if the user is authenticated. It means if correct mail and password were supplied. 

### Sessions

The application uses sessions to confirm that user is registered. Once the user logins, his credentials are checked with the hash function. Once everything passes a session is created (serialized and deserialized) and stored in the cookies.

### Database

Database stores all users and emails.
