# Lansing Codes

Static site with events and resources for Lansing coders

## Build Setup

### Build Pre-reqs

This project requires node and npm.

1. [Node.js](https://nodejs.org/en/) Javascript framework
2. [NPM](https://www.npmjs.com/) Dependency management
   1. During the build process, you may need additional system dependencies such as python2 or C build tools. See the [Build Issues](https://github.com/lansingcodes/www#build-issues) section if you run into an error while building `node-sass`.


### Build Process

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm run test
```

## Deployments

After a pull request is reviewed and merged to `master`, a Netlify deployment
will automatically build and publish the staging environment at
[lansingcodes-staging.netlify.com](https://lansingcodes-staging.netlify.com).

Once the staging environment has been reviewed, the `master` branch can be
promoted to the `production` branch with the following command:

``` sh
git fetch origin && git push --force origin origin/master:production
```

This will trigger another build and deployment by Netlify. The site will be
published to [www.lansing.codes](https://www.lansing.codes).

For both the staging and production sites, Netlify runs the command
`npm run build` to build the site and deploys the contents of the `/dist`
directory.

Staging is also configured to deploy _all_ branches, so creating a
pull request should create a temporary site where the changes can be previewed
before merging to `master`. Click on the _Details_ link next to the site check
labeled "netlify/lansingcodes-staging/deploy-preview" to see a live preview of
your changes.

The primary Humanity Codes account has administrator access to both Netlify
sites. Additional administrators can be added by invitation only.

## Want more?

For detailed explanation on how things work, check out the [guide](https://github.com/vuejs-templates/webpack#vue-webpack-boilerplate) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
