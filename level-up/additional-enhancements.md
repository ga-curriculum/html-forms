# ![Intermediate HTML - Level Up - Additional Enhancements](./assets/hero.png)

## The datalist element

At first glance, `<datalist>` and `<select>` look very similar. Both wrap around a number of `<option>` elements and allow the user to select one from a dropdown. 

To better understand what makes them unique, you can think about a `<datalist>` as sort of a combination of a`<input type="text">` input and a `<select>` element. A `<datalist>`  has a set of predefined options, but also allows the user to input their own text and submit that instead. `<datalist>`'s also provide an auto-complete feature - as the user starts typing, any available options that match their text will show up as suggestions. 

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

Some other differences to note - 
