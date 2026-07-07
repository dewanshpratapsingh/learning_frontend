# Forms & Accessibility

Forms are used to **collect data from users**.

## Common Examples

- Login page
- Signup page
- Contact form
- Search bar
- Checkout page
- Job application
- Feedback form

---

# `<form>`

The `<form>` element groups related user inputs together.

Example:

```html
<form>
    ...
</form>
```

A form tells the browser:

> "These input fields belong together and will be submitted as one unit."

---

## Important Attributes

### `action`

Specifies **where** the form data should be sent after submission.

```html
<form action="/login">
```

Example:

```text
User clicks Submit
        ↓
Browser sends data to
        ↓
/login
```

---

### `method`

Specifies **how** the data is sent.

The two most common methods are:

- `GET`
- `POST`

Example:

```html
<form action="/login" method="POST">
```

---

# Labels

Every form control should have a label.

Bad:

```html
<input type="text">
```

Users and screen readers don't know what this input is for.

---

## Proper Label Association

Correct:

```html
<label for="name">Name</label>

<input
    id="name"
    type="text"
>
```

Notice that:

- `for="name"` on the label
- `id="name"` on the input

must match.

### Why?

- Clicking the label focuses the input.
- Screen readers know which label belongs to which input.
- Improves accessibility.
- Makes forms easier to use.

---

# Common Input Types

## Text

```html
<input type="text">
```

Used for:

- Name
- Username
- City

---

## Email

```html
<input type="email">
```

Used for email addresses.

Benefits:

- Browser validates email format.
- Mobile devices show an email-friendly keyboard.

---

## Password

```html
<input type="password">
```

Hides typed characters.

---

## Number

```html
<input type="number">
```

Used for numeric values such as:

- Age
- Quantity

---

## Telephone

```html
<input type="tel">
```

Used for phone numbers.

Shows a numeric keypad on mobile devices.

---

## Date

```html
<input type="date">
```

Displays a date picker.

---

## Checkbox

Allows multiple selections.

```html
<input type="checkbox">
```

Example:

```text
☐ Java
☐ Python
☐ C++
```

Users can select multiple options.

---

## Radio Button

Allows only one selection from a group.

```html
<input type="radio">
```

Example:

```text
○ Male
○ Female
○ Other
```

### Important

All radio buttons in the same group **must share the same `name` attribute**.

```html
<input type="radio" name="gender" value="male">
<input type="radio" name="gender" value="female">
<input type="radio" name="gender" value="other">
```

Without the same `name`, multiple radio buttons can be selected, which defeats their purpose.

---

## File

```html
<input type="file">
```

Allows users to upload files.

---

## Color

```html
<input type="color">
```

Displays a color picker.

---

## Range

```html
<input type="range">
```

Creates a slider.

---

# Placeholder

Example:

```html
<input
    type="text"
    placeholder="Enter your name"
>
```

A placeholder provides a hint about the expected input.

### Important

A placeholder is **not a replacement for a label**.

Bad:

```html
<input placeholder="Email">
```

Good:

```html
<label for="email">Email</label>

<input
    id="email"
    type="email"
    placeholder="example@gmail.com"
>
```

---

# `<textarea>`

Used for multi-line text input.

Examples:

- Feedback
- Comments
- Messages

```html
<textarea></textarea>
```

Unlike `<input>`, it has both opening and closing tags.

---

# `<select>`

Creates a dropdown list.

```html
<select>
    <option>India</option>
    <option>USA</option>
    <option>Japan</option>
</select>
```

Each option is defined using the `<option>` element.

---

# `<button>` vs `<input type="submit">`

Old approach:

```html
<input type="submit">
```

Preferred approach:

```html
<button type="submit">
    Submit
</button>
```

### Why prefer `<button>`?

A button can contain:

- Text
- Icons
- Images
- Other HTML elements

Example:

```html
<button type="submit">
    📩 Send Message
</button>
```

---

# `required`

The `required` attribute prevents form submission if the field is empty.

```html
<input
    type="email"
    required
>
```

---

# `name`

The `name` attribute identifies the data when the form is submitted.

```html
<input
    name="email"
    type="email"
>
```

Submitted data:

```text
email=dewansh@example.com
```

Without the `name` attribute, the field's value is **not included** in the submitted form data.

---

# Accessibility

Accessibility ensures that everyone can use your website, including:

- Blind users
- Keyboard-only users
- Low-vision users
- Users with motor disabilities
- Color-blind users

---

## `alt` Attribute

Every meaningful image should include an `alt` attribute.

Bad:

```html
<img src="profile.png">
```

Good:

```html
<img
    src="profile.png"
    alt="Portrait of Dewansh Pratap Singh"
>
```

Benefits:

- Displayed if the image fails to load.
- Read aloud by screen readers.

For decorative images:

```html
<img src="divider.png" alt="">
```

---

## `aria-label`

Used when an element has no visible text.

Example:

Bad:

```html
<button>
    🔍
</button>
```

A screen reader only announces:

> Button

Good:

```html
<button aria-label="Search">
    🔍
</button>
```

Now the screen reader announces:

> Search button

---

# Keyboard Accessibility

A good website should be fully usable without a mouse.

Press the **Tab** key and ensure users can navigate through:

- Links
- Buttons
- Input fields
- Dropdowns
- Textareas

If an interactive element cannot be reached using the keyboard, there is likely an accessibility issue.

---

# Best Practices

- Always associate `<label>` with an input using `for` and `id`.
- Use the correct `input` type for each field.
- Never use a placeholder instead of a label.
- Always include the `name` attribute.
- Use `<button>` instead of `<input type="submit">`.
- Add `required` where appropriate.
- Provide meaningful `alt` text for images.
- Use `aria-label` for icon-only buttons.
- Test forms using only the keyboard.
- Choose semantic HTML elements whenever possible.