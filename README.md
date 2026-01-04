# 📲 Firebase Cloud Messaging (FCM) – Expo React Native

This project demonstrates **Push Notification integration using Firebase Cloud Messaging (FCM)** in a **React Native Expo application** using **Expo Dev Build** and **FCM HTTP v1**.

> ❗ Push notifications are **NOT supported in Expo Go**.  
> This project uses **native builds** via EAS.

---

## 🚀 Tech Stack

- React Native (Expo)
- Firebase Cloud Messaging (FCM v1)
- Expo Application Services (EAS)
- @react-native-firebase

---

## 📁 Project Setup

### 1️⃣ Create Expo App

```bash
npm create-expo-app --template
cd Fcmtest
```

##Install Required Packages
```bash
npm install @react-native-firebase/app
npm install @react-native-firebase/firestore
npm install @react-native-firebase/messaging
```

⚙️ Firebase Configuration
3️⃣ Set Android Package Name

## Update app.json:

{
  "expo": {
    "android": {
      "package": "com.bharath26.Fcmtest"
    }
  }
}


📌 Use the same package name in Firebase Console.

## 4️⃣ Firebase Console Setup

Go to Firebase Console

Create a new project

Add Android App

Paste the package name:

com.bharath26.Fcmtest


Download google-services.json

Place it in the project root directory

## 5️⃣ Link google-services.json in Expo

Update app.json:

{
  "expo": {
    "android": {
      "package": "com.bharath26.Fcmtest",
      "googleServicesFile": "./google-services.json"
    }
  }
}


Expo will automatically copy this file into android/app/ during build.

🔐 FCM HTTP v1 Setup (Required)
## 6️⃣ Generate Service Account Key

Firebase Console → Project Settings

Go to Service Accounts

Click Generate new private key

Download the JSON file

Place it in the project root directory

⚠️ Do NOT commit this file to GitHub

Add to .gitignore:

*-firebase-adminsdk-*.json

## 7️⃣ Configure FCM using EAS

Run:

eas credentials


Follow these steps:

Select Android

Select Production

Select Google Service Account

Choose Manage your Google Service Account Key for Push Notifications (FCM V1)

Select Set up a Google Service Account Key

Upload the service account JSON

Press Y when prompted

🏗️ Build the App (Required)

Push notifications require a development build:

eas build -p android --profile development


Install the generated APK on your Android device.

📲 Enable Notifications on Device

Android Settings → Apps → Your App

## Enable Notifications

🧪 Testing Push Notifications
Using Firebase Console

Firebase Console → Messaging

Click New Campaign

Select Notification

Add title & message

Select your Android App

Click Review → Publish

📩 Notification will be received on the installed app.

https://github.com/user-attachments/assets/9a588037-a3c4-467b-b5a4-45c6937416bd
https://github-production-user-asset-6210df.s3.amazonaws.com/132342144/531735484-9a588037-a3c4-467b-b5a4-45c6937416bd.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20260104%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20260104T150422Z&X-Amz-Expires=300&X-Amz-Signature=5309fc8060dabd90887499d93cfb6610967ea4281c70af9cfe12adfb9cc62640&X-Amz-SignedHeaders=host
