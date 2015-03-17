# YARSK

**Y**et **A**nother **R**eact **S**tarter **K**it.

Everyone has one, here's mine.

## Features

* [React](http://facebook.github.io/react/), of course.
* [Webpack](http://webpack.github.io/) for asset bundling.
* [React hot loader](https://github.com/gaearon/react-hot-loader) enabled out of the box. Changes to React components will show in the browser immediately without a full reload.
* [Babel](https://babeljs.io/) for ES6+ transpilation.
* [SASS](http://sass-lang.com/) and [Autoprefixer](https://github.com/postcss/autoprefixer) enabled by default through Webpack.
* [Karma](http://karma-runner.github.io/0.12/index.html) + [Mocha](http://mochajs.org/) for testing. [Istanbul](https://gotwarlost.github.io/istanbul/) and [isparta](https://github.com/douglasduteil/isparta) are also activated with `karma-coverage` for code coverage analysis, even on your ES6 classes. See [Testing](https://github.com/bradleyboy/yarsk#tests) below for more info.
* Production configuration for the most optimized file size possible with React. The bundled JS file produced from this example is less than 40KB minified and gzipped. See [Building](https://github.com/bradleyboy/yarsk#building) below for more info.

This kit is intentionally missing a specific Flux implementation, or any other non-essential library, as I use this as a base for experimenting with various parts of the React ecosystem.

## Usage

Fork this repo, then run:

```
npm install
npm run serve
```

That will fire up a webpack dev server in **hot** mode. Most changes will be reflected in the browser automatically without a browser reload. You can view the app in the browser at `http://localhost:8080`.

## Building

To generate a production build, run:

```
npm run build
```

The above command will generate a `dist` folder with the appropriate index.html file along with the minified CSS and JS files.

You can also automatically publish to GitHub pages. Just run this instead of the regular build command:

```
npm run build:gh
```

You can then view your app at `http://[yourgithubusername].github.io/[reponame]`. For example, you can load this demo at http://bradleyboy.github.io/yarsk.

## Tests

The tests use Karma, Mocha and Chai through PhantomJS. See the example test in `app/Application/__tests__/index.js`. The test suite can be run like so:

```
npm test
```

To run the tests in watch mode (tests will re-run each time a file changes), use this instead:

```
npm run test:watch
```

You can generate code coverage reports with:

```
npm run test:coverage
```

See the `coverage` directory once that command is completed.

Finally, the repo is [Travis](https://travis-ci.org) ready. The `.travis.yml` file should work out of the box, just add your repo in Travis.