# Heroku Buildpack for webpack

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for web applications that use webpack.

## Usage

The `bin/compile` script run webpack with the production configuration file (`webpack.prod.js` in your main directory). To use the buildpack:

1. Specify our buildpack as the priorized one, for now:

   ```bash
   $ heroku buildpacks:set https://github.com/floored/heroku-buildpack-webpack
   ```

2. Add the `heroku/nodejs` buildpack back at `index=1`:

  ```bash
  $ heroku buildpacks:add --index 1 heroku/nodejs
  ```

3. Deploy a new version of your app to Heroku.
