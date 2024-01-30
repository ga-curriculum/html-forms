# ![HTML Forms - Level Up - The Select Element](./assets/the-select-element.png)

**Learning objective:** By the end of this lesson, students will be able to use the `<select>` element and its accompanying `<option>` elements to create dropdown menus in HTML forms. 

One frequently used element is `<select>`, which is used for creating dropdown menus so that the user can select from a list of options. 

Each `<select>` element will contain a number of `<option>` 
elements. 

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
  <!-- Add the following: -->
  <div>
    <label for="category"> I'm contacting about: </label>
    <select id="category">
      <option value="work">A job opportunity</option>
      <option value="question">A question</option>
      <option value="misc">Miscellaneous</option>
    </select>
  </div>

  <div>
    <label for="msg"> Message: </label>
    <textarea id="msg" required maxLength="100"></textarea>
  </div>
  <button type="submit"> Submit <button>
</form>
```

As with our other inputs, we will attach a label by giving the `<select>` an `id`, and giving the label a `for` attribute that matches.  

Each `<option>` should have a `value` that contains the data value you want to submit with the form. If the user selects this option, then that `value` attribute is what will be sent to the server. For example, given the following `<option>`

```html
<option value="cats"> I Love Cats </option>
```

The user selects the string "I Love Cats", but the form itself submits "cats" as the value. 

## A quick note on styling

Select, and option elements in particular, are notoriously difficult to style. They are quite limited as far as what is able to be styled, and depending on the browser some key visual attributes like font and background color aren't accessible at all. 

You can learn more about the difficulties with styling select and option elements from MDN's [Advanced Form Styling](https://developer.mozilla.org/en-US/docs/Learn/Forms/Advanced_form_styling). 

