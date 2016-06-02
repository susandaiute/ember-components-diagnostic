# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components.

    ```md
    Site Name
      First Section Title
        Stuff in First Section
          SubStuff
          SubStuff
        More Stuff in First Section
      Second Section Title
        Stuff in Second Section

    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember g component my-map
    ```

1.  What files are edited to produce a component, and what are their
    responsibilities?

    ```md
    A component produces a component.js file and a template.hbs file.  The template file is where routes can be linked together and where the visual structure of the component will be built using handlebars.  The component file is where properties and behaviors can be added to the component.
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` path. What is
    the syntax for loading this component inside that template?

    ```html
    {{#each contacts.my-contact as |contact|}}
      {{contact.content}}
    {{/each}}
    ```

    Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{#each contact.my-phone as |phone|}}
      {{contact.phone}}
    {{/each}}
    ```
