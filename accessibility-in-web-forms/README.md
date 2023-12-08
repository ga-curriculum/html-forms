# ![Intermediate HTML - Accessibility in Web Forms](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will understand 

## Accessibility pitfalls: misuse of the placeholder attribute

We're already covered the importance of attaching labels to inputs when working with web forms. A good way to emphasize this is to examine some of the pitfalls that come along with a commonly used alternative: placeholders. 

[tktk example of placeholders in front end design form]

While the visual minimalism can be tempting, placeholders should not be used in place of labels. 

Placeholders are attributes, which are skipped over by Browser translators. You can imagine why - if a browser started to translate code, the code would break. 

Labels wrap text which can be translated safely, but placeholder's inject text as code which is ignored during translation. 

This is especially difficult for users who struggle with recall.

[tktk example of password guidelines in input]

[tktk example of a DATE formatting placeholder]


Another consideration is that not every user has the same level of digital literacy. To some people, especially at a glance, placeholder text can make it look as though the input is not empty. This makes it very easy to skip certain inputs, and can lead to a frustrating

To help remedy a lot of these issues, placeholder content should be moved above the input, and below the label. This way, it can be referenced, translated, and we remove any ambiguity about if the input is empty or not. 

[tktk example of label, then input info, then an empty input field]

