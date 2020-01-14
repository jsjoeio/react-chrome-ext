# react-chrome-ext

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app) but 2 key differences have been made, specific for Chrome Extensions:

1. The `manifest.json` in the `public` directory has been modified to match that of a Chrome Extension. You can read more here: [manifest file format](https://developer.chrome.com/extensions/manifest)

2. Per Chrome's [Content Security Policy](https://developer.chrome.com/extensions/contentSecurityPolicy#JSExecution), inline JavaScript will not be executed. Therefore, the `build` script has been modified in the `package.json` to include the variable `INLINE_RUNTIME_CHUNK=false` as per suggested in [create-react-app's advanced configuration doc](https://facebook.github.io/create-react-app/docs/advanced-configuration).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.<br>
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br>
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.<br>
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.<br>
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br>
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (Webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

## Testing Chrome Extension Locally

If you'd like to test your extension locally before pushing to the Chrome Web Store, follow these steps:

1. `npm run build`
2. Open Chrome and navigate to [chrome://extensions/](chrome://extensions/)
3. In the top right, toggle 'Developer Mode' on
4. On the left side, click 'Load unpacked'
5. Select the `build` directory in your project and click upload

You should see your app's icon appear 😃

[Example demo video](https://res.cloudinary.com/jsjoeio/video/upload/v1543765905/chrome-ext-demo.mp4)

## Publish to Chrome Web Store

When you're ready to share you extension with the world, follow the Chrome Developer Docs [here](https://developer.chrome.com/webstore/get_started_simple#step6).

### Helpful  Resources
- [Automate your Chrome Extension deployment in minutes](https://dev.to/gokatz/automate-your-chrome-extension-deployment-in-minutes-48gb)!
