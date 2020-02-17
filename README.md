# gatsby-plugin-why-did-you-render

Include the [@welldone-software/why-did-you-render](https://github.com/welldone-software/why-did-you-render) library when running `gatsby develop`.


## Before You Continue

This plugin can be replicated by adding `@welldone-software/why-did-you-render` as a dependency, and adding the
following code to your `gatsby-browser.js`:

```js
import React from 'react'

export const onClientEntry = () => {
  if (process.env.NODE_ENV !== 'production') {
    const whyDidYouRender = require('@welldone-software/why-did-you-render')
    whyDidYouRender(React, {
      trackAllPureComponents: true
    })
  }
}
```

You're probably better off doing that and retaining more control of the version of WDYR that gets installed. However, if
you want to continue...

## Installation

Using npm:

```
npm i gatsby-plugin-why-did-you-render
```

Using yarn:

```
yarn add gatsby-plugin-why-did-you-render
```

## How To Use

```
// In your gatsby-config.js
module.exports = {
  plugins: ['gatsby-plugin-why-did-you-render']
};
```

