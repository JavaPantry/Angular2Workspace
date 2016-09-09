#Experiment with `webpack`

- Chapter 10 of Angular_2_Development_with_TypeScript_v7_MEAP.pdf
- Additional guide https://webpack.github.io/docs/usage.html
	
	> npm install webpack -g
	
- search github for `webpack.config.js`
- [vilhelmfalkenmark/react-todo](https://github.com/vilhelmfalkenmark/react-todo)
- At the time of this writing the Angular team is working on Angular CLI (see [Angular CLI](https://github.com/angular/angular-cli) ), which is a
command line interface for automating the application creation,
testing, and deployment. You should check it out when released.
The Angular team is working on supporting Webpack in Angular
CLI.
- run `npm init` to init directory
- install webpack server `npm install webpack webpack-dev-server --save-dev`
- include  webpack-dev-server in _package.json_

    {
      "name": "play_webpack",
      "version": "1.0.0",
      "description": "play room",
      "main": "main.js",
      "dependencies": {
    					"webpack": "^1.13.2",
    					"webpack-dev-server": "^1.15.1"
    					  },
      "devDependencies": {
    					"webpack": "^1.13.2",
    					"webpack-dev-server": "^1.15.1"
    					  },
      "scripts": {
    "test": "webpack --watch",
    "start": "webpack-dev-server"
      },
      "author": "",
      "license": "ISC"
    }

    

- include  webpack-dev-server in _webpack.config.js_

    `
    const path = require('path');
    //const webpack = require('webpack');
    module.exports = {
        entry: "./main",
        output: {
            path: './dist',
            filename: 'bundle.js'
        },
        watch: true,
        devServer: {
            contentBase: '.'
        }
    };
    `

- now we can run webpack server `npm start`

- add loaders to config [list of webpack loaders](https://github.com/webpack/docs/wiki/list-of-loaders)
- install transpiler `npm install ts-loader --save-dev`
- install `npm install css-loader style-loader --save-dev`
- install `npm install html-loader --save-dev` 
- install `npm install raw-loader --save-dev`

    `
    loaders: [
    {test: /\.css$/, loader: 'to-string!css', exclude: /node_modules/}, //Exclude CSS files located in the directory node_modules
    {test: /\.css$/, loader: 'style!css', exclude: /src/}, //Inline the third-party CSS files located in node_modules.
    {test: /\.html$/, loader: 'raw'}, //Transform the content of each .html file into a string
    {test: /\.ts$/, loader: 'ts'} //Transpile each .ts file using ts-loader
    ]
    `

- _tslint_ preloader to check errors, readability and maintainability 

    `
    preLoaders: [
     {
     test: /\.ts$/,
     exclude: /node_modules/,
     loader: "tslint"
     }
     ]`


