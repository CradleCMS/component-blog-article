## Blog article data component

Web component for Cradle CMS fetching article data in JSON format.

## Setup steps

### 1. Add component file
Add the file `article.liquid` to the `components` folder. 

### 2. JSON-article template
Add a article template `article.json.liquid` in folder `templates` for JSON output with the following content:
```
{% layout 'none' %}
{{ article | json | unescape }}
```

### 3. Include component code
Include the component code to the site with tag `{% component 'article' %}`.

A good practise to dcrease the payload and utilize the browser cache is to include all the components to the same js-file in `assets` folder and include in the theme with `{{ 'components.js.liquid' | asset_url | script_tag }}` but please note that one should **remove the script tags in the js-component file `article.liquid`**.

### 4. Use component on site

Use the component at the desired place by including `<blog-article>` as html tag and the url article containing the `articles` slug. 

```
<blog-article url="{{ '<article handle with articles slug>' | url }}"></blog-article>
```

The URL contains the `articles` slug as it adds the article-context to the handle.
