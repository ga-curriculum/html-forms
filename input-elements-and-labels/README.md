# ![HTML Forms - Input Elements and Labels](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to create a form with labeled inputs. 

## The input element

The `<form>` is a container element, designed to be filled with other elements. One of the most common and versatile of these elements is the `<input>` tag.

The `<input>` element is the primary way to create interfaces for interacting with the user. The look of `<input>` elements can vary drastically depending on their `type` attribute, which dictates a lot about the behavior of the `<input>` and the kind of information they collect. 

**Common Text Based Inputs**

- **Text Input:** The most basic form of an input field. It allows users to enter a single line of text.

- **Email Input:** Similar in appearance to the text input but comes with built-in validation for email addresses. This ensures users enter a valid email format. 

Let's add the following `<input>` elements to our form:

```html
<form>
  <input type="text">
  <input type="email">
  <input type="text">
</form>
```

Open the page in the browser and check out the result!

## Using labels

You may have noticed that it's hard to determine what each of these inputs is supposed to do. Giving each of our inputs a clear label helps to solve that issue, and is an especially important step for maintaining good accessability. 

*Labels* provide a clear description of what information each input field is seeking. They are particularly important for users with visual impairments who rely on screen readers, as labels offer context that's otherwise missing.

Let's add labels to our form to illustrate their use:

```html
<form>
  <label for="name">Name:</label>
  <input type="text" id="name">
  <label for="email">Email:</label>
  <input type="email" id="email">
  <label for="message">Message:</label>
  <input type="text" id="message">
</form>
```

Notice the `for` attribute in the `<label>` element. This attribute should match the `id` of the corresponding input field. This link allows screen readers to announce the label when the user focuses on the input, enhancing accessibility.

> 💡 Labels also improve the user experience on various devices. For instance, clicking on the label on a touchscreen device will focus the corresponding input field, just like a mouse click would.

If we open these changes in the browser, we should see that each input has been given a label. 

## The textarea element

One final optimization before we move on. If you try to type a lengthy message into the "msg" textbox, you'll notice that the input field remains a fixed, single-line size. Imagine if you needed to write a paragraph or give detailed feedback - it would be a pretty awful user experience! 

The `<textarea>` element is specifically designed for multi-line text input, providing a much better user experience for lengthier text entries. It expands vertically, allowing users to enter and view their text comfortably.

Let's replace the single-line message input with a textarea:

```html
<form>
  <label for="name">Name:</label>
  <input type="text" id="name">
  <label for="email">Email:</label>
  <input type="email" id="email">
  <label for="message">Message:</label>
  <!-- Replacing input with textarea -->
  <textarea id="message"></textarea>
</form>
```

> Note: Unlike `<input>`, `<textarea>` needs a closing tag `</textarea>`. 

Refresh the browser and test this new `<textarea>` out. Much better!

## Form structure

In HTML forms, organization and clarity are really important. While you can use any regular HTML elements within a form, certain tags, like `<p>`, `<div>`, and lists, are particularly helpful in creating a user-friendly layout.

As an example, let's add some `<div>` tags to give our contact form a more vertical alignment. 

```html
<form>
  <div>
    <label for="name"> Name: </label>
    <input type="text" id="name" />
  </div>
  <div>
    <label for="email"> Email: </label>
    <input type="email" id="email" />
  </div>
  <div>
    <label for="msg"> Message: </label>
    <textarea id="msg"></textarea>
  </div>
</form>
```

Check your new layout in the browser! 

## Basic form considerations

When creating a form, try to keep things simple and focused. While forms are often necessary to collect certain information, from a user's perspective, entering a lot of information on a webpage can be tedious and frustrating.

When building a basic contact form, what information do we *actually* need from the user? 

- We want to collect their name, so that we know how to refer to them in a reply. This will require an `<input type="text" />` element.
- We need their email address, so that we have the ability to respond to them. This will require an `<input type="email" />` element.
- Finally, we need to collect the message itself. A `<textarea>` element is ideal for this, as it accommodates longer, multi-line text.

**Keeping it relevant and user-friendly**

Any other information we try to collect will likely feel unnecessary. Asking for the users age, or location, or the number of cats in their household is not directly relevant, so inputs for this information should be omitted. Stick to information that serves the immediate needs of your interaction with the user. This approach respects the user's time and privacy, leading to a more positive experience and higher likelihood of form completion.