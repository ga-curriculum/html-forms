# ![Intermediate HTML - Forms in HTML](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will understand what forms are, and how to construct a basic form in HTML. 

## What are forms? 

If you've used the internet for more than a couple of minutes, you'll likely  already be familiar with forms. Every time you've signed up for or signed into a website, every time you've 'googled' something - any time you've needed to enter text into a website to interact with it - you were using a form. 

Forms are one of the primary ways in which you will interact with user data as you develop applications. They are a crucial tool that allows us to collect data from users, data which can be sent to a server for storage or used to generate results to send back to the user. 

Forms can also give users the ability to interact with the application's  interface - for instance, a form might hold checkboxes that control hiding or showing certain UI elements. 

## The form element

The <form> element represents a document section containing interactive controls for submitting information. <form> acts as a wrapper element for various other elements, which either offer structure to the form, or work as **controls** for the form itself. 

To create a form: 

```html
<form>

</form>
```

## Creating a simple form

When creating a form, try to keep things simple and focused. While forms are often necessary to collect certain information, from a user's perspective entering a lot of data can be annoying or frustrating. 

Consider the following use-case: if we're building a basic contact form, what information do we actually need from the user? 

- We want to collect their name, so that we know how to refer to them in a reply. 
- We need their email address, so that we have the ability to reach back out to them. 
- Finally, we need to collect their message itself. 

Any other information we try to collect will likely seem unnecessary. Asking for the users age, or location, or the number of cats they have in their household etc. is not directly relevant, so inputs for this information should be omitted. 