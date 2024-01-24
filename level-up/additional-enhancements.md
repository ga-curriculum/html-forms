# ![HTML Forms - Level Up - Additional Enhancements](./assets/hero.png)

## The datalist element

At first glance, `<datalist>` and `<select>` look very similar - both allow the user to select a number of `<option>` elements from a dropdown.

However, the `<datalist>` element is more like an associated list of options for an `<input>`, where `<select>` is a dropdown list of options in a form.

To better understand what makes them unique, you can think about `<datalist>` as sort of a combination of an `<input>` and a `<select>` element. A datalist is a set of predefined options associated with a text input, which allows the user to either select from the options or submit alternative text. 

One big benefit is that `<datalist>`'s also provide an auto-complete feature - as the user starts typing, any available options that match their text will show up as suggestions. Historically, adding auto-complete to an input required a decent amount of JavaScript, but with `<datalist>` we now get this behavior natively with HTML! 

```html
<label for="pet-choice">Choose a pet: </label>
<input list="pets" id="pet-choice" name="pet-choice" />

<datalist id="pets">
  <option value="dog"></option>
  <option value="cat"></option>
  <option value="fish"></option>
  <option value="rabbit"></option>
  <option value="hamster"></option>
  <option value="chinchilla"></option>
</datalist>
```

Note that, as with labels, the input is not wrapped 

In this instance, we provide some of the most popular pets as options in a `<datalist>`. These options are not an exhaustive list of all possible pets a user could have, but they are statistically the most likely answers (maybe aside from chinchilla). 

Using an input with a datalist means that we can hint at popular answers, but also leave the option for the user to enter something else. It also subtly points users towards using generic terms like "dog" or "fish", vs. entering specifics like "Golden Labradoodle" or "Peppermint Angelfish". 

`<select>` is more rigid, and strictly enforces possible inputs to a curated list of possible options. An `<input>` with an associated `<datalist>` offers selectable options and auto-complete, but should still be treated like an `<input>`. 