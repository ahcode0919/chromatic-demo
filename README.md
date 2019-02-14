# Chromatic Test Application

Chromatic Storybook testing demo. Uses React Create React App demo app.

## Project Setup

* Install Yarn - `brew install yarn`
* Install Storybook - `npx -p @storybook/cli sb init`

## Chromatic Setup

* Get Chromatic account
* Configure your project and get your app ID

## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.<br>
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

### `yarn test`

Launches the test runner in the interactive watch mode.<br>
Will also compare and update snapshots<br>

### `yarn run storybook`

Launches Storybook app on Port : 9009<br>

### `yarn chromatic -- --app-code="{app-code}" --do-not-start`

* Use `--do-not-start` if you already have storybook running locally
* `app-code` is the unique app code displayed on chromatic's website for your app
* Full command is: `./node_modules/.bin/chromatic test --app-code="{app-code}"`

### `yarn run build`

Builds the app for production to the `build` folder.<br>
It correctly bundles React in production mode and optimizes the build for the best performance.

## Notes

* Storybooks are based on [CDD - Component Driven Development](https://blog.hichroma.com/component-driven-development-ce1109d56c8e) and [Visual TDD](https://blog.hichroma.com/visual-test-driven-development-aec1c98bed87)
* Storybooks allow manual visual testing
* Snapshot testing verifies the generated HTML code for UI components
* Unit tests can be used to test specific logic with Jest and Enzyme
  * Note: "It's possible that as the project matures, and the exact implementation of the Task changes --perhaps using a different classname or a textarea rather than an input--the test will fail, and need to be updated. This is not necessarily a problem, but rather an indication to be careful liberally using unit tests for UI. They're not easy to maintain. Instead rely on visual, snapshot, and visual regression (see testing chapter) tests where possible"
* Visual tests are too manual, snapshot tests trigger too many false positives when used for UI, and pixel-level unit tests are poor value. A complete Storybook testing strategy also includes visual regression tests. Visual regression tests are designed to catch changes in appearance. They work by capturing screenshots of every story and comparing them commit-to-commit to surface changes. This is perfect for verifying graphical elements like layout, color, size, and contrast.


## Usage Notes

* Adding Storybook
  * `npx -p @storybook/cli sb init`
* Adding Snapshot testing
  * [StoryShots](https://github.com/storybooks/storybook/tree/master/addons/storyshots)
  * `yarn add --dev @storybook/addon-storyshots react-test-renderer require-context.macro`
* Adding Chromatic
  * `yarn add storybook-chromatic`
* Running Chromatic tests
  * `./node_modules/.bin/chromatic test --app-code="{app-code}"`
* Adding Knobs add-on
  * `yarn add @storybook/addon-knobs`

## Resources

- [Chromatic Guide](http://docs.chromaticqa.com/)
- [Create React App](https://github.com/facebook/create-react-app)
- [Jest](https://jestjs.io/) - Javascript testing framework
- [Storybook](https://storybook.js.org/) - UI development environment
- [Storybook Tutorial](https://www.learnstorybook.com/react/en/get-started/)
- [Storybook Documentation](https://storybook.js.org/basics/introduction/)
- [Storybook Add-ons](https://storybook.js.org/addons/addon-gallery/)
- [Storybook Knobs Add-on](https://github.com/storybooks/storybook/tree/master/addons/knobs#object)
