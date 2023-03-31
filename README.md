Flask Web App for Email

Video Demo: https://youtu.be/9qOyya1-UDY

Description:

West Mail is a Flask-based web application that offers a range of basic email functionality for users. With West Mail, users can easily compose and send emails to their contacts, check their inbox, and read and respond to emails, just like they would on any other email client. The application is designed with user-friendliness and security in mind and is built on top of Flask, a popular Python web framework that provides developers with a wide range of tools and features to create robust and scalable web applications.

One of the key features of West Mail is its focus on security and privacy. The application uses email encryption technology to ensure that emails are secure and private, and that only the intended recipient can read the message. This feature is particularly important for users who want to keep their emails confidential and secure. In addition to its security features, West Mail also offers a mobile app with push notifications. This makes it easy for users to stay up-to-date with their emails on the go, and ensures that they never miss an important message.

West Mail offers a range of features to make email management easier and more convenient. These features include a compose and send email functionality, which allows users to easily create and send emails to their contacts. The inbox functionality allows users to check their inbox and view their incoming emails. Additionally, the read and respond to email functionality allows users to view their emails and reply to them directly from the application.

Another important feature of West Mail is its user interface, which is designed to be modern, user-friendly, and easy to navigate. The application uses HTML, CSS, Bootstrap, and JavaScript to create a modern and responsive interface that is easy to use on any device, from desktop computers to mobile phones.

The application is easy to set up and can be run using Flask's built-in server. To run the application, simply execute the command "flask run" from the command line. This will start the Flask development server, which can be accessed by opening a web browser and navigating to the specified address.

West Mail is an open-source project, which means that anyone can contribute to its development. The project is hosted on GitHub, where users can view the source code, contribute bug fixes and new features, and report issues or suggest improvements.

Overall, West Mail is an excellent choice for anyone looking for a simple and secure email client that offers all the basic functionality they need. With its focus on security, privacy, and mobile app functionality, West Mail is a great option for anyone who wants to stay connected and productive on the go. The application's modern and user-friendly interface, combined with its robust security features and easy-to-use functionality, make it an ideal choice for anyone who wants to manage their email easily and efficiently.

Features:

West Mail offers the following features:

Compose and send emails to your contacts
Check your inbox
Read and respond to emails
Secure and private email encryption technology
Mobile app with push notifications
Contributing:

If you would like to contribute to West Mail, we welcome pull requests to help improve the app and make it even more user-friendly.

Running the Application:

To run the application, enter the following command: flask run

One of the key features of West Mail is its focus on security and privacy. The application uses email encryption technology to ensure that emails are secure and private, and that only the intended recipient can read the message. This feature is particularly important for users who want to keep their emails confidential and secure.

In addition to its security features, West Mail also offers a mobile app with push notifications. This makes it easy for users to stay up-to-date with their emails on the go, and ensures that they never miss an important message.

West Mail was built using Flask, a popular Python web framework. Flask makes it easy to build web-based applications, and provides developers with a wide range of tools and features to create robust and scalable applications. The application also uses HTML, CSS, Bootstrap, and JavaScript to create a modern and user-friendly interface.

Overall, West Mail is a great choice for users who are looking for a simple and secure email client that is easy to use and provides all the basic functionality they need. With its focus on security, privacy, and mobile app functionality, West Mail is a great option for anyone who wants to stay connected and productive on the go.

LAYOUT OF THE PAGES:
the layout of the HTML file for the West Mail web application. It defines the structure of the web page and the various elements that make up the user interface of the application.

The first part of the HTML code includes meta tags that specify the character set and viewport settings for the web page. It also includes links to external resources, such as the Bootstrap CSS and JavaScript files, which provide styles and functionality for the web page.

The second part of the HTML code defines the structure of the web page. It includes a navigation bar at the top of the page that allows users to navigate between different sections of the application. The navigation bar contains links to the inbox, compose, and sent messages pages for logged-in users, as well as a link to the log out page. For non-logged-in users, the navigation bar contains links to the register and login pages.

The HTML code also includes a section for displaying flash messages, which are messages that are displayed to users to indicate the outcome of an action, such as successfully sending a message or encountering an error.

The main content of the web page is contained within a main section that is divided into various blocks. The main block is where the content of each page is displayed, and it is defined using the {% block main %}{% endblock %} syntax. This allows the content of each page to be easily added or modified by overriding the main block in a child template.

Finally, the HTML code includes a footer section that displays attribution information for the data used in the application.

In summary, the layout of the HTML code implies to the West Mail application by providing a consistent structure and user interface across the different pages of the application. It allows for easy navigation between different pages and provides feedback to users through flash messages. By using the Bootstrap CSS and JavaScript files, it ensures a responsive and visually appealing user interface.

compose.html:
The first block in the code sets the title of the page to "Compose". The second block is where the main content of the page is defined. It is a form that allows the user to compose an email. The form has several input fields, including the sender's email address, recipient's email address, subject, and body of the email. The input fields are styled using Bootstrap classes to make them look consistent and modern.

The form action is set to "/compose", which means that when the user clicks the "Submit" button, the data entered into the form will be sent to the "/compose" URL in the backend of West Mail.

Overall, this code is an important part of the West Mail application as it allows users to create and send emails. It is designed to be user-friendly and visually appealing, making it easier for users to compose and send emails.

email.html:
This HTML code block defines two blocks, title and main. The title block sets the title of the page to "Emails". The main block contains a series of div elements that display the details of an email message, including the sender, recipient, subject, timestamp, and body. The code also includes a form that allows the user to reply to the email message.

Similar to the previous code blocks, this code block will be rendered using the layout.html template when the corresponding URL is accessed. The extends statement tells Flask to use the layout.html template as the base template for this page, and the block statements define where the content for the title and main sections should be placed within the base template.

index.html:
The first line {% extends "layout.html" %} is telling the template engine to use the layout.html file as the base layout for this page.
The {% block title %}...{% endblock %} block is defining the page title, which will be inserted into the <title> tag in the HTML output.
The {% block main %}...{% endblock %} block is defining the main content of the page. Inside this block, there is a for loop that iterates over a list of emails passed into the template. For each email object, a HTML block is created that displays the sender, subject, timestamp, and a button to view the full email. The button is a form element that submits a hidden input emailId to the server when clicked, so that the server can retrieve the full email and render a new page.
Overall, this template is a way to render a list of emails with some basic information, and the ability to view the full email on a new page.

login.html:
It creates a form for a user to log in, with fields for username and password. The form submits to the "/login" endpoint using the HTTP POST method when the user clicks the "Log In" button. The username and password fields are input elements with the "form-control" class applied, which is a Bootstrap class that adds styling to form elements. The "autofocus" attribute is set on the username input field, which automatically sets focus to the field when the page loads. The "{{}}" syntax is used to interpolate the values of variables in the template, such as the values entered into the username and password fields.

register.html:
 It extends the layout.html template and creates a form that allows users to input their email, password, and confirm their password. The form's action is set to "/register" and the method is set to "post". The form's submit button is labeled "Register". Once the user submits the form, the data will be sent to the "/register" endpoint in the backend for processing.

 reply.html:
  It extends a layout file and defines a block for the page title and the main content. The main content includes a form with fields for the sender, recipient, subject, and body of the email being composed. The values of the fields are pre-filled with information from the email being replied to. Finally, there is a button to submit the form.

  projectdb:
  this is the database that house the data used in the infrastructure of west mail including all information like emails and messages sent between end users and password stored too and also encrypted