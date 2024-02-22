# ![HTML Forms - Level Up - Advanced Form Validation and Feedback](./assets/advanced-form-validation-and-feedback.png)

**Learning objective:** By the end of this lesson, students will be able to apply advanced form validation techniques using HTML and CSS. They will learn to use pseudo-classes like `:valid` and `:invalid` for live form validation feedback.

## CSS Selectors for Form Feedback

As we've seen, client-side form validation is a useful way to give users feedback about the data they've entered into a form. The downside is that, so far, in order to receive this feedback, users have needed to try and submit the form. This means that, if anything is incomplete or entered incorrectly, the user only knows this upon rejection - not the best user experience.

Luckily, HTML5 introduced new pseudo-classes like `:valid` and `:invalid` that help us add live validation feedback to our forms.

Let's leave our existing 'Contact Us' form aside for now, and use a simple login form to demonstrate the power of these pseudo-classes:

```html
  <form action="/sign-in" method="post">
    <label for="user">Username:</label>
    <input 
      type="text" 
      id="user" 
      minlength="6" 
      required 
    />
    <label for="password">Password:</label>
    <input 
      type="password" 
      id="password" 
      minlength="6" 
      required 
    />
    <button type="submit">Sign In</button>
  </form>
```

We have a username input that is `type="text"` and a password input that is `type="password"`. In addition, we set a required minimum length of 6.

Let's work on adding some feedback! To do so, we'll first need to create a `CSS` file:

```bash
mkdir css
touch css/style.css
```

Then, in `index.html`, link the style sheet.

Finally, in `style.css`, add the following:

```css
input:valid {
  border: green 1px solid;
  background-color: lightgreen;
}
```

By default, all of our inputs will be considered invalid. This is because they are empty (and each field is required), and also because each input has a `minLength` of 6 characters. We could add styling for `input:invalid` as well, however this is less pleasant to look at when completing a form.

Once all of the necessary conditions are met, the input becomes valid. You can test this out in the browser now - once you hit 6 characters in either field, the border and background should change, indicating a valid entry.

Hold on though - as it stands, we're allowing our users to set some truly weak passwords. '123456' or 'password' would both pass our current validation standards.

We can use the [pattern](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/pattern) attribute and a [regular expression](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_expressions) to create more strict requirements for validity. Don't worry too much about understanding the regular expression, just know that a regular expression is essentially a string of text that lets you define a pattern. We can use these strings to enforce a specific pattern for an input!

Let's take a common example. Most passwords require at least one uppercase character and at least 1 number, along with at least 1 special character.

We'd specify these requirements like so:

```html
    <label for="password">Password:</label>
    <input 
      type="password" 
      id="password" 
      pattern="(?=.*\d)(?=.*[a-z])(?=.*[A-Z])(?=.*[@#$%^&+=!?]).{6,}"
      required 
    />
```

Explained briefly and at a very surface level, this is what the regular expression string is specifying:

`(?=.*\d)` contains at least one digit
`(?=.*[a-z])` contains at least one lowercase letter
`(?=.*[A-Z])` contains at least one uppercase letter
`(?=.*[@#$%^&+=!?])` contains at least one special character from the included characters
`.{6,}` is a word of at least 6 characters

So, we are looking for a word of at least 6 characters in which there is at least one digit, lowercase letter, uppercase letter, and special character. Since our pattern also enforces a minimum length, we can remove the `minLength` attribute from our `<input>`.

In the browser, try entering a password that conforms to this pattern. You should get visual feedback from our `:valid` selector once you've matched the pattern correctly.

> 🧠 Remember, all of this validation is happening on the client side. The `:valid` selector turns the input border green when the user's input matches the required pattern, but the password entry won't be verified until that data gets to the server and can be matched against the correct password held there.

## Accessibility Concerns

Typically, invalid inputs are styled red while valid inputs are styled green. For people with certain types of color blindness, this can present accessibility issues. As such, accompanying text or icons are typically favored over simply using color to note the validity of a form. This can be handled with JavaScript, or in CSS by adding an image background of an icon to the input background.
