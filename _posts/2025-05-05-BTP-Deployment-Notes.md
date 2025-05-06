---
layout:     post
title: 「Web App」Bus Trip Planner (Web) Deployment Notes
date:       2025-05-05 12:00:00
author:     "LPZhang"
catalog: false
header-style: text
tags: 
  - Vercel
  - React
  - Web
---

## Bus Trip Planner (Web) Deployment Notes

### Deployment
Front-end Repo: https://github.com/pricezhang42/Commute-Compass-Vercel
Back-end Repo: https://github.com/pricezhang42/Commute-Compass-Backend

The backend server won't work locally using "vercel dev" but it's able to run when deployed online.

Tutorial for the deployment of node.js server with Vercel:
https://vercel.com/guides/using-express-with-vercel

Tutorial for the deployment of frontend:
https://blog.logrocket.com/deploy-react-app-for-free-using-vercel/

Vercel CLI was used for both backend and frontend.

To deploy frontend: 
Go to the repo -> run commands:
`vercel`
_Note_: Deployment on Vercel Projects Page won't work due to permission deny.

### Debugging
Front-end app (the web) built with **React** can be debugged with the built-in developer tool (F12) in browser.

Back-end app (for retrieving routes info) can be debugged with the built-in **node.js** debugger in vscode by creating a `launch.json` file.
