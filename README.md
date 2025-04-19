# Jobsite Attendance Tracker

A smart, Firebase-powered web app for streamlined jobsite check-ins.

## Live Demo: https://jobsitetracker-e986a.web.app
 
**GitHub Repo**: [https://github.com/nnusaibah/jobsite-attendance-tracker](https://github.com/nnusaibah/jobsite-attendance-tracker)


## Features

- **User Authentication** with Firebase
- **Geo-fenced Check-In System** – users must be near the jobsite
- **Offline Mode** – check-ins are stored locally and sync when back online
- **QR Code-Based Access** for quick, secure check-ins
- **Anomaly Detection** – flags unusual location activity


## Tech Stack

- **Frontend**: Angular, TypeScript, HTML/CSS
- **Backend**: Firebase Firestore & Firebase Authentication
- **Extras**: Capacitor Geolocation, Angularx QR Code


## Screenshots 

![image](https://github.com/user-attachments/assets/83c07c9a-81c5-48e7-b6f9-a868dcf0df70)



## How to Run Locally

1. Clone the repo  
   `git clone https://github.com/nnusaibah/jobsite-attendance-tracker.git`
2. Navigate to the folder  
   `cd jobsite-attendance-tracker`
3. Install dependencies  
   `npm install`
4. Run the app  
   `ng serve --open`


## How It Works

1. Click **Sign In with Google**.
2. Use **Check In** to log your current location.


## Firestore Rules

```ts
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /check-ins/{docId} {
      allow read: if true;
      allow write: if request.auth != null;
    }
  }
}


## Work in Progress

This project is still actively being developed. Current improvements underway:

- Displaying **user name and email** alongside check-ins
- Adding **check-out functionality** with duration tracking
- Improving **mobile responsiveness**
- Export to CSV or download history
- More robust **error handling** (e.g. failed geolocation)

Stay tuned! 


## Inspiration

This project began as a way to explore geolocation APIs, Firebase, and Angular’s modern component structure — with the goal of building something real and useful.


## 🙋‍♀️ About Me

Hi! I'm **Nusaibah**, a Computer Science undergraduate passionate about solving real-world problems through clean code and smart design. I love working on impactful projects that go beyond the classroom.


