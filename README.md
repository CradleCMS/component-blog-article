## Server side rendered component
This is a server side rendered component to Cradle CMS article data in JSON format.

## Setup steps

### 1. Add component file
Add file `article.liquid` to the `components` folder. 

### 2. JSON-article template
Add the article template `article.json.liquid` for JSON.

### 3. Include component code
Include the component code to the site with tag `{% component 'article' %}`, this tag can be included directly to the site but then **need `script` tags added**.

A good practise to dcrease the payload and utilize the browser cache is to include all the components to the same js-file in `assets` folder and include in the theme with `{{ 'components.js.liquid' | asset_url | script_tag }}`.

### 4. Use component on site
Use the component at the desired place by including `<blog-article url="{{ 'articles/toc' | url }}"></blog-article>`, the URL contains the `articles` slug as it adds the article-context to the handle.
