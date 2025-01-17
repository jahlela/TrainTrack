## TrainTrack

[![Netlify Status](https://api.netlify.com/api/v1/badges/56e7dcca-dca3-4516-bfec-a1fead6ee773/deploy-status)](https://app.netlify.com/sites/train-track/deploys)

Keeping the world on track with _TrainTrack_!

## Setup

Install `netlify` client:

```
npm install netlify-cli -g
```

## Babel/webpack compilation

All functions are compiled with webpack using the Babel Loader, so you can use modern JavaScript, import npm modules, etc., without any extra setup.

## Local Development

Before developing, clone the repository and run `yarn` from the root of the repo to install all dependencies.

### Run the functions dev server

From inside the project folder, run:

```
yarn start:lambda
```

This will open a local server running at `http://localhost:9000` serving your Lambda functions, updating as you make changes in the `src/lambda` folder.

You can then access your functions directly at `http://localhost:9000/{function_name}`, but to access them with the app, you'll need to start the app dev server.

### Run the app dev server

While the functions server is still running, open a new terminal tab and run:

```
yarn start
```

This will start the normal create-react-app dev server and open your app at `http://localhost:3000`.

Local in-app requests to the relative path `/.netlify/functions/*` will automatically be proxied to the local functions dev server.
