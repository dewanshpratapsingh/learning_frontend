# Forms and Accessibilty
- A form is used to collect data from the user.
- Examples:
Login page
Signup page
Contact form
Search bar
Checkout page
Job application

- <form>

The <form> element groups user inputs together.

Example:

<form>
    ...
</form>
A form tells the browser:

"These fields belong together and will be submitted."

Important Attributes
action

Specifies where the data should be sent.
<form action="/login">
- method
Specifies how the data is sent.
<form action="/login" method="POST">
Labels

One of the most important concepts.

Suppose you write

<input type="text">

Proper Label Association

Correct way:

<label for="name">
    Name
</label>

<input
    id="name"
    type="text">

    Why?

Now clicking

Name

focuses the input.

Screen readers also know:

"This label belongs to this input."

This is much better for accessibility.

common input types
Important:

All radio buttons in the same group must share the same name.