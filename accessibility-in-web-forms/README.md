# ![HTML Forms - Accessibility in Web Forms](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will understand how labels and placeholders differ. 

## Accessibility pitfalls: misuse of the placeholder attribute

We're already covered the accessibility benefits of labeling inputs when working with web forms. A good way to emphasize this is to examine some of the pitfalls that come along with a commonly used alternative: placeholders. 

[tktk example of placeholders in front end design form]

While the visual minimalism can be tempting, placeholders should not be used in place of labels.

One key reason is that, since placeholders are attributes, they are skipped over by Browser translators. You can imagine why - if a browser started to translate parts of code into other languages, the code itself would break. 

`<label>`'s wrap text which can be translated safely, but placeholder's inject text as code which is ignored during translation. 

Another consideration when working with placeholders involves possible impacts to your site's **Cognitive Accessibility**.

When a user enters any value into an input field, the placeholder text is replaced by this value. As a result, any instructions regarding what should go into that field are lost. 

This is especially difficult for users who struggle with recall, such as those with short term memory loss or ADHD.

[tktk example of password guidelines in input]

[tktk example of a DATE formatting placeholder]


A third consideration is that not every user has the same level of digital literacy. To some people, especially at a glance, placeholder text can make it look as though the input is not empty. This makes it very easy to skip certain inputs, and can lead to a frustrating

To help remedy a lot of these issues, any information about the subject of or requirements for an input should be moved above the input, and below the label. This way, it can be referenced, translated, and we remove any ambiguity about if the input is empty or not. 

[tktk example of label, then input info, then an empty input field]

