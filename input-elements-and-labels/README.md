# ![Intermediate HTML - Input Elements and Labels](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to create a form with labeled inputs. 

## The input element

As we discussed above, `<form>` is a container element, designed to be filled with other elements. 

Let's introduce one of the most common elements now: `<input>`

The `<input>` element is the primary way to create interfaces for interacting with the user. `<input>` elements can vary drastically depending on their `type` attribute, which dictates a lot about the behavior of the `<input>`. 

An `<input>` with a type of `"text"` will create a single-line text field.

An `<input>` with a type of `"email"` will at first glance look identical to one with a type of `"text"`, but will offer some validation to make sure the input is formatted like an email address. 

Let's add the following three `<input>` elements to our form:

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

So, let's add labels to display what information each input is seeking to capture: 

```html
<form>
  <label for="name"> Name: </label>
  <input type="text" id="name" />
  <label for="email"> Email: </label>
  <input type="email" id="email" />
  <label for="msg"> Message: </label>
  <input type="text" id="msg" />
</form>
```

Note that we use a `for` attribute on each `<label>` element, which corresponds to an `id` of the input it is labelling. This step achieves two things - first, it allows for mouse, trackpad, and touch device association between the label and the input, and secondly it gives each input a readable name for screen readers. 

If we open these changes in the browser, we should see that each input has been given a label. 

## The textarea element

One final optimization before we move on. If you try to type a lengthy message into the "msg" textbox, you'll notice that the input field remains a fixed, single-line size. Imagine if you wanted to write a paragraph long question, or more - it would be a pretty awful user experience! 

Luckily, we can instead use the `<textarea>` element, which is an input element specifically designed for multiline text! 

<form>
  <label for="name"> Name: </label>
  <input type="text" id="name" />
  <label for="email"> Email: </label>
  <input type="email" id="email" />
  <label for="msg"> Message: </label>
  <textarea id="msg"></textarea>
</form>

Unlike `<input>`, `<textarea>` needs a closing tag. 

After making the above adjustments, refresh the browser and test this new `<textarea>` out. Much better!

## Form Structure

When structuring inside of a form, we can use normal HTML. `<p>` tags and `<div>` tag are commonly used to create structure, as are lists. 

As an example of this, let's add some `<div>` tags to give our contact form a more vertical alignment. 

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


## Basic Form Considerations

When creating a form, try to keep things simple and focused. While forms are often necessary to collect certain information, from a user's perspective entering a lot of data can be frustrating. 

When building a basic contact form, what information do we actually need from the user? 

- We want to collect their name, so that we know how to refer to them in a reply. This will require an `<input type="text" />` element.
- We need their email address, so that we have the ability to reach back out to them. This will require an `<input type="email" />` element.
- Finally, we need to collect their message itself. This could use an `<input>` element, but for reasons discussed above is better suited to a `<textarea>` element.

Any other information we try to collect will likely feel unnecessary. Asking for the users age, or location, or the number of cats they have in their household etc. is not directly relevant, so inputs for this information should be omitted. 