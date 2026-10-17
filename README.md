# HeatWise India ☀️

A heat-aware outdoor day planner that turns live hourly weather into practical timing suggestions for walks, errands, sports, commuting and outdoor work.

## Features
- Search Indian cities with Open-Meteo Geocoding; optional browser location after an explicit tap.
- Live hourly forecast: temperature, apparent temperature, humidity, UV and precipitation probability where available.
- Transparent 0–100 planning heuristic and suggested lower-score time windows.
- Activity planner, local saved list, and simple on-page break reminders.
- Responsive UI; no login, backend, API key or database required.

## Run / test / build
Requirements: Node.js 18+ and npm.
```bash
npm install
npm test
npm run dev
npm run build
npm run preview
```

## GitHub + Vercel
1. Create a GitHub repo, extract this folder, then run `git init`, `git add .`, `git commit -m "Build HeatWise India"`.
2. Add your remote: `git remote add origin https://github.com/YOUR-USERNAME/heatwise-india.git`
3. Push: `git branch -M main && git push -u origin main`.
4. Import the repo into Vercel. Select Vite, build command `npm run build`, output directory `dist`. No environment variables are required.

## Privacy & data
Weather queries go to Open-Meteo. Activity names and reminder preference are saved in browser localStorage on this device. Geolocation is requested only when the user taps “Use my location”. No project-owned server, analytics, or account system is included. Avoid putting sensitive personal information in task names.

## Safety and limitations
The score is a product heuristic, not a certified heat index, clinical risk assessment, or official heat warning. Forecasts can change; refresh before acting and follow local public-health guidance. Individual risk varies with age, health, medication, clothing, shade and activity intensity. Prototype reminders are on-page prompts only, not push notifications. Review Open-Meteo usage terms before commercial deployment.

## Structure
- `src/main.js`: UI, API calls and interactions
- `src/logic.js`: score and time-window functions
- `src/style.css`: responsive design
- `tests/logic.test.js`: unit tests using Node's built-in runner

## 90-second demo
1. Search Ahmedabad (10s); 2. show current conditions and hourly score (20s); 3. compare windows for an evening walk (25s); 4. save activity and show local reminders (20s); 5. explain privacy and the non-official score caveat (15s).
