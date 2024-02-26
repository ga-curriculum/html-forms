# ![HTML Forms - Advanced Input Types](./assets/advanced-input-types.png)

**Learning objective:** By the end of this lesson, students will be able to identify and utilize various advanced HTML input types.

## Using advanced inputs

We've explored some common input types, such as a text input, but over twenty different input types are available, each with distinct behaviors. An `<input>` with the `type="checkbox"` attribute, for example, creates a single check box that toggles between selected and deselected. Some input types like `type="date"` create entirely new types of inputs!

Let's look at some examples. Add the following form to `index.html`:

```html
<h2>Advanced input demo</h2>
<form>
  <div>
    <label for="checkbox-input">Checkbox input:</label>
    <input type="checkbox" id="checkbox-input" />
  </div>
  <div>
    <label for="number-input">Number input:</label>
    <input type="number" id="number-input">
  </div>
  <div>
    <label for="date-input">Date input:</label>
    <input type="date" id="date-input"/>
  </div>
  <div>
    <label for="color-input">Color input:</label>
    <input type="color" id="color-input" />
  </div>
  <div>
    <label for="password-input">Password input:</label>
    <input type="password" />
  </div>
  <div>
    <label for="telephone-input">Telephone input:</label>
    <input type="tel" id="telephone-input"/>
  </div>
</form>
```

Open the page in the browser and experiment with each input. You'll see that while they are all `<input>` elements, the behavior of each type of input varies greatly.

- `number` ensures that an input will only be valid if it only contains numberical values. Mobile browsers on touchscreen devices show a numerical keyboard when users interact with this input, further improving their experience.
- `date` is a helpful type due to the variety of date formats worldwide (DD/MM/YYYY, MM/DD/YYYY, YYYY/MM/DD, etc). Using the `date` type for inputs helps ensure users format a date strings correctly.
- `color` is similarly helpful as many users will not be familiar with RGB or Hexadecimal codes, and adding a visual component will help many users select the color they want for an input.
- `password` is similar to text but has the added benefit of obscuring the value as it is being entered.
- `tel` can be very useful for mobile sites, as it will attempt to bring up a keypad to make entering a phone number easier. Note that `tel` will not attempt to validate the structure of a phone number because there is too much variance in telephone format worldwide.

You can check out the [full list of input types](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#input_types) on MDN.
