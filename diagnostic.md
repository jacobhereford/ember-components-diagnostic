# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components.

    ```md
    components that are within a route that is nested within a route
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember g component my-map   or   ember generate component my-map
    ```

1.  What files are edited to produce a component, and what are their
    responsibilities?

    ```md
    model, route, and template
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` path. What is
    the syntax for loading this component inside that template?

    ```html
    /contacts/my-contact
    ```

    Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    <h2>{{my-contact.title}}</h2>

    <ul>
      {{#each my-phone.items as |item|}}
      {{contact/my-contact/my-phone/item item=item}}
      {{/each}}
    </ul>
    ```
