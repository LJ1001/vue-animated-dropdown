# Vue Animated Dropdown

This is an animated dropdown written in Vue.js based on the [Animated Dropdown Fireship Episode](https://www.youtube.com/watch?v=IF6k0uZuypA) (which is written in [React.js](https://github.com/fireship-io/229-multi-level-dropdown)).

The styling of components is made via [Tailwindcss](https://tailwindcss.com/). PurgeCSS is not configured so the production CSS file is pretty big.
Transitions are done via tailwind [helper classes](https://tailwindcss.com/docs/transition-property) or via the built in [Vue transition component](https://vuejs.org/v2/guide/transitions.html#Overview).

Some UI elements do not have the exact same styling as in the video but you could easily tweak the CSS values via the [tailwind config file](https://tailwindcss.com/docs/configuration/#apps).

## Build Setup

``` bash
# install dependencies
yarn install

# serve with hot reload at localhost:8080
yarn run dev
```
