
## Intro to Webpack (https://www.freecodecamp.org/news/an-intro-to-webpack-what-it-is-and-how-to-use-it-8304ecdc3c60/)
* Webpack is a static module bundler and makes sure the browser understands all the code.
* It puts all the dependent code into a bundle.js file that can easily be plugged into the app.
* To begin run 'npm init' to create a starter package and add a package.json file
* For react we need to run 'npm i react react-dom --save'
* Next we add webpack so we can bundle the app together by running 'npm i webpack webpack-dev-server webpack-cli --save--dev'
* We also will need babel to translate es6 code by running 'npm i babel-core babel-loader @babel/preset-react @babel/preset-env html-webpack-plugin --save-dev'
* Once the installs are complete, add a webpack.config.js file in the root directory of the app and add the following code:
const path = require('path');const HtmlWebpackPlugin = require('html-webpack-plugin');
module.exports = {  //This property defines where the application starts  entry:'./src/index.js',
 //This property defines the file path and the file name which will be used for deploying the bundled file  output:{    path: path.join(__dirname, '/dist'),    filename: 'bundle.js'  },
  //Setup loaders  module: {    rules: [      {        test: /\.js$/,         exclude: /node_modules/,        use: {          loader: 'babel-loader'        }      }    ]  },
  // Setup plugin to use a HTML file for serving bundled js files plugins: [    new HtmlWebpackPlugin({      template: './src/index.html'    })  ]}

  * Now you can write react code in the app.js file
  * Adding these two scripts will enable auto reloads
  "start": "webpack-dev-server --mode development --open --hot",
  "build": "webpack --mode production"
  * now run 'npm start' to start the dev server and serve the html in the browser

## Webpack Concepts (https://webpack.js.org/concepts/)
To get started with webpack you need to understand these:
* An Entry Point shows which module webpack should use to begin building its internal dependency graph. By default it is ./src/index.js, but you can set an 'entry' property in the webpack configuration
* The Output property tells webpack where to emit the bundles it creates and how to name these files. it defaults to ./dist/main.js for the main output file and to the ./dist folder for any other generated file.
* To start webpack only understands JavaScript and JSON files. Loaders allow webpack to process other types of files. They have two properties, 'test' identifies which files should be transformed, 'use' indicates which loader should be used to do the transforming.
* Plugins can be used to perform a wider range of tasks like bundles optimization, asset management and injection of environment variables.
* By setting the Mode parameter to either development, production, or none you can enable webpacks built in optimization that corresponds to each environment. the default is production.
* Webpack supports all browsers that are ES5 compliant, and needs Promise for import() and require.ensure(). To use with older browsers you will need to load a polyfill before using the expressions.

## rendering elements
* React manages what is inside the root DOM node.
* to render a react element into a root dom node, pass both to ReactDOM.render()
* react elements are immutable, and its children can not be changed, the only way to update it is to create a new element and pass it to ReactDOM.render()
* When something changes, react only updates the changes and leaves the rest the same
* thinking about how the ui should look at a given point in time reduces bugs

## react hello world(https://reactjs.org/docs/hello-world.html)
* The smallest react example looks like this:
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);

## introducing JSX(https://reactjs.org/docs/introducing-jsx.html)
* JSX looks like html and can be saved into variables like: const name = <h1>Jim</h1>
* Javascript can be added into JSX within {}
* You can also use JSX inside if statements and for loops
* You can use quotes to specify string literals
* you can also use {} to embed a javascript expression in an attribute
* it uses camel case for naming
* tags can be auto closed with />
* it is safe to embed user input in jsx
* babel compiles jsx down to React.createElement() calls