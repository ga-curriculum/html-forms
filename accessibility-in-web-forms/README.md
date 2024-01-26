# ![HTML Forms - Accessibility in Web Forms](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will understand how labels and placeholders differ for accessibility. 

## Accessibility pitfall: misuse of the placeholder attribute

We've already discussed the accessibility benefits of labeling inputs when working with web forms. A good way to emphasize this is to examine some of the pitfalls that come along with a commonly used alternative: placeholders. 

[tktk Hunter example of placeholders in front end design form]

While the visual minimalism can be tempting, placeholders should not be used in place of labels.

The primary reason is that because placeholders are attributes, they are skipped over by Browser translators. `<label>` elements wrap text which can be translated safely, but placeholders inject text as code which is ignored during translation. You can imagine why - if a browser started to translate parts of code into other languages, the code itself would break. 

## Accessibility pitfall: vanishing instructions

When designing placeholders, it's important to think about how they affect **Cognitive Accessibility**. For individuals who struggle with recall, such as those with short-term memory loss or ADHD, placeholders can be tricky. As soon as a user starts typing in an input field, the placeholder text disappears, taking any hints or instructions with it. This can be challenging for users who may find it hard to remember what information the field requires.

[tktk Hunter example of password guidelines in input]

[tktk Hunter example of a DATE formatting placeholder]

When considering different levels of digital literacy among users, it's crucial to recognize that placeholder text might be misleading for some. To certain individuals, especially during a quick scan, an input field with placeholder text might appear already filled. This can unintentionally lead users to overlook these fields, potentially causing frustration when they realize they've missed entering necessary information.

To help remedy these issues, it's advisable to place any details about the content or requirements of an input field in a clear and accessible position. Ideally, this information should be situated above the input field itself and below its corresponding label. 

This way, it can be referenced, translated, and we remove any ambiguity about if the input is empty or not. 

[tktk Hunter example of label, then input info, then an empty input field]

