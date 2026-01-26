# Simple Weather

A small React weather-card app that displays current weather for a fixed location. Built with Material UI, Axios, moment.js and react-i18next for localization (including RTL support for Arabic).

## Features

- City name and current date/time
- Large temperature display with weather description and min/max
- Large weather icon (Material Icons)
- English and Arabic (RTL) support using `react-i18next`

## Libraries / Stack

- React (Create React App)
- Material UI (`@mui/material`, `@mui/icons-material`)
- axios
- moment
- i18next / react-i18next

## Project files (important)

- `src/App.js` — main UI and data fetching
- `src/i18n.js` — i18next initialization
- `src/index.js` — imports `src/i18n` before mounting `App`

## Setup

1. Clone the repository and install dependencies:

```bash
git clone <your-repo-url>
cd simple-weather
npm install
```

2. OpenWeatherMap API key:

- This project calls OpenWeatherMap in `src/App.js` using an `appid` query parameter. Replace the existing key with your own, or add an environment variable (recommended):

```env
REACT_APP_OPENWEATHER_KEY=your_api_key_here
```

Then update the request URL in `src/App.js` to use `process.env.REACT_APP_OPENWEATHER_KEY`.

3. Start the app:

```bash
npm start
```

Open http://localhost:3000

## Localization / RTL

- `src/i18n.js` initializes translations and is imported in `src/index.js`.
- Use the language toggle in the UI to switch between Arabic and English. The layout direction updates accordingly.

## Troubleshooting

- If you get `i18n.changeLanguage is not a function`, ensure `src/i18n.js` is imported before `App` (see `src/index.js`).
- If translations fail, check `public/locales/` or the backend used by `i18next-http-backend`.

## Customization

- Change the lat/lon in `src/App.js` to display another city.
- Move inline styles to CSS files for finer control.

## Next improvements (optional)

- Move API key to `.env` and use `process.env`.
- Add unit tests and linting.
- Make the location configurable via UI.

## License

MIT

---

If you want, I can update the code to read the API key from `.env` and remove the hard-coded key from `src/App.js`.
