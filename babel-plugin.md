# babel-plugin-styled-wind

This plugin is a highly recommended supplement to the base [styled-wind](https://styled-wind.netlify.app/) library, offering some useful features:

- Use tailwind classnames in styled-components without using any additional dependencies
- Supports all features of [styled-wind](https://github.com/product-ride/styled-wind), but with no additional bundle size
- It works independently and doesnt require installing `styled-wind`

**Note:** For testing/playing around the tool, use the actual library. Use the `babel-plugin-styled-wind` only for production to avoid unnecssary configurations. If you are using `create-react-app`, you should `eject` before using it. 



## Quick start

Install the plugin first:

```
npm install --save-dev babel-plugin-styled-wind

or 

yarn add -D babel-plugin-styled-wind
```

Then add it to your babel configuration:

```JSON
{
  "plugins": ["babel-plugin-styled-wind"]
}
```

## Custom theming

> The configurations works very similar to tailwindcss with few exceptions. Details about configuring or extending the default theme object can be found [here](https://tailwindcss.com/docs/configuration)

* Create a file `styled-wind.js` in the root of your project and add custom styles in it. A sample implementation: 

```js
// styled-wind.js
module.exports = {
    theme: {
        extend: {
            colors: {
                cyan: '#9cdbff'
            },
        }
    }
}
```

As simple as that :)
