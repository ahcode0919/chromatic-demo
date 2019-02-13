# Chromatic Test Application

Chromatic Storybook testing demo. Uses React Create React App demo app.

## Chromatic Docs

[Chromatic Guide](http://docs.chromaticqa.com/)

## Storybook

[Storybook](https://storybook.js.org/) - UI development environment
[Storybook Tutorial](https://www.learnstorybook.com/react/en/get-started/)
[Storybook Documentation](https://storybook.js.org/basics/introduction/)

## Test Runner

[Jest](https://jestjs.io/) - Javascript testing framework

## Project Setup
* Note: These have already been completed

* Install Yarn - `brew install yarn`
* Create test React Application - `npx create-react-app {root-directory}/`
* Install Storybook - `npx -p @storybook/cli sb init`

## Chromatic Setup

* Get Chromatic account

## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.<br>
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

### `yarn test`

Launches the test runner in the interactive watch mode.<br>

### `yarn run build`

Builds the app for production to the `build` folder.<br>
It correctly bundles React in production mode and optimizes the build for the best performance.

## Notes

* Storybooks are based on [CDD - Component Driven Development](https://blog.hichroma.com/component-driven-development-ce1109d56c8e) and [Visual TDD](https://blog.hichroma.com/visual-test-driven-development-aec1c98bed87)
* Storybooks allow manual visual testing
* Snapshot testing verifies the generated HTML code for UI components
* Unit tests can be used to test specific logic with Jest and Enzyme
  * Note: "It's possible that as the project matures, and the exact implementation of the Task changes --perhaps using a different classname or a textarea rather than an input--the test will fail, and need to be updated. This is not necessarily a problem, but rather an indication to be careful liberally using unit tests for UI. They're not easy to maintain. Instead rely on visual, snapshot, and visual regression (see testing chapter) tests where possible"

## Resources

- [Create React App](https://github.com/facebook/create-react-app)
