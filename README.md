# Foundation App MVP

## Features
- Wake logic (morning greeting)
- Tone-based activity suggestions
- Token accumulation and reward simulation
- Personalized task suggestions based on history
- Firebase integration

## Setup
1. Replace the values in `firebase.js` with your Firebase project details.
2. Run `npm install` to install dependencies.
3. Run the app with `expo start`.

## Firebase Firestore Rules
```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /users/{userId} {
      allow read, write: if request.auth != null && request.auth.uid == userId;
    }
  }
}
```
