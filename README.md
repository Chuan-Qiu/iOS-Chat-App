# 📱 iOS Chat App  
A real-time one-on-one chat application built with **iOS UIKit**, **Firebase Authentication**, and **Firestore**.  
Users can register, log in, and exchange messages with other authenticated users—similar to WhatsApp or Messenger.

---

## 🚀 Features

- **🔐 Firebase Authentication**  
  - User registration (name, email, password + confirmation)  
  - Secure login & logout  
  - Input validation & error alerts

- **💬 Real-Time One-on-One Chat**  
  - Firestore snapshot listeners for instant updates  
  - Persistent chat history  
  - Automatic scroll-to-latest messages  
  - Timestamped message bubbles

- **🎨 Clean Messenger-Style UI**  
  - Right-aligned bubbles for self, left-aligned for friends  
  - Lightweight, reusable table view cells  
  - Adaptive Auto Layout for all screen sizes

---

## 📁 Architecture

```
iOS-Chat-App/
├── AppDelegate.swift
├── SceneDelegate.swift
├── Models/
│   ├── ChatMessage.swift
│   └── User.swift
├── Views/
│   ├── ChatCellSelf.swift
│   ├── ChatCellFriend.swift
│   └── LoginView.swift (if applicable)
├── Controllers/
│   ├── LoginViewController.swift
│   ├── RegisterViewController.swift
│   ├── ChatListViewController.swift
│   └── ChatViewController.swift
└── Services/
    ├── FirebaseAuthManager.swift
    └── FirestoreChatManager.swift
```

---

## 🗄️ Firestore Data Structure

```
Firestore/
└── chats/
    └── {chatID}/
        ├── participants: [userA, userB]
        └── messages/
            ├── {messageID}/
                ├── senderID: "uid"
                ├── senderName: "Alice"
                ├── text: "Hello!"
                ├── timestamp: 2024-01-01T00:00:00Z
                └── isSelf: true/false
```

---

## 📸 Screenshots

*(Place your images inside a folder named `Screenshots/` and reference them like this)*

```
Screenshots/
├── login.png
├── chat_list.png
└── chat_room.png
```

**Example in README**:

![Chat Room](Screenshots/chat_room.png)

---

## 🛠️ Tech Stack

- **Language:** Swift  
- **Framework:** UIKit  
- **Backend:** Firebase Authentication, Cloud Firestore  
- **Architecture:** MVC + Service Layer  
- **Tools:** Git, Xcode, CocoaPods / SPM  

---

## 📦 Installation

1. Clone the repository  
   ```sh
   git clone https://github.com/Chuan-Qiu/iOS-Chat-App.git
   cd iOS-Chat-App
   ```

2. Open the project  
   ```
   open iOS-Chat-App.xcodeproj
   ```

3. Configure your Firebase project  
   - Download **GoogleService-Info.plist**  
   - Put it into the Xcode project root  
   - (Optional) Enable email/password login in Firebase Console  

4. Build & run on simulator or device.

---

## 📄 License

Private source code — available upon request for recruiting purposes.

---

## 🔮 Future Work

- Add profile pictures & user presence  
- Push notifications (Firebase Cloud Messaging)  
- Group chat support  
- Dark mode UI  
- Message attachments (images, files)

---

## 👤 Author

**Chance Qiu**  
GitHub: https://github.com/Chuan-Qiu  
