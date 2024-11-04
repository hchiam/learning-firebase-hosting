# Learning Firebase Hosting

Just one of the things I'm learning. <https://github.com/hchiam/learning>

```sh
npm install -g firebase-tools
firebase login
firebase init
```

(Aside: I had to `firebase logout` and then `firebase login` to get `firebase init` to work.)

then either one of the two following:

## 1 of 2

Install:

```sh
npm install firebase
```

```js
// Import the functions you need from the SDKs you need
import { initializeApp } from "firebase/app";
import { getAnalytics } from "firebase/analytics";
// TODO: Add SDKs for Firebase products that you want to use
// https://firebase.google.com/docs/web/setup#available-libraries

// Your web app's Firebase configuration
// For Firebase JS SDK v7.20.0 and later, measurementId is optional
const firebaseConfig = {
  apiKey: "...",
  authDomain: "....firebaseapp.com",
  databaseURL: "https://....firebaseio.com",
  projectId: "...",
  storageBucket: "....firebasestorage.app",
  messagingSenderId: "...",
  appId: "...",
  measurementId: "..."
};

// Initialize Firebase
const app = initializeApp(firebaseConfig);
const analytics = getAnalytics(app);
```

## 2 of 2

or use script tags:

```html
<script type="module">
  // Import the functions you need from the SDKs you need
  import { initializeApp } from "https://www.gstatic.com/firebasejs/11.0.1/firebase-app.js";
  import { getAnalytics } from "https://www.gstatic.com/firebasejs/11.0.1/firebase-analytics.js";
  // TODO: Add SDKs for Firebase products that you want to use
  // https://firebase.google.com/docs/web/setup#available-libraries

  // Your web app's Firebase configuration
  // For Firebase JS SDK v7.20.0 and later, measurementId is optional
  const firebaseConfig = {
    apiKey: "...",
    authDomain: "....firebaseapp.com",
    databaseURL: "https://....firebaseio.com",
    projectId: "...",
    storageBucket: "....firebasestorage.app",
    messagingSenderId: "...",
    appId: "...",
    measurementId: "..."
  };

  // Initialize Firebase
  const app = initializeApp(firebaseConfig);
  const analytics = getAnalytics(app);
</script>
```

## either way, this is the last step

```sh
firebase deploy
```

e.g.: <https://trysterollup.web.app/>
