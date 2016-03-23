# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    The router file specifies the url hierarchy of an ember project, an ember route file specifies what should be shown (but now how it should be show) on a specific page.
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
    ember generate route boston/campus
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
    The first route definition actually specifies two routes: products and products/:product_id. The second only specifies one: products/:product_id.

    
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
    According to the pattern we've been following, we would reference it with params.movie_id.
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    We use the keyword "model".
    ```
