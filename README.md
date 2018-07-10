[![CircleCI](https://circleci.com/gh/pozetroninc/qrbarco_de-frontend.svg?style=svg&circle-token=320161206f9cfe0e9078e58e6d58a5819d064d63)](https://circleci.com/gh/pozetroninc/qrbarco_de-frontend)

# QRBarco.de Frontend
This is the Vue.js Frontend for the qrbarco.de website. The backend can be found on the `qrbarco_de` branch of the [pozetron-barcode-service ](https://github.com/pozetroninc/pozetron-barcode-service/tree/qrbarco_de)

## Quickstart

Install Dependencies

    npm install


Configure app

    cp app.config.example.json app.config.json

    nano app.config.json


Then, run development server (on `http://localhost:8080`)

    npm run serve


Or, create production build (into a `dist/` directory)

    npm run build


Or, run tests

    npm run test:unit


## App configuration (`app.config.json`)

| Key                      | Type     | Description     |
| :---                     | :---     | :---            |
| **DEV_QRCODE_SERVICE**   | Required | Full URL of the backend barcode service for dev environements  |
| **PROD_QRCODE_SERVICE**  | Required | Full URL of the backend barcode service for production environements  |
| **RECAPTCHA_SITE_KEY**   | Optional | Google reCaptcha v3 site key. If provided, automatically enables recaptcha checks |
| **SENTRY_API_URL**       | Optional | Full URL of Sentry API. If provided, automatically enables error monitoring with sentry     |
| **GITHUB_LINK**          | Optional | Github repository link for the "Fork me on Github" ribbon |

## Styling configuration (`app.sass.config.json`)

The `app.sass.config.json` file provides styling configs that are available in both js and sass code.

| Key                      | Type     | Description     |
| :---                     | :---     | :---            |
| **COLOR_SCHEMES**        | Required | Extends Bulma's colors with new ones which can be used anywhere css classes like Bulma's `.is-info` are useful. Note this should be an object (not a list) |
