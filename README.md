# react-app-without-framework

## Commits
1. Initialize the project
    * Create a repo on GitHub, I use SSH
    * `git clone git@github.com:USER-NAME/REPOSITORY-NAME.git`
        * cd into REPOSITORY-NAME
            * `git remote -v`
            * Should see
                * origin  git@github.com:USER-NAME:git_test.git (fetch)
                * origin  git@github.com:USER-NAME:git_test.git (push) 
	    * Initialize the project with `npm init` to add the package.json file
	    * Add a .gitignore file in the project root
	    * exclude the following
	        * node_modules
	        * dist
2. Add static assets
    * Add public directory to the project root
        * Add a index.html file in public which is used by React to render the app
        * See this commit to see contents of the index.html file
3. Add Babel
    * `npm i --save-dev @babel/core @babel/cli @babel/preset-env @babel/preset-react`
    * Create a .babelrc file in the project root
    * Add what is in the below bullet point to the file and save
        * { "presets": ["@babel/env", "@babel/preset-react"] }
4. Add Webpack
    * `npm i --save-dev webpack webpack-dev-server style-loader css-loader babel-loader`
    * Create a webpack.config.js file in the project root
    * See this commit to see the contents of the webpack.config.js file
5. Add React setup
    * `npm i react react-dom`
    * Create a src directory in the project root
    * In that src directory, create a containers folder
    * In the containers directory, create an app folder
    * In the app folder, add the following files
        * Add a index.js file
        * Add a App.js file
        * Add a App.css file
    * See this comment to see the contents of each of the three files above
    * Place webpack-dev-server --mode development in the npm script in the package.json file
        * "scripts": { "start": "webpack-dev-server --mode development" }
    * CLI for webpack must be installed
        * webpack-cli https://github.com/webpack/webpack-cli
        * Use `npm` to install the CLI via `npm i -D webpack-cli`
    * Test
        * `npm start`
        * copy/paste `http://localhost:3000/` into a web browser URL box, press enter and you should see Hello World!
        * cmd+option+j to check for any errors before committing

- - -

## Final project structure

* .
* +-- node_modules
* +-- public
    * +- index.html
* +-- src
    * +-- containers
        * +-- app
            * +-- App.css
            * +-- App.js
            * +-- index.js
* +-- .babelrc
* +-- .gitignore
* +-- package-lock.json
* +-- package.json
* +-- webpack.config.json
