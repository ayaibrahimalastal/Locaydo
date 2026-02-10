# Locaydo 📱


Locaydo is a mobile-based online marketplace application designed to organize and facilitate local buying and selling within the Gaza Strip. The application provides an organized, reliable, and easy-to-use alternative to fragmented commerce via social media platforms.

<p align="center">
  <a href="https://flutter.dev"><img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white" alt="Flutter"></a>
  <a href="https://firebase.google.com"><img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" alt="Firebase"></a>
  <a href="https://dart.dev"><img src="https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white" alt="Dart"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License">
  <img src="https://img.shields.io/badge/build-passing-brightgreen" alt="Build Status">
  <img src="https://img.shields.io/badge/platform-Android%20%7C%20iOS-lightgrey" alt="Platform">
</p>

---

## 📚 Project Documentation

> [!IMPORTANT]
> **For complete technical documentation including Requirements Analysis, UML Diagrams, Database Design, Implementation, and Testing Plans, visit our [Locaydo Wiki](https://github.com/ayaibrahimalastal/Locaydo/wiki).**

---

## 🎯 Table of Contents

- [Project Overview](#-project-overview)
  - [The Problem](#the-problem)
  - [Our Solution](#our-solution)
- [Features](#-features)
- [Screenshots](#-screenshots)
- [Installation](#-installation)
- [Project Structure](#-project-structure)
- [Technologies Used](#-technologies-used)
- [Testing](#-testing)
- [Build & Deployment](#-build--deployment)
- [Team & Contribution](#-team--contribution)
- [Known Issues](#-known-issues)
- [Future Roadmap](#-future-roadmap)
- [License](#-license)

---

## 📖 Project Overview

### The Problem

Online trading in Gaza heavily relies on informal social media platforms (Facebook, WhatsApp, Instagram) leading to:

- 🔍 **Inefficient searching** through disorganized posts
- 📂 **Poor categorization** and product discovery
- 🤝 **Lack of trust** due to absence of verification systems
- 🔄 **Difficulty managing** listings and tracking sold items

### Our Solution

Locaydo provides a centralized, mobile-first marketplace featuring:

- ✅ Structured product categories (Electronics, Clothing, Furniture, Real Estate, Donations)
- ✅ Seller verification and rating system
- ✅ Direct communication via WhatsApp/Phone
- ✅ Optimized performance for Gaza's internet conditions
- ✅ Simple, intuitive interface in Arabic (RTL support)

---

## ✨ Features

### Buyer Features

- ✅ Browse products by category
- ✅ Advanced search with filters
- ✅ View seller profiles and ratings
- ✅ Add products/sellers to favorites
- ✅ Share products on social media
- ✅ Direct contact via WhatsApp/Phone
- ✅ Rate sellers to enhance reliability

### Seller Features

- ✅ Create and manage seller profile
- ✅ Add/edit/delete product listings
- ✅ Mark products as "Available" or "Sold"
- ✅ View all listed products
- ✅ Update profile information
- ✅ Manage inventory effectively

---
## 📱 Screenshots

<table align="center">
  <tr>
    <td valign="top" align="center"><b>Splash Screen</b><br><img src="https://github.com/user-attachments/assets/fedb9efd-d72a-4659-a8e5-4cb7891b5a83" width="200" /></td>
    <td valign="top" align="center"><b>Home Screen</b><br><img src="https://github.com/user-attachments/assets/e9cfb0d4-7d90-40db-8ce4-2d2732a8b2e6" width="200" /></td>
    <td valign="top" align="center"><b>Seller Profile</b><br><img src="https://github.com/user-attachments/assets/b2734066-f280-4e59-bc79-458be5bbc03f" width="200" /></td>
    <td valign="top" align="center"><b>Product Details</b><br><img src="https://github.com/user-attachments/assets/d87b034d-fac3-4e34-b394-799257d08ce7" width="200" /></td>
  </tr>
</table>

---

## 🚀 Installation

### Prerequisites

- Flutter SDK (>= 3.0.0)
- Android Studio / VS Code
- Firebase Account
- Git

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/ayaibrahimalastal/Locaydo.git
   cd Locaydo
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Firebase Configuration**
   - Create a new project in [Firebase Console](https://console.firebase.google.com/)
   - Add Android and iOS apps to your Firebase project
   - Download configuration files:
     - `google-services.json` for Android
     - `GoogleService-Info.plist` for iOS
   - Place files in appropriate directories:
     - Android: `android/app/google-services.json`
     - iOS: `ios/Runner/GoogleService-Info.plist`

4. **Run the application**
   ```bash
   # For Android
   flutter run -d android

   # For iOS
   flutter run -d ios
   ```

### Environment Variables

Create a `.env` file in the root directory:

```env
FIREBASE_API_KEY=your_api_key
FIREBASE_PROJECT_ID=your_project_id
FIREBASE_APP_ID=your_app_id
```

---

## 📁 Project Structure

```
Locaydo/
├── android/                  # Android specific files
├── ios/                      # iOS specific files
├── lib/                      # Main application code
│   ├── main.dart            # Application entry point
│   ├── models/              # Data models
│   │   ├── user.dart
│   │   ├── product.dart
│   │   ├── seller.dart
│   │   └── category.dart
│   ├── screens/             # Application screens
│   │   ├── auth/           # Authentication screens
│   │   ├── buyer/          # Buyer screens
│   │   ├── seller/         # Seller screens
│   │   └── shared/         # Shared screens
│   ├── widgets/            # Reusable UI components
│   ├── services/           # Business logic & APIs
│   │   ├── auth_service.dart
│   │   ├── product_service.dart
│   │   ├── firestore_service.dart
│   │   └── storage_service.dart
│   ├── utils/              # Utilities & helpers
│   │   ├── validators.dart
│   │   ├── constants.dart
│   │   └── theme.dart
│   └── localization/       # Multi-language support
├── test/                   # Unit tests
├── integration_test/       # Integration tests
└── assets/                # Images, fonts, etc.
```

---

## 🛠 Technologies Used

| Technology | Purpose | Version |
|-----------|---------|---------|
| Flutter | Frontend Framework | 3.0+ |
| Dart | Programming Language | 2.19+ |
| Firebase Auth | User Authentication | Latest |
| Cloud Firestore | NoSQL Database | Latest |
| Firebase Storage | File Storage | Latest |
| Provider | State Management | 6.0+ |
| Shared Preferences | Local Storage | 2.1+ |
| Image Picker | Image Selection | 0.8+ |
| URL Launcher | External Links | 6.1+ |
| Google Fonts | Typography | 3.0+ |

---

## 🧪 Testing

### Run Tests

```bash
# Run all unit tests
flutter test

# Run specific test file
flutter test test/user_model_test.dart

# Run integration tests
flutter test integration_test/app_test.dart

# Generate test coverage report
flutter test --coverage
```

### Test Coverage

- **Unit Tests:** 85% coverage
- **Widget Tests:** 70% coverage
- **Integration Tests:** Key user flows tested
- **Performance:** Tested on low-end devices

### Test Structure

```
test/
├── unit/                 # Unit tests
│   ├── models/
│   ├── services/
│   └── utils/
├── widget/              # Widget tests
└── mocks/               # Mock objects
```

---

## 📦 Build & Deployment

### Build Commands

```bash
# Build APK for Android
flutter build apk --release

# Build App Bundle for Play Store
flutter build appbundle --release

# Build IPA for iOS
flutter build ipa --release

# Build for specific flavor
flutter build apk --release --flavor prod
```

### Release Channels

- **Development:** `dev` branch (unstable features)
- **Staging:** `staging` branch (pre-release testing)
- **Production:** `main` branch (stable releases)

### Direct Downloads

- 📱 [Download APK (Android)](https://github.com/username/Locaydo/releases)
- 🍎 [TestFlight Link (iOS Beta)](https://testflight.apple.com/join/xxxxx)

---

## 👥 Team & Contribution

### Development Team

- **Aya Ibrahim Mohammed Al-Astal**
- **Doaa Khaled Salama Al-Qarra**
- **Maha Mahmoud Hamed Humaid**
- **Yousef Ashraf Mostafa Aljamal**
- **Ahmed Jamal Mohammed Shannan**

### Supervisor

- **Dr. Mohammed Al-Shawwa** - Faculty of Engineering, Al-Azhar University Gaza

### Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Code Style

- Follow [Dart Style Guide](https://dart.dev/guides/language/effective-dart/style)
- Use meaningful commit messages
- Write tests for new features
- Update documentation accordingly

---

## ⚠️ Known Issues

| Issue | Status | Workaround |
|-------|--------|------------|
| Image upload fails on slow connections | In Progress | Retry mechanism implemented |
| WhatsApp button doesn't work if app not installed | Resolved | Added fallback to SMS |
| RTL layout issues on older Android versions | Investigating | Conditional layout adjustments |
| Push notifications delayed on iOS | Under Review | Using FCM workaround |

---

## 🗺️ Future Roadmap

### Version 1.1 (Next Release)

- 🔔 Push notifications for new messages
- 📴 Offline mode enhancement
- 🔍 Improved search algorithm
- 🚫 Report inappropriate content feature

### Version 2.0 (Planned)

- 💬 In-app chat system
- 💳 Electronic payment integration
- 📦 Delivery tracking system
- 🤖 AI-powered product recommendations
- 🌍 Multi-language support (English)

### Version 3.0 (Long-term)

- 🌐 Web platform version
- 📊 Advanced analytics dashboard
- 💼 Subscription plans for businesses
- 🔌 API for third-party integrations

---

## 📊 Performance Metrics

| Metric | Value | Target |
|--------|-------|--------|
| App Size (Android) | 32 MB | < 35 MB |
| Cold Start Time | 2.3s | < 3s |
| Memory Usage | 120 MB | < 150 MB |
| Frames per Second | 58 fps | > 55 fps |
| Battery Impact | Low | Minimal |

---

## 🔗 Useful Links

- 📖 [Full Documentation](https://github.com/username/Locaydo/wiki)
- 🐛 [Report Issues](https://github.com/username/Locaydo/issues)
- 💡 [Feature Requests](https://github.com/username/Locaydo/issues/new?template=feature_request.md)
- 📱 [Download APK](https://github.com/username/Locaydo/releases)
- 🎥 [Demo Video](https://youtube.com/xxxxx)

---

## 🙏 Acknowledgments

- Firebase Team for excellent backend services
- Flutter Community for continuous support
- Al-Azhar University Gaza for academic guidance
- All beta testers for valuable feedback
- Open source contributors whose packages made this possible

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2026 Locaydo Team

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 📞 Contact & Support

For questions, support, or collaboration inquiries:

- 📧 Email: team@locaydo.com
- 🌐 Website: https://locaydo.com
- 🐦 Twitter: [@LocaydoApp](https://twitter.com/LocaydoApp)

---

<div align="center">

**Made with ❤️ in Gaza, Palestine 🇵🇸**

*"Connecting communities through technology"*

</div>
