# react-native-web-demo
1. First Create a /src folder and move App.js and app.json and create a html file.
2. Duplicate index.js to src/ folder, it will be the entry point of the web app
3. Rename index.js of the root (NOT the new file in src/) to index.native.js, it will be the entry point of the native app.
4. Update imports’ paths in index.native.js
5. The web-app doesn’t seem to support the example components of react-native/Libraries/NewAppScreen, so you have to remove these from src/App.js
6. You need to add runApplication() to src/index.js (the entry point of the web app) to load the web app correctly.
7. Add react-scripts, react-native-web, react-dom in package.json
8. To continue to run tests, you have to update references of _tests__/App-test.js
9. I have encountered some version conflicts about babel-jest and jest libraries, so you need to remove these from development dependencies of package.json. Don’t worry, they are dependencies of other packages, you can continue to run tests.
10. After, you may need to remove and re-install the node_modules
11. You need to add web task to package.json to run the web app {"web": "react-scripts start"}
