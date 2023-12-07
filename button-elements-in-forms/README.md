# ![Intermediate HTML - Button Elements in Forms](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to tktk


## The button element

With our form complete, we have one final step - we need some way for the user to submit the form once it has been filled out. 

For this, we can use a `<button>` element with a type attribute of `"submit"`. If the `<button type="submit">` is inside of the form element, it will submit the form data when clicked. 

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
  <button type="submit"> Submit <button>
</form>
```
