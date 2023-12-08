# ![Intermediate HTML - Accessibility in Web Forms](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to tktk

## Accessibility Concerns 

We're already covered the importance of labeling inputs when working with web forms. However, there are a few other important ways in which we can make our web forms more accessible. 

## ARIA roles

ARIA roles can be added to elements to tell assistive technologies how to best treat that element. Without them, it can be difficult to figure out the purpose of various elements on a page, which 

As a result, it's important to include a role attributes to elements on which it is not implicit. 

For example, `<input type="checkbox">` has an implicit ARIA role of "checkbox" by default. 

ARIA roles are added to HTML elements using role="role type", where role type is the name of a role in the ARIA specification.

The role attribute can provide semantics information, furthering the goals of semantic HTML. 




Overview of ARIA roles and attributes


## Accessibility pitfalls: misuse of the placeholder attribute


While the visual minimalism can be tempting, placeholders should not be used in place of labels. 

[tktk example of placeholders in front end design form]

Placeholders are attributes, which are skipped over by Browser translators. You can imagine why - if a browser started to translate code, the code would break. 

Labels wrap text which can be translated safely, but placeholder's inject text as code which is ignored during translation. 

This is especially difficult for users who struggle with recall.

[tktk example of password guidelines in input]

[tktk example of a DATE formatting placeholder]


Another consideration is that not every user has the same level of digital literacy. To some people, especially at a glance, placeholder text can make it look as though the input is not empty. This makes it very easy to skip certain inputs, and can lead to a frustrating



To help remedy a lot of these issues, placeholder content should be moved above the input, and below the label. This way, it can be referenced, translated, and we remove any ambiguity about if the input is empty or not. 

[tktk example]

