# Flip panel for Vue

## description

An animated panel that flips between front and back. Made for VueJs. It uses two slots: "front" and "back".

Example of template:
```html
<template>
    <flip-panel class="flip-panel">
        <template slot="front">
          <h3>Default settings</h3>
          <p>
            Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, ...
          </p>
        </template>
        <template slot="back">
          <h3>Back</h3>
          <p>
            Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem. Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur
          </p>
        </template>
    </flip-panel>
</template>
```
You can put any html or (framework) component in one of the slots.

The component itself has no formatting. Use properties to add/remove "shadow", "border", "rounded corners". See the properties table for an overview of the properties.

The component is based on this article [Intro to CSS 3D Transforms: Card Flip]https://3dtransforms.desandro.com/card-flip)
