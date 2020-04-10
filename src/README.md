# Overview

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## TOC

<!-- toc -->

- [Set up](#set-up)
- [Testing](#testing)
- [Deployment](#deployment)
- [Learn More](#learn-more)

<!-- tocstop -->

## Set up

### Install dependencies

```bash
npm ci
```

> If you're on MacOS and seeing `node-gyp` issues, follow [this guide](https://github.com/nodejs/node-gyp/blob/master/macOS_Catalina.md) to troubleshoot

### Run App

> Note
>
> The app is using default port 3000. If you want to run this on a different port, you'll have to make changes to quite a few places

1. The page will reload if you make edits.
1. You will also see any lint errors in the console.

```bash
npm start
echo http://localhost:3000 # open to view in browser
```

## Testing

We're using [cypress](https://www.cypress.io/) for testing.

There's a pipeline set up to run against pr that will test against the following browsers

> Safari is currently [not supported in Cypress](https://github.com/cypress-io/cypress/issues/6422)

- edge (both Mac & Windows)
- chrome
- firefox
- electron

To test against the browser you want, run

```bash
npm run test:<BROWSER_NAME>
```

> See [package.json](package.json) for available npm scripts.

### Debugging

If your tests are failing and you need to debug, run `cypress` in debug mode

1. Modify the `cy:run:debug` script in [package.json](package.json) to the browser you want. It is using `chrome` by default
2. Run

   ```bash
   npm run test:debug
   ```

## Linting

I would recommend you install the [ESLint extension](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) for `VsCode` to lint and fix style issues. The validation pipeline will also do this and will block on PR merge.

The rules are specified [here](.eslintrc.js).

## Deployment

App deployment is done through an AzDO pipeline, the configuration is defined [here](../devops/pipelines/deploy-web-app.yaml)

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

<details>

<summary> Expand to see more </summary>
### Code Splitting

This section has moved here: <https://facebook.github.io/create-react-app/docs/code-splitting>

### Analyzing the Bundle Size

This section has moved here: <https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size>

### Making a Progressive Web App

This section has moved here: <https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app>

### Advanced Configuration

This section has moved here: <https://facebook.github.io/create-react-app/docs/advanced-configuration>

### Deployment

This section has moved here: <https://facebook.github.io/create-react-app/docs/deployment>

### `npm run build` fails to minify

This section has moved here: <https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify>

</details>
