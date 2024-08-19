## Description
This is a server side rendered component to Cradle CMS which will use data for an article.

## Setup steps

### 1. Add component file
Add file `article.liquid` to the `components` folder

### 2. JSON-article template
Add the article template `article.json.liquid` for JSON.

### 3. Include component code
Include the component code to the site with tag `{% component 'article' %}`. 
A good practise is to include all the components to the same file and when cached by the browser will decreate the payload of the site, this would be done by creating a js-file in assets where all components could be added.

### 4. Use component on site
Use the component at the desired place by including `<blog-article url="{{ 'articles/toc' | url }}"></blog-article>`, note that the URL contains the `articles` slug as it adds the context to the handle.
