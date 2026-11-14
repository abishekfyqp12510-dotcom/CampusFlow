# CampusFlow - Student Life Manager

CampusFlow helps students organise their academic life in one place. It works in the browser and can be installed on phones and computers like an app.

## Features

- **Dashboard**: today's classes, upcoming assignments, attendance and exam countdowns at a glance
- **Timetable**: weekly class schedule
- **Study planner**: plan study sessions and mark them done
- **Assignments**: track due dates and priorities
- **Attendance**: record classes and see your attendance percentage
- **Notes**: save notes by subject
- **Exams**: upcoming exams with a day countdown
- **Progress**: study completion and attendance statistics
- **Installable**: add to your home screen or desktop
- **Offline use**: works without an internet connection after the first visit

## Project files

| File | Purpose |
|------|---------|
| `index.html` | Page structure (login screen and app) |
| `style.css` | Colours, layout and responsive design |
| `app.js` | Logic: login, data storage and all pages |
| `manifest.json` | App name, colours and icons for installing |
| `sw.js` | Service worker for offline use |
| `icon-192.png`, `icon-512.png` | App icons |
| `README.md` | This file |

## Run it on your computer

Open the project folder in a terminal and run:

    python -m http.server 8000

Then open http://localhost:8000 in your browser.

Secure login requires either localhost or an https address. Opening `index.html` by double-clicking may not work for login.

## Install as an app

- **Android (Chrome):** menu (three dots), then **Install app**
- **iPhone (Safari):** Share button, then **Add to Home Screen**
- **Computer (Chrome or Edge):** install icon in the address bar, then **Install**

## Hosting

The app runs entirely in the browser. It can be hosted for free on GitHub Pages.

## Updating the app

When you change any app file, increase the version in `sw.js`:

    const CACHE_VERSION = 'campusflow-v3';

This makes installed copies download the new version.

## Data and privacy

- All data is stored in the browser's local storage on the device you use.
- Passwords are hashed with PBKDF2 and never stored in plain text.
- Data does not sync between devices or browsers.
- Clearing browser data deletes your CampusFlow data.
