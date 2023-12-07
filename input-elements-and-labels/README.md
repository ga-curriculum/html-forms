# ![Intermediate HTML - Input Elements and Labels](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to tktk


As we discussed above, `<form>` is a container element, designed to be filled with other elements. 

Let's introduce two of the most common of these elements now - `<input>` and `<textarea>`. 

The `<input>` element 




When creating a form, try to keep things simple and focused. While forms are often necessary to collect certain information, from a user's perspective entering a lot of data can be frustrating. 

Consider the following use-case: if we're building a basic contact form, what information do we actually need from the user? 

- We want to collect their name, so that we know how to refer to them in a reply. This will require an `<input>` element.
- We need their email address, so that we have the ability to reach back out to them. This will require an `<input>` element.
- Finally, we need to collect their message itself. This could use an `<input>` element, but for reasons discussed above is better suited to a `<textarea>` element.

Any other information we try to collect will likely feel unnecessary. Asking for the users age, or location, or the number of cats they have in their household etc. is not directly relevant, so inputs for this information should be omitted. 