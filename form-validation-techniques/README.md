# ![Intermediate HTML - Form Validation Techniques](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to tktk

## Form Validation

As a user, you no doubt have had the experience of entering information into a form and pressing the submit button, only for "This field is required" to pop up next to an empty input you missed. Or perhaps you've entered a password that didn't exactly conform to the 12 different rules laid out on a sign-up page. While this can be frustrating, it's actually for the user's benefit - after all, why allow data to make it to the server if we know it's not in a form we can use?

This is called client-side validation - tests that happen before the data is actually sent off to wherever it's going. 

## Built-in form validation

Some validation is built in to HTML as validation attributes. 

A popular example of one of these attributes is `required`, which ensures that a form field is filled in (has a value) before the form can be submitted. It's a Boolean, so we don't need to use `required="true"`. Simply including the attribute on the input is sufficient: 

```html
<form action="/the-form-submits-here" method="post">
  <div>
    <label for="name"> Name: </label>
    <input type="text" id="name" required />
  </div>
  <div>
    <label for="email"> Email: </label>
    <input type="email" id="email" required />
  </div>
  <div>
    <label for="msg"> Message: </label>
    <textarea id="msg" required></textarea>
  </div>
  <button type="submit"> Submit <button>
</form>
```

Note that the "email" type input also has a further level of [built-in validation](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/email#value), as mentioned previously. By default, `<input type="email">` will automatically make sure that the input value is either empty, or properly-formatted. In this way, `type` itself can be considered a form of validation as well. 

When we make an `<input type="email">` input required, we also ensure that it cannot be empty. This way, we guarantee* an email address will be entered before this form can be submitted. 

> 🧠 A note on the word "guarantee"
> Client-side validation should never be considered as a replacement for server-side validation, as client-side validation is relatively easy to bypass. Rather, client-side validation is intended to provide a better user experience by catching and rejecting invalid entries and allowing a user to fix them immediately. 

We can also use built in validation to control things like the `maxLength` of a text entry, or the `min` and `max` values of numerical inputs.

For instance, to prevent someone from copying an entire novel into our `<textarea>` (the default max characters of a textarea is 524,288, which is roughly 375 pages), we could add a `maxLength` attribute: 

```html
<form action="/the-form-submits-here" method="post">
  <div>
    <label for="name"> Name: </label>
    <input type="text" id="name" required />
  </div>
  <div>
    <label for="email"> Email: </label>
    <input type="email" id="email" required />
  </div>
  <div>
    <label for="msg"> Message: </label>
    <textarea id="msg" required maxLength="100"></textarea>
  </div>
  <button type="submit"> Submit <button>
</form>
```

Open this in your browser and start typing - you'll see that after 100 characters, you're cut off from entering anything further. 
