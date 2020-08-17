# gatsby-plugin-no-javascript

Removes all javascript files created by Gatsby from the static HTML files. This plugin does **NOT** remove all javascript, but only the
javascript that Gatsby is adding to the page.

:warning: The Gatsby javascript is only removed from the production build `gatsby build` and not during the dev build `gatsby develop`.
If you do not write any state logic or event handlers then this should not effect you. This feature may be something this plugin wants to
tackle in the future.

## How to install

`npm install mcagalj/gatsby-plugin-no-javascript` or `yarn add mcagalj/gatsby-plugin-no-javascript`

:warning: This plugin should be included last in your `gatsby-config.js` as it relies on [onPreRenderHTML](https://www.gatsbyjs.org/docs/ssr-apis/#onPreRenderHTML)
`replaceHeadComponents` and `replacePostBodyComponents`.
