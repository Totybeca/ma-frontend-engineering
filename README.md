0x03. ES6 data manipulation
Resources
Read or watch:

array

Typed array

Set Data Structure

Map Data Structure

[Weak Map](https://developer.mozilla.org/en-The Set, Map, and Weak link data structuresUS/docs/Web/JavaScript/Reference/Global_Objects/Map)

Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

How to use map, filter and reduce on arrays

Typed arrays

The Set, Map, and Weak link data structures

Requirements
All your files will be executed on Ubuntu 18.04 LTS using NodeJS 12.11.x Allowed editors: vi, vim, emacs, Visual Studio Code All your files should end with a new line A README.md file, at the root of the folder of the project, is mandatory Your code should use the js extension Your code will be tested using Jest and the command npm run test Your code will be verified against lint using ESLint Your code needs to pass all the tests and lint. You can verify the entire project running npm run full-test All of your functions must be exported

Setup
Install NodeJS 12.11.x
Install Jest, Babel, and ESLint
in your project directory:

Install Jest using: npm install --save-dev jest Install Babel using: npm install --save-dev babel-jest @babel/core @babel/preset-env Install ESLint using: npm install --save-dev eslint

Configuration files
package.json
{ "scripts": { "lint": "./node_modules/.bin/eslint", "check-lint": "lint [0-9].js", "dev": "npx babel-node", "test": "jest", "full-test": "./node_modules/.bin/eslint [0-9].js && jest" }, "devDependencies": { "@babel/core": "^7.6.0", "@babel/node": "^7.8.0", "@babel/preset-env": "^7.6.0", "eslint": "^6.4.0", "eslint-config-airbnb-base": "^14.0.0", "eslint-plugin-import": "^2.18.2", "eslint-plugin-jest": "^22.17.0", "jest": "^24.9.0" } }

babel.config.js
module.exports = { presets: [ [ '@babel/preset-env', { targets: { node: 'current', }, }, ], ], };

.eslintrc.js
module.exports = { env: { browser: false, es6: true, jest: true, }, extends: [ 'airbnb-base', 'plugin:jest/all', ], globals: { Atomics: 'readonly', SharedArrayBuffer: 'readonly', }, parserOptions: { ecmaVersion: 2018, sourceType: 'module', }, plugins: ['jest'], rules: { 'max-classes-per-file': 'off', 'no-underscore-dangle': 'off', 'no-console': 'off', 'no-shadow': 'off', 'no-restricted-syntax': [ 'error', 'LabeledStatement', 'WithStatement', ], }, overrides:[ { files: ['*.js'], excludedFiles: 'babel.config.js', } ] };

and…
Don’t forget to run $ npm install when you have the package.json

License
[ALX_Africa]
