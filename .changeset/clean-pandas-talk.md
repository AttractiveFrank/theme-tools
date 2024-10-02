---
'@shopify/theme-language-server-common': minor
'theme-check-vscode': minor
---

Add Liquid tag snippet completion

- Accept the completion item for `if` and get `{% if condition %}\n  \n{% endif %}` with tabulated placeholders
- Accept the completion item for `render` and get `{% render 'snippet' %}`
- The snippets are smart depending on context:
    - Will infer whitespace stripping characters based on context
    - Will not snippet complete `{%` and `%}` if inside a `{% liquid %}` tag
    - Will not snippet complete if markup is already present in the tag definition
