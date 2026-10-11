# Student Management System

A small, browser-only student directory built with React and Vite. Student data is kept in React state and is not saved to a backend or database.

## Requirements

- Node.js 18 or newer
- npm (included with Node.js)

## Install and run

Open a terminal in the project folder and run:

```powershell
npm ci
npm run dev
```

Open the local URL printed by Vite (usually `http://localhost:5173`).

## Create a production build

```powershell
npm run build
```

Vite writes the production-ready site to the `dist` folder. To preview that build locally:

```powershell
npm run preview
```

## Jenkins Freestyle Project on Windows

Install Node.js 18 or newer on the Jenkins agent and make sure `node` and `npm` are available on `PATH`. Configure the project checkout from GitHub, then add an **Execute Windows batch command** build step:

```bat
npm ci
if errorlevel 1 exit /b %errorlevel%
npm run build
if errorlevel 1 exit /b %errorlevel%
```

The generated website is in `dist`. The application has no backend or external UI-library dependencies.

## Project structure

```text
student-management-system/
├── index.html
├── package.json
├── package-lock.json
├── vite.config.js
├── .gitignore
├── README.md
└── src/
    ├── main.jsx
    ├── App.jsx
    ├── styles.css
    └── components/
        ├── StudentForm.jsx
        └── StudentTable.jsx
```
