# iOS Chat App

A real-time one-on-one chat application built for iOS using **Firebase Authentication** and **Cloud Firestore**.  
This project demonstrates secure user auth, cloud-hosted messaging, dynamic chat UI, and clean modular architecture suitable for mobile portfolio presentation.

---

## 📱 Features

### **Authentication**
- Register with name, email, password, and password confirmation  
- Login / Logout with Firebase Authentication  
- Input validation with user-friendly alert messages  
- Persistent user session until manual logout  

### **Real-Time Chat**
- One-on-one messaging between all authenticated users  
- Real-time message sync powered by Firestore snapshot listeners  
- Automatic scroll-to-latest message  
- Chat history persisted across sessions  
- Timestamp formatting for readable message metadata  

### **Chat UI**
- WhatsApp-style left/right aligned message bubbles  
- Dynamic cell layouts showing:
  - Sender name
  - Message text
  - Timestamp  
- Clean, responsive Auto Layout  
- Separated cells for "self" vs "friend" messages  

---

## 🧱 Architecture

iOS-Chat-App
│
├── Authentication
│ ├── LoginViewController
│ ├── RegisterViewController
│ └── AuthManager (Firebase Authentication wrapper)
│
├── Chat
│ ├── ChatListViewController
│ ├── ChatViewController
│ ├── Message.swift
│ ├── ChatService (Firestore CRUD + listeners)
│ └── MessageCell (self / friend variants)
│
└── Shared
├── User.swift
├── Extensions (UI helpers / formatting)
└── Utilities (alerts, constants, etc.)

### **Key Principles**
- MVVM-lite style separation  
- Firebase service classes isolate networking logic  
- Reusable UI components for cleaner controllers  
- Snapshot listeners push updates reactively  
- All user input validated before backend operations  

---

## 🗄️ Firebase Structure

### **Authentication**
- Email/Password Auth  
- DisplayName stored with user profile  

### **Firestore**
messages (collection)
└── chatRoomID (document)
└── messages (subcollection)
├── messageID
│ ├── senderID
│ ├── senderName
│ ├── text
│ ├── timestamp
│ └── isSelf

---

## 📸 Screenshots

> Place your images in:  
> **/ScreenShots** (create this folder in the repo root)  
>  
> Then reference like:  
> `![Chat Screen](ScreenShots/chat_screen.png)`

_Add your screenshots here after uploading._

---

## 🚀 How to Run

1. Clone the repo  
   ```bash
   git clone git@github.com:Chuan-Qiu/iOS-Chat-App.git
Open the project
open iOS-Chat-App.xcodeproj
Add your GoogleService-Info.plist to the Xcode project root
Run on an iOS Simulator or physical device
🧪 Requirements
iOS 15+
Xcode 14+
Swift 5
CocoaPods / SPM not required (Firebase added via project configuration)
🔐 Security Notes
API keys are handled using Firebase recommended configuration
No private code or school assignment requirements are included
Sensitive logic is encapsulated in local service classes
🧭 Future Work (Optional)
Support image messages
Add typing indicator
Group chat rooms
Push notifications via Firebase Cloud Messaging
Online/Offline presence tracking
Profile pictures stored in Firebase Storage
👥 Teamwork Notes
Originally developed as part of a team assignment; this repository contains only clean, public-safe, non-school-restricted code.
📄 License
This project is available for portfolio demonstration purposes.
Commercial or production use is not permitted.
