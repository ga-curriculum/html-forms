# ![Intermediate HTML - Input Elements and Labels](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to tktk

## The input element

As we discussed above, `<form>` is a container element, designed to be filled with other elements. 

Let's introduce one of the most common elements now: `<input>`

The `<input>` element is the primary way to create interfaces for interacting with the user. `<input>` elements can vary drastically depending on their `type` attribute, which dictates a lot about the behavior of the `<input>`. 

For example, an `<input>` with the `type="text"` attribute creates a single-line text field. An `<input>` with the `type="checkbox"` attribute, in contrast, creates a single check box that toggles between selected and deselected. Some input types like `type="data"` create entire data pickers.  

Add the following form to `index.html`: 

```html
<form>
  <input type="text" />
  <input type="checkbox" />
  <input type="date" />
  <input type="color" />
</form>
```

Open the page in the browser and experiment with each input. You'll see that while they are all `<input>`'s, the behavior of each type of input varies wildly. 

## Using labels

You may have also noticed that it's hard to determine what each of these inputs is for. Giving each of our inputs a clear label helps to solve that issue, and is especially important for accessability. 

First, let's simplify our code a bit. We'll change the inputs to mimic a simple "Contact Us" form: 

```html
<form>
  <input type="text">
  <input type="email">
  <input type="text">
</form>
```

Next, let's add labels that denote what information each input is seeking to capture: 

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

Note that we use a `for` attribute on each `<label>` element, which corresponds an `id` of the input it is labelling. This step achieves two things - first, it allows for mouse, trackpad, and touch device association between the label and the input, and secondly it gives each input a legible name for screen readers. 

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

After making the above adjustments, open the browser again and test this new <textarea> out. Much better!


## Basic Form Considerations

When creating a form, try to keep things simple and focused. While forms are often necessary to collect certain information, from a user's perspective entering a lot of data can be frustrating. 

When building a basic contact form, what information do we actually need from the user? 

- We want to collect their name, so that we know how to refer to them in a reply. This will require an `<input type="text" />` element.
- We need their email address, so that we have the ability to reach back out to them. This will require an `<input type="email" />` element.
- Finally, we need to collect their message itself. This could use an `<input>` element, but for reasons discussed above is better suited to a `<textarea>` element.

Any other information we try to collect will likely feel unnecessary. Asking for the users age, or location, or the number of cats they have in their household etc. is not directly relevant, so inputs for this information should be omitted. 