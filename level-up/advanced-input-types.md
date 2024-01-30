# ![HTML Forms - Level Up - Advanced Input Types](./assets/advanced-input-types.png)

**Learning objective:** By the end of this lesson, students will be able to identify and utilize various advanced HTML input types.

There are over twenty different input types that are available, each with distinct behaviors. An `<input>` with the `type="checkbox"` attribute, for example, creates a single check box that toggles between selected and deselected. Some input types like `type="data"` create entire data pickers!

Let's look at some examples. Add the following form to `index.html`: 

```html
<form>
  <input type="text" />
  <input type="checkbox" />
  <input type="date" />
  <input type="color" />
  <input type="password" />
  <input type="tel" />
</form>
```

Open the page in the browser and experiment with each input. You'll see that while they are all `<input>`'s, the behavior of each type of input varies wildly.

- **Date** is a useful type due to how commonly users will format a date string incorrectly. Using a time/date picker helps to ensure the date is always expressed in the same order.

- **Color** is similarly useful as many users will not be familiar with RGB or Hexadecimal codes, and adding a visual component will help many users in selecting the color they want for an input.

- **Password** is similar to text, but has the added benefit of obscuring the value as it is being entered.

- **Tel** can be very useful for mobile sites, as it will attempt to bring up a keypad to make entering a phone number easier. Note that Tel will not attempt to validate the structure of a phone number, because there is too much variance in telephone format across the world.

You can check out the [full list of input types](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#input_types) on MDN.