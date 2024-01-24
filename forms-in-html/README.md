# ![Intermediate HTML - Forms in HTML](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will understand what forms are, and how to construct a basic form in HTML. 

## What are forms? 

If you've used the internet for more than a couple of minutes, you're likely already familiar with forms. Every time you've signed up for or signed into a website, every time you've 'googled' something - any time you've needed to enter text into a website to interact with it - you were using a form. 

Forms are one of the primary ways in which you will interact with user data as you develop applications. They are a crucial tool that allows us to collect data from users.  They also give users the ability to interact with the application's  interface - for instance, a form might hold checkboxes that control hiding or showing certain UI elements. 

## The form element

The `<form>` element represents a document section containing interactive controls for submitting information. `<form>` acts as a wrapper element for various other elements, which either offer structure to the form, or work as **controls** for the form itself. 

To create a form, we use the `<form>` container element: 

```html
<form>
  ...
</form>
```


The form element has a number of attributes that help to configure how the form will behave. All of these attributes are optional, but some of them like **action** and **method** are used on every form when working with sending form data to a server. 

```html
<form action="/my-page" method="post">
  ...
</form>
```

The `action` attribute defines the URL that the form's data is sent to when the form is submitted. 

The `method` attribute defines which HTTP method to send the data with. In the above example, the form data is being sent as a 'post' request.

As both a URL and an HTTP method are required to 'hit' a route, you'll almost always see both of these attributes on a form. 

For a more complete list of `<form>` attributes, check out [Form Attributes on MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form#attributes)