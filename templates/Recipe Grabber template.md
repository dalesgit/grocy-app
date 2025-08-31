---
tags: 
- recipe 
created: {{datePublished}}
author: {{author.name}}
url: {{url}} 
---

# [{{{name}}}]({{url}})

{{{description}}}

![{{{name}}}]({{image}})

# Ingredients

{{#each recipeIngredient}}
- {{{this}}}
{{/each}}

# Directions

{{#each recipeInstructions}}
{{#if this.itemListElement}}
#### {{{this.name}}}
{{#each this.itemListElement}}
- {{{this.text}}}
{{/each}}
{{else if this.text}}
- {{{this.text}}}
{{else}}
- {{{this}}}
{{/if}}
{{/each}}

-----

## Notes
