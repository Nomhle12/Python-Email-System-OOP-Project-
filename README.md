Python-Email-System-OOP-Project
Email simulation system built using Python Object-Oriented Programming (OOP)

Overview
This project is a simple email simulation system built using Python Object-Oriented Programming (OOP). It demonstrates how users can send, receive, read, and delete emails within a virtual inbox system. Each email includes metadata such as sender, receiver, subject, body, timestamp, and read status.

Features

- Create users
- Send emails between users
- Receive emails into an inbox
- List all emails in inbox
- Read full email content
- Delete emails
- Automatic timestamping of emails
- Read/unread tracking

Project Structure

Email Class
Represents a single email message.

Attributes:
- `sender` → User who sends the email  
- `receiver` → User who receives the email  
- `subject` → Email subject  
- `body` → Email message content  
- `timestamp` → Time email was created  
- `read` → Status of email (True/False)  

Methods:
- `mark_as_read()` → Marks email as read  
- `display_full_email()` → Displays full email content  
- `__str__()` → Returns a short email summary  

Inbox Class
Manages a collection of emails for a user.

Attributes:
- `emails` → List of Email objects  

Methods:
- `receive_email(email)` → Adds email to inbox  
- `list_emails()` → Displays all emails in inbox  
- `read_email(index)` → Opens and displays selected email  
- `delete_email(index)` → Removes email from inbox  

User Class
Represents a system user.

Attributes:
- `name` → User’s name  
- `inbox` → Inbox object  

Methods:
- `send_email(receiver, subject, body)` → Sends an email  
- `check_inbox()` → Displays inbox summary  
- `read_email(index)` → Reads a specific email  
- `delete_email(index)` → Deletes a specific email  

How It Works:

1. Users are created using the `User` class  
2. A sender creates and sends an email  
3. The email is added to the receiver’s inbox  
4. The receiver can:
   - View all emails
   - Read full emails
   - Delete emails
     
Example Usage:
tory = User('Tory')
ramy = User('Ramy')

tory.send_email(ramy, 'Hello', 'Hi Ramy, just saying hello!')
ramy.send_email(tory, 'Re: Hello', 'Hi Tory, hope you are fine.')

ramy.check_inbox()
ramy.read_email(1)
ramy.delete_email(1)
ramy.check_inbox()

Timestamp Format
Emails use the following format: YYYY-MM-DD HH:MM
Example: 2026-06-01 14:35

Concepts Used
Object-Oriented Programming (OOP)
Classes and Objects
Encapsulation
Lists and Indexing
datetime module
String formatting (f-strings)

Author
Nomhle Mabena
