# Your Teacher AI
Created by Shahab Millizai

A mobile-first student AI assistant starter app with:
- Assignment generator
- AI tutor chat
- Study notes / book creator
- MCQ quiz maker
- Writing assistant
- Print / Save as PDF and TXT
- Google Gemini or OpenAI provider selector
- Pink/purple responsive design and launch splash screen

## Quick start
1. Extract this ZIP.
2. Upload `index.html`, `manifest.webmanifest`, and `sw.js` to a new public GitHub repository.
3. In GitHub, open Settings → Pages → Deploy from a branch → `main` → `/ (root)` → Save.
4. Wait for GitHub Pages to publish, then open the generated website URL.
5. Open Settings inside the app, choose Gemini or OpenAI, paste your own API key and press “Save for this session”.

## API key security — read before publishing
This is a prototype / personal-use starter. It sends AI requests directly from the browser to the selected provider. The key is kept in JavaScript memory only (not localStorage and not committed to GitHub), and clears on page reload. However, a key entered into a browser/WebView can still be inspected by the device owner or potentially exposed by a compromised wrapper. **Do not distribute this exact BYOK prototype as a public APK with a valuable API key.**

For a public commercial release, create a secure backend proxy:
- Store provider API keys as server-side environment secrets.
- Authenticate and rate-limit users.
- Add per-user usage limits and abuse protection.
- Never put a shared OpenAI/Gemini secret in frontend JavaScript, GitHub, or an APK.

## PDF export
The app uses the browser's Print dialog. Choose “Save as PDF” on Android/desktop. The TXT button downloads plain text.

## AdMob and Amazon Appstore
The ad box is only a visual placeholder. A normal website/WebView cannot activate AdMob ads by itself. AdMob generally needs a native Android SDK integration (or a wrapper that explicitly supports AdMob and provides its own app/ad unit configuration). Use test ads during development, then request production ad serving after AdMob approval. Follow Amazon Appstore policies and Google AdMob policies; approval and revenue are not guaranteed.

Before submitting:
- Replace the prototype's direct-browser API calls with a secure backend.
- Add a privacy policy and terms/contact page.
- Test API failures, low network, small screens, PDF printing and Android back navigation.
- Confirm that the chosen web-to-APK service supports current Android WebView and AdMob SDK integration.
- Do not promise students that AI output is always correct; ask them to verify facts and learn from drafts.

## Official key pages
- Gemini: https://aistudio.google.com/app/apikey
- OpenAI: https://platform.openai.com/api-keys
