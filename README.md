[![npm][npm]][npm-url]
[![node][node]][node-url]
[![deps][deps]][deps-url]
[![test][test]][test-url]
[![build][build]][build-url]
[![coverage][cover]][cover-url]

<div align="center">
  <a href="https://github.com/webpack/webpack"></a>
  <h1>Webpack</h1>
	<a href="https://npmjs.com/package/webpack">
		<img src="https://img.shields.io/npm/dm/webpack.svg">
	</a>
	<a href="https://opencollective.com/webpack#backer">
		<img src="https://opencollective.com/webpack/backers/badge.svg">
	</a>
	<a href="https://opencollective.com/webpack#sponsors">
		<img src="https://opencollective.com/webpack/sponsors/badge.svg">
	</a>
	<a href="https://gitter.im/webpack/webpack">
		<img src="https://img.shields.io/badge/gitter-webpack%2Fwebpack-brightgreen.svg">
	</a>
  <p>
    Webpack is a bundler for modules. The main purpose is to bundle JavaScript files for usage in a browser, yet it is also capable of transforming, bundling, or packaging just about any resource or asset.
  <p>
</div>

<h2 align="center">Install</h2>

```bash
npm i -D webpack
```

<h2 align="center">Introduction</h2>

webpack is a bundler for modules. The main purpose is to bundle JavaScript
files for usage in a browser, yet it is also capable of transforming, bundling,
or packaging just about any resource or asset.

**TL;DR**

* Bundles both [CommonJS](http://wiki.commonjs.org/) and [AMD](https://github.com/amdjs/amdjs-api/wiki/AMD) modules (even combined).
* Can create a single bundle or multiple chunks that are asynchronously loaded at runtime (to reduce initial loading time).
* Dependencies are resolved during compilation reducing the runtime size.
* Loaders can preprocess files while compiling, e.g. coffeescript to JavaScript, handlebars strings to compiled functions, images to Base64, etc.
* Highly modular plugin system to do whatever else your application requires.

### [Getting Started](https://webpack.github.io/docs/tutorials/getting-started)

Check out webpack's [docs](https://webpack.github.io/docs/?utm_source=github&utm_medium=readme&utm_campaign=trdr) for quick Getting Started guide, in-depth usage,
tutorials and resources.

<h2 align="center">Features</h2>

### [Plugins](https://webpack.github.io/docs/list-of-plugins.html)

webpack has a [rich plugin
interface](https://webpack.github.io/docs/plugins.html). Most of the features
within webpack itself use this plugin interface. This makes webpack very
**flexible**.

### [Loaders](https://webpack.github.io/docs/list-of-loaders.html)

webpack enables use of loaders to preprocess files. This allows you to bundle
**any static resource** way beyond JavaScript. You can easily [write your own
loaders](https://webpack.github.io/docs/loaders.html) using node.js.

Loaders are activated by using `loadername!` prefixes in `require()` statements,
or are automatically applied via regex from your webpack configuration.

Please see [Using Loaders](https://webpack.github.io/docs/using-loaders.html) for more information.

##### Files

|Name|Status|Description|
|:--:|:----:|:----------|
|[raw-loader][raw]|![raw-npm]|Loads raw content of a file (utf-8)|
|[val-loader][val]|![val-npm]|Executes code as module and consider exports as JS code|
|[url-loader][url]|![url-npm]|Works like the file loader, but can return a Data Url if the file is smaller than a limit|
|[file-loader][file]|![file-npm]|Emits the file into the output folder and returns the (relative) url|


[raw]: https://github.com/webpack/raw-loader
[raw-npm]: https://img.shields.io/npm/v/raw-loader.svg
[val]: https://github.com/webpack/val-loader
[val-npm]: https://img.shields.io/npm/v/val-loader.svg
[url]: https://github.com/webpack/url-loader
[url-npm]: https://img.shields.io/npm/v/url-loader.svg
[file]: https://github.com/webpack/file-loader
[file-npm]: https://img.shields.io/npm/v/file-loader.svg

#### Transpiling

|Name|Status|Description|
|:--:|:----:|:----------|
|<img width="64" height="64" title="babel-loader" src="https://worldvectorlogo.com/logos/babel-10.svg">|[![babel-npm]][babel]|Loads ES2015+ code and transpiles to ES5 using <a href="https://github.com/babel/babel">Babel</a>|
|<img width="64" height="64" src="https://google.github.com/traceur-compiler/logo/tc.svg">|![traceur-npm]|Loads ES2015+ code and transpiles to ES5 using [Traceur](https://github.com/google/traceur)|
|<img width="64" height="64" src="https://worldvectorlogo.com/logos/coffeescript.svg">|![coffee-npm]|Loads CoffeeScript like JavaScript|
|<img width="64" height="64" src="http://www.typescriptlang.org/assets/images/logo_nocircle.svg">|![type-npm]|Loads TypeScript like JavaScript|


[babel]: https://github.com/babel/babel-loader
[babel-npm]: https://img.shields.io/npm/v/babel-loader.svg

[traceur]: https://github.com/jupl/traceur-loader
[traceur-npm]: https://img.shields.io/npm/v/traceur-loader.svg

[coffee]: https://github.com/webpack/coffee-loader
[coffee-npm]: https://img.shields.io/npm/v/coffee-loader.svg

[type]: https://github.com/andreypopp/typescript-loader
[type-npm]: https://img.shields.io/npm/v/typescript-loader.svg


#### JSON

|Name|Status|Description|
|:--:|:----:|:----------|
|<img width="64" height="64" src="https://worldvectorlogo.com/logos/json.svg">|![json-npm]|Loads file as JSON|

[json]: https://github.com/webpack/json-loader
[json-npm]: https://img.shields.io/npm/v/json-loader.svg

#### Templating

|Name|Status|Description|
|:--:|:----:|:----------|
|<img width="64" height="64" src="https://worldvectorlogo.com/logos/html5.svg">|![html-npm]|Exports HTML as string, require references to static resources|
|<img width="64" height="64" src="https://cdn.rawgit.com/pugjs/pug-logo/eec436cee8fd9d1726d7839cbe99d1f694692c0c/SVG/pug-final-logo-_-colour-64.svg">|![pug-npm]|Loads Pug templates and returns a function|
|<img width="64" height="64" src="https://worldvectorlogo.com/logos/jade-3.svg">|![jade-npm]|Loads Jade templates and returns a function|
|<img width="64" height="64" src="https://worldvectorlogo.com/logos/markdown.svg">|![md-npm]|Compiles Markdown to HTML|
|<img width="64" height="64" src="http://posthtml.github.io/posthtml/logo.svg">|![posthtml-npm]|Loads and transforms a HTML file using [PostHTML](https://github.com/posthtml/posthtml)|
|<img width="64" height="64" src="https://worldvectorlogo.com/logos/handlebars-1.svg">|![hbs-npm]| Compiles Handlebars to HTML|

[html]: https://github.com/webpack/html-loader
[html-npm]: https://img.shields.io/npm/v/html-loader.svg

[pug]: https://github.com/pugjs/pug-loader
[pug-npm]: https://img.shields.io/npm/v/pug-loader.svg

[jade]: https://github.com/webpack/jade-loader
[jade-npm]: https://img.shields.io/npm/v/jade-loader.svg

[md]: https://github.com/peerigon/markdown-loader
[md-npm]: https://img.shields.io/npm/v/markdown-loader.svg

[posthtml]: https://github.com/posthtml/posthtml-loader
[posthtml-npm]: https://img.shields.io/npm/v/posthtml-loader.svg

[hbs]: https://github.com/altano/handlebars-loader
[hbs-npm]: https://img.shields.io/npm/v/handlebars-loader.svg

#### Styling

|Name|Status|Description|
|:--:|:----:|:----------|
|<img width="64" height="64" src="https://worldvectorlogo.com/logos/style.svg">|![style-npm]|Add exports of a module as style to DOM|
|<img width="64" height="64" src="https://worldvectorlogo.com/logos/css-3.svg">|![css-npm]|Loads CSS file with resolved imports and returns CSS code|
|<img width="64" height="64" src="https://worldvectorlogo.com/logos/less-63.svg">|![less-npm]|Loads and compiles a LESS file|
|<img width="64" height="64" src="https://worldvectorlogo.com/logos/sass-1.svg">|![sass-npm]|Loads and compiles a SASS/SCSS file|
|<img width="64" height="64" src="https://worldvectorlogo.com/logos/stylus.svg">|![stylus]|Loads and compiles a Stylus file|
|<img width="64" height="64" src="https://worldvectorlogo.com/logos/postcss.svg">|![postcs-npm]|Loads and transforms a CSS/SSS file using [PostCSS](http://postcss.org)|

[style]: https://github.com/webpack/style-loader
[style-npm]: https://img.shields.io/npm/v/style-loader.svg

[css]: https://github.com/webpack/css-loader
[css-npm]: https://img.shields.io/npm/v/css-loader.svg

[less]: https://github.com/webpack/less-loader
[less-npm]: https://img.shields.io/npm/v/less-loader.svg

[sass]: https://github.com/jtangelder/sass-loader
[sass-npm]: https://img.shields.io/npm/v/sass-loader.svg

[stylus]: https://github.com/shama/stylus-loader
[stylus-npm]: https://img.shields.io/npm/v/stylus-loader.svg

[postcss]: https://github.com/postcss/postcss-loader
[postcss-npm]: https://img.shields.io/npm/v/postcss-loader.svg

#### Linting && Testing

|Name|Status|Description|
|:--:|:----:|:----------|
|<img width="64" height="64" src="https://worldvectorlogo.com/logos/mocha.svg">|![mocha-npm]|Tests with mocha (Browser/NodeJS)|
|<img width="64" height="64" src="https://worldvectorlogo.com/logos/eslint.svg">|![eslint-npm]|PreLoader for linting code using ESLint|
|<img width="64" height="64" src="http://jshint.com/res/jshint-dark.png">|![jshint-npm]|PreLoader for linting code using JSHint|
|<img width="64" height="64" src="https://worldvectorlogo.com/logos/jscs.svg">|![jscs-npm]|PreLoader for code style checking using JSCS|

[mocha]: https://github.com/webpack/mocha-loader
[mocha-npm]: https://img.shields.io/npm/v/mocha-loader.svg

[eslint]: https://github.com/MoOx/eslint-loader
[eslint-npm]: https://img.shields.io/npm/v/eslint-loader.svg

[jshint]: https://github.com/webpack/jslint-loader
[jshint-npm]: https://img.shields.io/npm/v/jslint-loader.svg

[jscs]: https://github.com/unindented/jscs-loader
[jscs-npm]: https://img.shields.io/npm/v/jscs-loader.svg


#### Frameworks

|Name|Status|Description|
|:--:|:----:|:----------|
|<img width="64" height="64" src="https://worldvectorlogo.com/logos/vue-9.svg">|![vue-npm]|Loads an compiles Vue Components|
|<img width="64" height="64" src="https://worldvectorlogo.com/logos/polymer.svg">|![polymer-npm]|Process HTML & CSS with preprocessor of choice and `require()` Web Components like first-class modules|
|<img width="64" height="64" src="https://worldvectorlogo.com/logos/angular-icon-1.svg">|![angular-npm]| Loads and compiles Angular 2 Components|

[vue]: https://github.com/vue/vue-loader
[vue-npm]: https://img.shields.io/npm/v/vue-loader.svg

[polymer]: https://github.com/JonDum/polymer-loader
[polymer-npm]: https://img.shields.io/npm/v/polymer-loader.svg

[angular]: https://github.com/TheLarkInn/angular2-template-loader
[angular-npm]: https://img.shields.io/npm/v/angular2-template-loader.svg

### Performance

webpack uses async I/O and has multiple caching levels. This makes webpack fast
and incredibly **fast** on incremental compilations.

### Module Formats

webpack supports ES2015+, CommonJS and AMD modules **out of the box**. It performs clever static
analysis on the AST of your code. It even has an evaluation engine to evaluate
simple expressions. This allows you to **support most existing libraries** out of the box.

### [Code Splitting](https://webpack.github.io/docs/code-splitting.html)

webpack allows you to split your codebase into multiple chunks. Chunks are
loaded asynchronously at runtime. This reduces the initial loading time.

### [Optimizations](https://webpack.github.io/docs/optimization.html)

webpack can do many optimizations to **reduce the output size of your
JavaScript** by deduplicating frequently used modules, minifying, and giving
you full control of what is loaded initially and what is loaded at runtime
through code splitting. It can also make your code chunks **cache
friendly** by using hashes.

<h2 align="center">Example</h2>

```js
// webpack is a module bundler.
// This means webpack takes modules with dependencies
// and emits static assets representing those modules.

// Dependencies can be written in CommonJS
var commonjs = require("./commonjs");
// or in AMD
define(["amd-module", "../file"], function (amdModule, file) {
	// while previous constructs are sync,
	// this is async
	require(["big-module/big/file"], function (big) {
		 // For async dependencies, webpack splits
		 // your application into multiple "chunks".
		 // This part of your application is
		 // loaded on demand (code-splitting).
		var stuff = require("../my/stuff");
		// "../my/stuff" is also loaded on-demand
		//  because it's in the callback function
		//  of the AMD require.
	});
});


require("coffee!./cup.coffee");
// "Loaders" are used to preprocess files.
// They can be prefixed in the require call
// or configured in the configuration.
require("./cup");
// This does the same when you add ".coffee" to the extensions
// and configure the "coffee" loader for /\.coffee$/

function loadTemplate (name) {
	return require("./templates/" + name + ".jade");
	// Many expressions are supported in require calls.
	// A clever parser extracts information and concludes
	// that everything in "./templates" that matches
	// /\.jade$/ should be included in the bundle, as it
	// can be required.
}


// ...and you can combine everything.
function loadTemplateAsync (name, callback) {
	require(["bundle?lazy!./templates/" + name + ".jade"],
	  function (templateBundle) {
	          templateBundle(callback);
	});
}
```

<h2 align="center">Contributing</h2>

Most of the time, if webpack is not working correctly for you it is a simple configuration issue.

If you are still having difficulty after looking over your configuration carefully, please post
a question to [StackOverflow with the webpack tag](http://stackoverflow.com/tags/webpack). Questions
that include your webpack.config.js and relevant files are more likely to receive responses.

If you have discovered a bug or have a feature suggestion, feel free to create an issue on Github.

If you create a loader or plugin, please consider open sourcing it, putting it
on NPM and following the `x-loader`, `x-plugin` convention.

You are also welcome to correct any spelling mistakes or any language issues.

If you want to discuss something or just need help, [here is our gitter.im room](https://gitter.im/webpack/webpack).

<h2 align="center">Backers</h2>
<a href="https://opencollective.com/webpack#backer">Become a backer</a>

This is a free-time project. The time I invest in it fluctuates. If you use webpack for a serious task, and you'd like me to invest more time on it, please donate. This project increases your income/productivity too. It makes development and applications faster and it reduces the required bandwidth.

Another way you can help fund Webpack is by buying the ebook ["SurviveJS - Webpack"](https://leanpub.com/survivejs-webpack), where around ~30% of the book's profit will go to me.

I'm very thankful for every dollar. If you leave your username or email, I may show my thanks by giving you extra support.

<br>
<br>
<a href="https://opencollective.com/webpack/backer/0/website" target="_blank"><img src="https://opencollective.com/webpack/backer/0/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/1/website" target="_blank"><img src="https://opencollective.com/webpack/backer/1/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/2/website" target="_blank"><img src="https://opencollective.com/webpack/backer/2/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/3/website" target="_blank"><img src="https://opencollective.com/webpack/backer/3/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/4/website" target="_blank"><img src="https://opencollective.com/webpack/backer/4/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/5/website" target="_blank"><img src="https://opencollective.com/webpack/backer/5/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/6/website" target="_blank"><img src="https://opencollective.com/webpack/backer/6/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/7/website" target="_blank"><img src="https://opencollective.com/webpack/backer/7/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/8/website" target="_blank"><img src="https://opencollective.com/webpack/backer/8/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/9/website" target="_blank"><img src="https://opencollective.com/webpack/backer/9/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/10/website" target="_blank"><img src="https://opencollective.com/webpack/backer/10/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/11/website" target="_blank"><img src="https://opencollective.com/webpack/backer/11/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/12/website" target="_blank"><img src="https://opencollective.com/webpack/backer/12/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/13/website" target="_blank"><img src="https://opencollective.com/webpack/backer/13/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/14/website" target="_blank"><img src="https://opencollective.com/webpack/backer/14/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/15/website" target="_blank"><img src="https://opencollective.com/webpack/backer/15/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/16/website" target="_blank"><img src="https://opencollective.com/webpack/backer/16/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/17/website" target="_blank"><img src="https://opencollective.com/webpack/backer/17/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/18/website" target="_blank"><img src="https://opencollective.com/webpack/backer/18/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/19/website" target="_blank"><img src="https://opencollective.com/webpack/backer/19/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/20/website" target="_blank"><img src="https://opencollective.com/webpack/backer/20/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/21/website" target="_blank"><img src="https://opencollective.com/webpack/backer/21/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/22/website" target="_blank"><img src="https://opencollective.com/webpack/backer/22/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/23/website" target="_blank"><img src="https://opencollective.com/webpack/backer/23/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/24/website" target="_blank"><img src="https://opencollective.com/webpack/backer/24/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/25/website" target="_blank"><img src="https://opencollective.com/webpack/backer/25/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/26/website" target="_blank"><img src="https://opencollective.com/webpack/backer/26/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/27/website" target="_blank"><img src="https://opencollective.com/webpack/backer/27/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/28/website" target="_blank"><img src="https://opencollective.com/webpack/backer/28/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/29/website" target="_blank"><img src="https://opencollective.com/webpack/backer/29/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/30/website" target="_blank"><img src="https://opencollective.com/webpack/backer/30/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/31/website" target="_blank"><img src="https://opencollective.com/webpack/backer/31/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/32/website" target="_blank"><img src="https://opencollective.com/webpack/backer/32/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/33/website" target="_blank"><img src="https://opencollective.com/webpack/backer/33/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/34/website" target="_blank"><img src="https://opencollective.com/webpack/backer/34/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/35/website" target="_blank"><img src="https://opencollective.com/webpack/backer/35/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/36/website" target="_blank"><img src="https://opencollective.com/webpack/backer/36/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/37/website" target="_blank"><img src="https://opencollective.com/webpack/backer/37/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/38/website" target="_blank"><img src="https://opencollective.com/webpack/backer/38/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/39/website" target="_blank"><img src="https://opencollective.com/webpack/backer/39/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/40/website" target="_blank"><img src="https://opencollective.com/webpack/backer/40/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/41/website" target="_blank"><img src="https://opencollective.com/webpack/backer/41/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/42/website" target="_blank"><img src="https://opencollective.com/webpack/backer/42/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/43/website" target="_blank"><img src="https://opencollective.com/webpack/backer/43/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/44/website" target="_blank"><img src="https://opencollective.com/webpack/backer/44/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/45/website" target="_blank"><img src="https://opencollective.com/webpack/backer/45/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/46/website" target="_blank"><img src="https://opencollective.com/webpack/backer/46/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/47/website" target="_blank"><img src="https://opencollective.com/webpack/backer/47/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/48/website" target="_blank"><img src="https://opencollective.com/webpack/backer/48/avatar.svg"></a>
<a href="https://opencollective.com/webpack/backer/49/website" target="_blank"><img src="https://opencollective.com/webpack/backer/49/avatar.svg"></a>

<h2 align="center">Sponsors</h2>

Become a sponsor and get your logo on our README on Github with a link to your site. [Become a sponsor](https://opencollective.com/webpack#sponsor)

![Sponsors](https://opencollective.com/webpack/sponsors/badge.svg)

<a href="https://opencollective.com/webpack/sponsor/0/website" target="_blank"><img src="https://opencollective.com/webpack/sponsor/0/avatar.svg"></a>
<a href="https://opencollective.com/webpack/sponsor/1/website" target="_blank"><img src="https://opencollective.com/webpack/sponsor/1/avatar.svg"></a>
<a href="https://opencollective.com/webpack/sponsor/2/website" target="_blank"><img src="https://opencollective.com/webpack/sponsor/2/avatar.svg"></a>
<a href="https://opencollective.com/webpack/sponsor/3/website" target="_blank"><img src="https://opencollective.com/webpack/sponsor/3/avatar.svg"></a>
<a href="https://opencollective.com/webpack/sponsor/4/website" target="_blank"><img src="https://opencollective.com/webpack/sponsor/4/avatar.svg"></a>
<a href="https://opencollective.com/webpack/sponsor/5/website" target="_blank"><img src="https://opencollective.com/webpack/sponsor/5/avatar.svg"></a>
<a href="https://opencollective.com/webpack/sponsor/6/website" target="_blank"><img src="https://opencollective.com/webpack/sponsor/6/avatar.svg"></a>
<a href="https://opencollective.com/webpack/sponsor/7/website" target="_blank"><img src="https://opencollective.com/webpack/sponsor/7/avatar.svg"></a>
<a href="https://opencollective.com/webpack/sponsor/8/website" target="_blank"><img src="https://opencollective.com/webpack/sponsor/8/avatar.svg"></a>
<a href="https://opencollective.com/webpack/sponsor/9/website" target="_blank"><img src="https://opencollective.com/webpack/sponsor/9/avatar.svg"></a>
<a href="https://opencollective.com/webpack/sponsor/10/website" target="_blank"><img src="https://opencollective.com/webpack/sponsor/10/avatar.svg"></a>
<a href="https://opencollective.com/webpack/sponsor/11/website" target="_blank"><img src="https://opencollective.com/webpack/sponsor/11/avatar.svg"></a>
<a href="https://opencollective.com/webpack/sponsor/12/website" target="_blank"><img src="https://opencollective.com/webpack/sponsor/12/avatar.svg"></a>
<a href="https://opencollective.com/webpack/sponsor/13/website" target="_blank"><img src="https://opencollective.com/webpack/sponsor/13/avatar.svg"></a>
<a href="https://opencollective.com/webpack/sponsor/14/website" target="_blank"><img src="https://opencollective.com/webpack/sponsor/14/avatar.svg"></a>
<a href="https://opencollective.com/webpack/sponsor/15/website" target="_blank"><img src="https://opencollective.com/webpack/sponsor/15/avatar.svg"></a>
<a href="https://opencollective.com/webpack/sponsor/16/website" target="_blank">
<img src="https://opencollective.com/webpack/sponsor/16/avatar.svg">
</a>
<a href="https://opencollective.com/webpack/sponsor/17/website" target="_blank"><img src="https://opencollective.com/webpack/sponsor/17/avatar.svg"></a>
<a href="https://opencollective.com/webpack/sponsor/18/website" target="_blank"><img src="https://opencollective.com/webpack/sponsor/18/avatar.svg"></a>
<a href="https://opencollective.com/webpack/sponsor/19/website" target="_blank"><img src="https://opencollective.com/webpack/sponsor/19/avatar.svg"></a>

<h2 align="center">Maintainers</h2>

<table>
  <tbody>
   <tr>
    <td align="center">
      <img width="150 height="150"
      src="https://avatars.githubusercontent.com/u/1365881?v=3&s=150">
      <br />
      <a href="https://github.com/sokra">Tobias Koppers</a>
    </td>
		<td align="center">
      <img width="150 height="150"
      src="https://avatars.githubusercontent.com/u/166921?v=3&s=150">
      <br />
      <a href="https://github.com/bebraw">Juho Vepsäläinen</a>
    </td>
		<td align="center">
      <img width="150 height="150"
      src="https://avatars.githubusercontent.com/u/3408176?v=3&s=150">
      <br />
      <a href="https://github.com/TheLarkInn">Sean Larkin</a>
    </td>
		<td align="center">
      <img width="150 height="150"
      src="https://avatars.githubusercontent.com/u/781746?v=3&s=150">
      <br />
      <a href="https://github.com/jhnns">Johannes Ewald</a>
    </td>
   </tr>
  <tbody>
</table>

<h2 align="center">Thanks to</h2>
<p align="center">(In chronological order)</p>

* @google for [Google Web Toolkit (GWT)](https://code.google.com/archive/p/google-web-toolkit), which aims to compile Java to JavaScript. It features a similar [Code Splitting](http://www.gwtproject.org/doc/latest/DevGuideCodeSplitting.html) as webpack.
* @medikoo for [modules-webmake](https://github.com/medikoo/modules-webmake), which is a similar project. webpack was born because I wanted Code Splitting for modules-webmake. Interestingly the [Code Splitting issue is still open](https://github.com/medikoo/modules-webmake/issues/7) (thanks also to @Phoscur for the discussion).
* @substack for [browserify](http://browserify.org/), which is a similar project and source for many ideas.
* @jrburke for [require.js](http://requirejs.org/), which is a similar project and source for many ideas.
* @defunctzombie for the [browser-field spec](https://gist.github.com/defunctzombie/4339901), which makes modules available for node.js, browserify and webpack.
* Every early webpack user, which contributed to webpack by writing issues or PRs. You influenced the direction...
* @shama, @jhnns and @sokra for maintaining this project
* Everyone who has written a loader for webpack. You are the ecosystem...
* Everyone I forgot to mention here, but also influenced webpack.

[npm]: https://img.shields.io/npm/v/webpack.svg
[npm-url]: https://npmjs.com/package/webpack

[node]: https://img.shields.io/node/v/webpack.svg
[node-url]: https://nodejs.org

[test]: https://img.shields.io/travis/webpack/webpack/master.svg
[test-url]: https://travis-ci.org/webpack/webpack

[build-url]: https://ci.appveyor.com/project/sokra/webpack/branch/master
[build]: https://ci.appveyor.com/api/projects/status/github/webpack/webpack?svg=true

[cover]: https://img.shields.io/coveralls/webpack/webpack.svg
[cover-url]: https://coveralls.io/r/webpack/webpack/

[deps]: https://img.shields.io/david/webpack/webpack.svg
[deps-url]: https://david-dm.org/webpack/webpack

[deps-dev]: https://david-dm.org/webpack/webpack/dev-status.svg
[deps-dev-url]: https://david-dm.org/webpack/webpack#info=devDependencies

[deps-peer]: https://david-dm.org/webpack/webpack/peer-status.svg
[deps-peer-url]: https://david-dm.org/webpack/webpack#info=peerDependencies
