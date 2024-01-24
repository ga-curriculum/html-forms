# ![Intermediate HTML - Button Elements in Forms](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to use a button to submit a form.

## The button element

With our form complete, we have one final step - we need some way for the user to submit the form once it has been filled out. 

For this, we can use a `<button>` element with a type attribute of `"submit"`. When a `<button type="submit">` inside of a form element is clicked, it will submit the form data to the URL designated by the form's `action` attribute.

```html
<form action="/the-form-submits-here" method="post">
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
  <button type="submit"> Submit <button>
</form>
```

> As `"/the-form-submits-here"` is a placeholder URL, clicking submit in this example does nothing. 

