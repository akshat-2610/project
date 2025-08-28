Temple Demo — Vishwanath (college project)

Files:
- index.html      -> Devotee booking page (generate token + QR)
- admin.html      -> Admin panel (start/pause/next token)
- display.html    -> Big-screen display (now serving + countdown)
- styles.css      -> Shared styles

Setup:
1. Create a Firebase project (https://console.firebase.google.com).
2. In Firebase Console: Add a Web App and copy the config (apiKey, authDomain, databaseURL, projectId, etc).
3. In each HTML file replace the placeholder comment:
   var firebaseConfig = /* YOUR_FIREBASE_CONFIG_HERE */ {};
   with your firebase config object, e.g.:
   var firebaseConfig = {
     apiKey: "ABC...",
     authDomain: "project-id.firebaseapp.com",
     databaseURL: "https://project-id-default-rtdb.firebaseio.com",
     projectId: "project-id",
     storageBucket: "project-id.appspot.com",
     messagingSenderId: "12345",
     appId: "1:123:web:abc"
   };

4. Create Realtime Database (test mode is fine for local demo).
5. (Optional) Set initial data via Firebase console or let admin page initialize system node.

Running locally:
- Use a static server (recommended) to avoid browser file restrictions:
  - If you have Node: run 'npx http-server' in the folder and open http://localhost:8080/index.html
  - Or use VSCode Live Server extension.
- Open three tabs:
  - index.html (simulate devotees booking)
  - admin.html (control the system)
  - display.html (TV/monitor)

Notes:
- This demo is for college/prototype use only. It uses open Firebase rules by default for speed; do not use in production.
- For production you'd add authentication, stricter DB rules, SMS integration (Twilio), and better error handling.
