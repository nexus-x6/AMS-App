# <p align="center">Asset Management System</p>

<p align="center">
  <b>A comprehensive and user-friendly financial management application for tracking your assets, expenses, and income across multiple wallets.</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Flutter-2.17.3+-blue.svg" alt="Flutter">
  <img src="https://img.shields.io/badge/Firebase-Integrated-orange.svg" alt="Firebase">
  <img src="https://img.shields.io/badge/Version-1.0.1-green.svg" alt="Version">
  <img src="https://img.shields.io/badge/License-GPL%20v3-yellow.svg" alt="License">
</p>

---

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Building](#building)
- [Screenshots](#screenshots)
- [License](#license)

---

## 🎯 Overview

**Asset Management System (AMS)** is a cross-platform financial management application built with Flutter. It provides users with a powerful yet intuitive interface to manage multiple wallets, track transactions, categorize expenses and income with custom tags, and monitor their financial health in real-time.

The application leverages Firebase services for authentication and real-time data synchronization, ensuring your financial data is secure and accessible across all your devices.

---

## ✨ Features

### 💰 Wallet Management
- **Multiple Wallets**: Create and manage unlimited wallets for different purposes
- **Multi-Currency Support**: Track assets in various currencies with real-time conversion
- **Wallet Descriptions**: Add custom descriptions to organize your wallets

### 📊 Transaction Tracking
- **Income & Expense Recording**: Log all financial transactions with ease
- **Transaction History**: View complete history with timestamps for each wallet
- **Transaction Categories**: Organize transactions with customizable colored tags
- **Edit & Delete**: Modify or remove transaction records as needed

### 🏷️ Tag System
- **Custom Tags**: Create personalized tags for categorizing transactions
- **Color Coding**: Visual identification with custom colors for each tag
- **Action-Based Tags**: Separate tags for income (gelir) and expenses (gider)

### 🔐 Authentication & Security
- **Email/Password Authentication**: Secure login with Firebase Authentication
- **Email Verification**: Verify user accounts for added security
- **Account Management**: Update email, change passwords, or delete accounts
- **Data Privacy**: All data stored securely in Firebase Realtime Database

### 🎨 User Experience
- **Dark/Light Theme**: Toggle between themes for comfortable viewing
- **Responsive Design**: Optimized for various screen sizes
- **Smooth Animations**: Polished UI with native splash screen
- **Offline Support**: Firebase persistence for offline data access
- **Custom Fonts**: Beautiful typography with Proxima Nova and Exo2 fonts

### 📱 Cross-Platform Support
- Android
- iOS
- Web
- Windows
- macOS
- Linux

---

## 🛠️ Technology Stack

### Frontend Framework
- **Flutter** (SDK >=2.17.3 <3.0.0) - Cross-platform UI toolkit
- **Dart** - Programming language

### Backend Services
- **Firebase Authentication** - User authentication and authorization
- **Firebase Realtime Database** - Real-time data synchronization
- **Cloud Firestore** - Document database for structured data

### Key Dependencies
- **Provider** - State management
- **RxDart** - Reactive programming extensions
- **SharedPreferences** - Local data persistence
- **Google Fonts** - Custom typography
- **Intl** - Internationalization and date formatting
- **Flutter SVG** - SVG asset support
- **Google Mobile Ads** - Monetization integration
- **Responsive Grid** - Adaptive layouts

### Development Tools
- **Flutter Launcher Icons** - App icon generation
- **Flutter Native Splash** - Splash screen creation
- **Flutter Lints** - Code quality and style enforcement

---

## 📁 Project Structure

```
ams-app/
├── lib/
│   ├── models/              # Data models
│   │   ├── account.dart     # User account model
│   │   ├── wallet.dart      # Wallet model
│   │   ├── history_node.dart # Transaction model
│   │   ├── tag.dart         # Tag model
│   │   └── currency.dart    # Currency model
│   ├── services/            # Business logic services
│   │   ├── auth_service.dart      # Authentication service
│   │   ├── database_service.dart  # Database operations
│   │   ├── currency_service.dart  # Currency management
│   │   └── theme_service.dart     # Theme management
│   ├── pages/               # UI screens
│   │   ├── splash_page.dart
│   │   ├── login_page.dart
│   │   ├── email_verification_page.dart
│   │   ├── main_page.dart
│   │   ├── add_wallet_page.dart
│   │   ├── transaction_page.dart
│   │   ├── history_page.dart
│   │   ├── settings_page.dart
│   │   └── tags_dialog.dart
│   ├── widgets/             # Reusable UI components
│   │   ├── wallet_widget.dart
│   │   ├── current_wallet.dart
│   │   ├── history_node_widget.dart
│   │   ├── tag_widget.dart
│   │   └── wallet_action_button.dart
│   ├── constants.dart       # App constants
│   ├── functions.dart       # Utility functions
│   ├── firebase_options.dart # Firebase configuration
│   └── main.dart            # Application entry point
├── assets/                  # Static assets
│   ├── ams.svg
│   ├── ams.png
│   ├── ams-onlyicon.svg
│   └── curs.json            # Currency data
├── fonts/                   # Custom fonts
│   ├── proxima/
│   ├── exo2/
│   └── MyFlutterApp.ttf
├── android/                 # Android platform code
├── ios/                     # iOS platform code
├── web/                     # Web platform code
├── linux/                   # Linux platform code
├── macos/                   # macOS platform code
├── windows/                 # Windows platform code
├── pubspec.yaml             # Project dependencies
└── README.md
```

---

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **Flutter SDK** (2.17.3 or higher)
- **Dart SDK** (comes with Flutter)
- **Android Studio** or **Xcode** (for mobile development)
- **Firebase Account** with a project set up
- **Git** for version control

### Platform-Specific Requirements

**Android:**
- Android SDK
- Java Development Kit (JDK)

**iOS:**
- Xcode 12.0 or higher
- CocoaPods
- macOS (required for iOS development)

**Web:**
- Chrome browser for debugging

---

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/nexus-x6/AMS-App.git
cd AMS-App
```

### 2. Install Dependencies

```bash
flutter pub get
```

### 3. Verify Flutter Installation

```bash
flutter doctor
```

Resolve any issues reported by Flutter Doctor before proceeding.

---

## ⚙️ Configuration

### Firebase Setup

1. **Create a Firebase Project:**
   - Go to [Firebase Console](https://console.firebase.google.com/)
   - Create a new project or use an existing one

2. **Enable Firebase Services:**
   - Enable **Authentication** (Email/Password provider)
   - Enable **Realtime Database**
   - Enable **Cloud Firestore** (if needed)

3. **Add Firebase Configuration:**

   **For Android:**
   - Download `google-services.json` from Firebase Console
   - Place it in `android/app/`

   **For iOS:**
   - Download `GoogleService-Info.plist` from Firebase Console
   - Add it to your iOS project in Xcode

   **For Web:**
   - Add Firebase SDK configuration to `web/index.html`

   **For other platforms:**
   - Update `lib/firebase_options.dart` with your Firebase configuration

4. **Configure Firebase Realtime Database Rules:**

```json
{
  "rules": {
    "accounts": {
      "$uid": {
        ".read": "auth != null && auth.uid == $uid",
        ".write": "auth != null && auth.uid == $uid"
      }
    }
  }
}
```

### Google Mobile Ads Setup (Optional)

If you want to enable ads:

1. Create an AdMob account
2. Update `lib/ad_options.dart` with your Ad Unit IDs
3. Add AdMob App IDs to platform-specific configuration files

---

## 🔨 Building

### Run in Debug Mode

```bash
# Run on connected device/emulator
flutter run

# Run on specific device
flutter run -d <device_id>

# Run on Chrome (web)
flutter run -d chrome
```

### Build for Production

**Android (APK):**
```bash
flutter build apk --release
```

**Android (App Bundle):**
```bash
flutter build appbundle --release
```

**iOS:**
```bash
flutter build ios --release
```

**Web:**
```bash
flutter build web --release
```

**Windows:**
```bash
flutter build windows --release
```

**macOS:**
```bash
flutter build macos --release
```

**Linux:**
```bash
flutter build linux --release
```

### Generate App Icons

```bash
flutter pub run flutter_launcher_icons:main
```

### Generate Splash Screen

```bash
flutter pub run flutter_native_splash:create
```

---

## 📱 Screenshots

<p align="center">
  <img src="./ss/1.png" width="200" alt="Screenshot 1">
  <img src="./ss/2.png" width="200" alt="Screenshot 2">
  <img src="./ss/3.png" width="200" alt="Screenshot 3">
  <img src="./ss/4.png" width="200" alt="Screenshot 4">
  <img src="./ss/5.png" width="200" alt="Screenshot 5">
</p>

---

## 📄 License

This project is licensed under the GPL v3 License - see the LICENSE file for details.

[![MIT License](https://img.shields.io/apm/l/atomic-design-ui.svg?)](https://github.com/tterb/atomic-design-ui/blob/master/LICENSEs)
[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

---

## 👨‍💻 Developer

Made with ❤️ using Flutter

---

## 📞 Support

If you have any questions or need help, please open an issue in the repository.

---

**Happy Financial Management! 💰📊**
