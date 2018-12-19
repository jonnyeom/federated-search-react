# Federated Search ReactJS app

This app renders search results from a Solr search index.  It was developed as the front end to the [search_api_federated_solr Drupal module](https://github.com/palantirnet/search_api_federated_solr#federated-solr-search-api-module).  Read the sections below to learn how to use this app.

## Requirements

- Node.js
- Yarn
- An Apache Solr server

### Node

You’ll need to have Node version 6 or greater on your local development machine. You can use [nvm](https://github.com/creationix/nvm#installation) (macOS/Linux) or [nvm-windows](https://github.com/coreybutler/nvm-windows#node-version-manager-nvm-for-windows) to easily switch Node versions between different projects.

### Yarn

Yarn is used instead of Node Package Manager (NPM) for package management and running commands.

[Yarn installation instructions](https://yarnpkg.com/en/docs/install)

### Apache Solr

This project depends on configuring a Solr search server. The server can exist locally or hosted.

Note: If you are hosting the search server at a different domain, you may need to configure CORS support for Apache Solr. If this is not configured correctly, you may get notices in the browser console and the results will not be returned. See [https://opensourceconnections.com/blog/2015/03/26/going-cross-origin-with-solr/](https://opensourceconnections.com/blog/2015/03/26/going-cross-origin-with-solr/) for some information on how that can be set up.

## Local setup

### Install dependencies

Run `yarn install` from the repo root.

### Configure the app

Create a `src/.env.local.js` configuration file.

You can copy the [src/.env.local.js.example](src/.env.local.js.example) example and edit the values provided.

### Start the development server

Run `yarn start` from the repo root to run the app in development mode.

It should automatically open http://localhost:3000 in a browser.

The page will automatically reload if you make changes to the code.
                                      
You will see the build errors and lint warnings in the console.

## Local testing

When you run the start script `yarn start`, code quality (linting) tests are automatically run and feedback is provided in the terminal.

## Code quality

### Linting

We recommend using linters to review your work.

ESLint is included and configured in `.eslintrc`.

Note that even if you edit your `.eslintrc` file further, these changes will **only affect the editor integration**. They won’t affect the terminal and in-browser lint output. This is because Create React App intentionally provides a minimal set of rules that find common mistakes.

#### Linting in an editor

Some editors, including Sublime Text, Atom, and Visual Studio Code, provide plugins for ESLint.

#### Linting in the console

You should see the linter output right in your terminal as well as the browser console.

## Theme the search app

TODO

## Use the app on your site

TODO

## Publishing releases

- Run `yarn build` to build the static assets and copy the `package.json` file into the `build/static` directory
- Run `yarn deploy` to push the contents of `build/static` to the `master` branch of this repository 
- Run `yarn deploy tag` to push the contents of `build/static` to the `master` branch and tag it with the version listed in `package.json` (be sure to bump as you see fit and commit that change before running this)

### Requiring this project as a dependency

Deploying this package produces production-ready JS and CSS files that can be referenced in a project as external dependencies. For example:

- CSS: `https://cdn.jsdelivr.net/gh/palantirnet/federated-search-react@v1.0.10/css/main.cf6a58ce.css`
- JS: `https://cdn.jsdelivr.net/gh/palantirnet/federated-search-react@v1.0.10/js/main.d41fc3fe.js`

To update the package, increment the version number AND hash for each file based on the current release.

## Additional documentation

This project was created with the [Create React App](https://github.com/facebook/create-react-app).

The original documentation is located at [/docs/README.create-react-app.md](/docs/README.create-react-app.md).
