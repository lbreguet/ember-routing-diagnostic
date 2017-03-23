# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    The main tasks you perform inside the Ember Application Router is define the
    the different routes of the application and also the different paths. Inside
    an Ember Route you define the data being passed through to that route/url.
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
    ember g route campus/boston
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
    {{#link-to 'campus/boston'}}Boston{{/link-to}}
    ```

1.  Explain **at least** two differences between the following two route
    definitions.

    ```js
    this.route('products', function () {
      this.route('product', { path: '/:product_id' }); // <= 👀here
    });

    this.route('product', { path: '/products/:product_id' }); // <= 👀 here
    ```

    ```md
    In the first example, the path 'product' is nested inside 'products', while
    in the second it isn't but uses data from 'products' to define the
    appropriate route.
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
    We would reference the value '123' inside a route by defining a paramater
    id.
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    {{#each model as |student|}}
    {{student.name}}
    {{/each}}
    ```
