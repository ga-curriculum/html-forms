# ![HTML Forms - Advanced Input Types](./assets/advanced-input-types.png)

**Learning objective:** By the end of this lesson, students will be able to identify and utilize various advanced HTML input types.

## Using advanced inputs

We've explored some common input types, such as a text input, but over twenty different input types are available, each with distinct behaviors. An `<input>` with the `type="checkbox"` attribute, for example, creates a single check box that toggles between selected and deselected. Some input types like `type="date"` create entirely new types of inputs!

Let's look at some examples. Add the following form to `index.html`:

```html
<h2>Advanced input demo</h2>
<form>
  <div>
    <label for="number-input">Number input:</label>
    <input type="number" id="number-input">
  </div>
  <div>
    <label for="checkbox-input">Checkbox input:</label>
    <input type="checkbox" id="checkbox-input" />
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

- **Date** is a useful type due to how commonly users will format a date string incorrectly. Using a time/date picker helps to ensure the date is always expressed in the same order.
- **Color** is similarly useful as many users will not be familiar with RGB or Hexadecimal codes, and adding a visual component will help many users in selecting the color they want for an input.
- **Password** is similar to text, but has the added benefit of obscuring the value as it is being entered.
- **Tel** can be very useful for mobile sites, as it will attempt to bring up a keypad to make entering a phone number easier. Note that Tel will not attempt to validate the structure of a phone number, because there is too much variance in telephone format across the world.

You can check out the [full list of input types](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#input_types) on MDN.
