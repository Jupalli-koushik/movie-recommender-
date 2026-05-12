# Getting Started with Create React App

## Skill Application Write-up

To complete the movie recommender, I applied React by decomposing the interface into small, reusable components and coordinating them with state and props. The App component serves as the controller. It tracks the search query, selected movie, movie list, debounce timer, and error message with useState so the view reacts to data changes.

I built a debounced search handler that clears the previous timer and triggers the OMDb API call after a short delay, which demonstrates event handling and keeps network traffic efficient while the user types. Axios manages the asynchronous requests, and I wrapped the calls in try/catch blocks to surface friendly errors when the API returns no results or a request fails.

Rendering is data driven: when results exist, MovieComponent cards are mapped from the response, and when results are empty a placeholder image is shown. Selecting a movie updates state with the imdbID. MovieInfoComponent responds through useEffect by fetching detailed metadata for that id. It illustrates conditional rendering by showing a loading state until data arrives. It then presents structured fields such as rating, year, language, and plot. I passed callbacks through props for selection and close actions, maintaining one-way data flow and a predictable state model.

Styling is handled with styled components, which let me define layout, spacing, and typography next to each component and build consistent flexbox sections like the header, search bar, and movie grid. I also used a controlled input, clear iconography, and a responsive list layout so the interface stays approachable as results change.

Overall, the project clearly demonstrates core React skills, including functional components, hooks, controlled inputs, state management, and composition. It pairs those skills with external API integration to deliver a responsive browsing experience. This approach emphasizes clarity, reuse, and maintainability while keeping the user experience fast and intuitive throughout.

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
