# Dr. Kristofor Kalvig — Podiatry Website

## Overview
A static marketing website (plain HTML/CSS/vanilla JS, no build tools) for a podiatry practice, plus an optional Node/Express backend for emailing contact-form submissions.

## Project Structure
- `index.html`, `about.html`, `procedures.html`, `insurance.html`, `contact.html` — static pages
- `css/styles.css` — stylesheet
- `js/script.js` — mobile nav toggle + form handling (contact/newsletter forms submit via Web3Forms API directly, not the local backend)
- `assets/images/` — site images
- `server/` — standalone Express backend (`index.js`, `sendEmail.js`) that can send contact-form emails via Outlook/Microsoft 365 SMTP (nodemailer). Not currently called by the frontend, which uses Web3Forms instead.

## Running in Replit
- `Start application` workflow: `node static-server.js` serves the static site on `0.0.0.0:5000` (webview).
- `Email Backend` workflow: `cd server && PORT=3001 node index.js` runs the optional Express email backend on port 3001 (console). Requires `EMAIL_USER`, `APPPASSWORD`, `EMAIL_RECIPIENT` env vars to actually send email (see `.env.example`); works fine without them since the frontend doesn't call it.

## User preferences
None recorded yet.
