# saucectl cypress & typescript example

In this first step, we demonstrate that we can run our cypress tests either locally on our machine directly, or via sauce ctl. 

```
yarn test:cypress
```

To run directly


```
yarn test:saucelabs
```

To run via sauce labs. 

## Part 2

In this next part, I have added the [cypress testing library](https://testing-library.com/docs/cypress-testing-library/intro) extension. 

(I needed the rename the package to   `typescript-demo` as you get install errors trying to install   `typescript ` into  `typescript`).

You can see that the tests work fine when running directly, but when running via saucelabs it fails because it doesn't have access to the required dependencies. 

```
Error: Webpack Compilation Error
./cypress/support/commands.js
Module not found: Error: Can't resolve '@testing-library/cypress/add-commands' in '/home/seluser/__project__/cypress/support'
resolve '@testing-library/cypress/add-commands' in '/home/seluser/__project__/cypress/support'
  Parsed request is a module
  ```


  We can try manually remove `node_modules` from the `.sauceignore` but (works fine in this case, but in another scenario (monorepo) I have issues). 

  





Example running saucectl with cypress & typescript.

## What You'll Need

The steps below illustrate one of the quickest ways to get set up. If you'd like a more in-depth guide, please check out
our [documentation](https://docs.saucelabs.com/testrunner-toolkit/installation).

### Install `saucectl`

```shell
npm install -g saucectl
```

### Set Your Sauce Labs Credentials

```shell
saucectl configure
```

## Running The Examples

Simply check out this repo, navigate into `examples/typescript` and run the command below :rocket:

```bash
saucectl run
```

## The Config

[Follow me](.sauce/config.yml) if you'd like to see how saucectl is configured for this example.

**NOTE:**
Some examples were taken from the cypress.io testing [repository](https://github.com/cypress-io/cypress-example-kitchensink) 
