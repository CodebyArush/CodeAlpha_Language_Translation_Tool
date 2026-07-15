🌐 Full-Stack Language Translation Tool
Overview
Break down language barriers with this sleek, full-stack Language Translation Tool. Designed with a modern aesthetic and built for performance, this application pairs a highly interactive, responsive frontend with a robust Python Flask backend. By leveraging the MyMemory Translation API, it delivers fast, accurate translations across more than 20 global languages while providing a seamless user experience complete with text-to-speech capabilities, clipboard management, and real-time server health monitoring.

✨ Key Features
🎨 Intuitive & Modern User Interface
Glassmorphism Aesthetic: A beautiful, responsive UI featuring backdrop blurs, smooth gradients, and CSS animations (like the sliding startup animation and interactive button hovers).

Real-time Character Tracking: Built-in validation tracks character count up to a 5,000-character limit, with dynamic color-coding that warns users as they approach the maximum.

One-Click Swap: A dynamic toggle button instantly swaps the source and target languages (and their respective text blocks) with a satisfying rotation animation.

⚡ Interactive Tools
Text-to-Speech (TTS): Integrated Web Speech API allows users to hear the translated text spoken out loud with accurate, localized accents.

Smart Clipboard Integration: A one-click "Copy" feature with a seamless fallback mechanism ensures translations can be instantly copied to the user's clipboard across different browsers.

Keyboard Shortcuts: Power users can hit Ctrl + Enter to trigger translations instantly without touching the mouse.

🛠️ Robust Backend Engine
Flask API Gateway: A lightweight, secure Python backend routes translation requests, preventing direct client-side API exposure.

MyMemory API Integration: Utilizes the MyMemory Translation API for accurate, context-aware translations, including an "Auto-detect" feature for unknown source languages.

Active Server Monitoring: The frontend continuously pings the backend, displaying a real-time "Server Connected" or "Server Disconnected" status indicator so users never have to guess if the app is online.

💻 Tech Stack
Frontend
HTML5 / CSS3: Structured layout with Flexbox/Grid, custom keyframe animations, and a mobile-first responsive design.

Vanilla JavaScript (ES6+): Object-Oriented JS (using a PythonTranslationTool class) handles DOM manipulation, event listeners, async fetch API calls, and the SpeechSynthesis interface.

Backend
Python 3: The core server logic.

Flask: A micro web framework serving the frontend templates and handling RESTful API POST and GET requests.

Requests Library: Manages secure, timeout-protected HTTP calls to the external MyMemory API.

🚀 How It Works:
Input: The user types text into the source text area. As they type, the JavaScript class updates the character count in real-time.

Request: Upon clicking "Translate" (or Ctrl + Enter), the frontend bundles the text, source language code, and target language code into a JSON payload and sends an async POST request to the /translate Flask endpoint.

Processing: The Flask server sanitizes the input, URL-encodes the text, and routes it to the MyMemory API.

Response: The backend catches the API's JSON response, handles any potential errors (like timeouts or empty payloads), and passes the clean, translated text back to the client.

Display: The UI elegantly animates the appearance of the new text, temporarily disables the loading state, and surfaces the "Copy" and "Speak" action buttons for the user to interact with.
