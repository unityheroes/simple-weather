# Simple Weather

تطبيق React صغير يعرض حالة الطقس الحالية لموقع محدد. تم بناؤه باستخدام Material UI وaxios وmoment وreact-i18next لدعم اللغات (بما في ذلك RTL للغة العربية).

## المميزات

- عرض اسم المدينة والتاريخ/الوقت الحالي
- عرض درجة الحرارة الحالية مع وصف الطقس والحد الأدنى/الأقصى
- أيقونات الطقس كبيرة باستخدام Material Icons
- دعم لغتيْن: العربية (RTL) والإنجليزية باستخدام `react-i18next`

## المتطلبات

- Node.js وnpm
- مفتاح API من OpenWeatherMap

## الإعداد السريع

1. استنساخ المشروع وتثبيت الحزم:

````bash
# Simple Weather

A small React weather-card app that displays current weather for a fixed location. Built with Material UI, Axios, moment.js and react-i18next for localization (including RTL support for Arabic).

## Features

- City name and current date/time
- Large temperature display with weather description and min/max
- Large weather icon (Material Icons)
- English and Arabic (RTL) support using `react-i18next`

## Requirements

- Node.js and npm
- An OpenWeatherMap API key

## Quick Setup

1. Clone the repository and install dependencies:

```bash
git clone <your-repo-url>
cd simple-weather
npm install
````

2. Environment variables (`.env`):

Create a `.env` file in the project root and add your OpenWeatherMap key:

```env
REACT_APP_OPENWEATHER_KEY=your_api_key_here
```

The app reads the key from `process.env.REACT_APP_OPENWEATHER_KEY`. If you have a hard-coded key in `src/App.js`, replace it to use the env variable.

3. Start the app:

```bash
npm start
```

Open http://localhost:3000

## State / Redux note

State is managed locally in components; Redux is not configured in this project.
If you want to add Redux quickly, run:

```bash
npm install @reduxjs/toolkit react-redux
```

Then create a basic `src/store.js`, wrap the app with `<Provider store={store}>` in `src/index.js`, and move shared state into slices using `@reduxjs/toolkit`.

## Customization & Future Improvements

- Make the displayed location (lat/lon) configurable via the UI
- Persist language or city preferences locally
- Improve error handling and loading states

## License

MIT
