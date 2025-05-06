---
layout:     post
title: 「Mobile App」Bus Trip Planner (Mobile) Deployment Notes
date:       2025-05-06 12:00:00
author:     "LPZhang"
catalog: false
header-style: text
tags: 
  - Vercel
  - React
  - React Native
  - Mobile
---

## Bus Trip Planner (Mobile) Deployment Notes

### Deployment
Back-end Repo: https://github.com/pricezhang42/Commute-Compass-Backend
Web and mobile version both use this backend app.
Front-end Repo: https://github.com/pricezhang42/WinnipegBusTripPlanner

```bash
npx create-expo-app@latest
npm run android

npx @react-native-community/cli init NativeCall
npx react-native run-android
```

### Debugging
Front-end app (mobile) built with **React Native** can be debugged with the built-in debugger in browser.

Back-end app (for retrieving routes info) can be debugged with the built-in **node.js** debugger in vscode by creating a `launch.json` file.
