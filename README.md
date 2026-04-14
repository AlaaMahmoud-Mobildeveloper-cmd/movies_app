# 🎬 Moves Final Project

A robust Flutter application built with a feature-driven architecture, integrating Firebase for backend services and BLoC/Provider for state management.

---

## 📸 Screenshots

### 1. Onboarding & Authentication
The user journey starts with registration and secure access to the platform.

<p align="center">
  <img src="assets/screenshots/1.png" width="189" title="Register Screen" alt="Register Screen">
  <img src="assets/screenshots/2.png" width="189" title="Login Screen" alt="Login Screen">
</p>

### 2. Core Experience
Exploring, searching, and viewing movie details.

<p align="center">
  <img src="assets/screenshots/3.png" width="190" title="Home Screen" alt="Home Screen">
  <img src="assets/screenshots/4.png" width="189" title="Movie Details Screen" alt="Movie Details Screen">
</p>
<p align="center">
  <img src="assets/screenshots/5.png" width="186" title="Search Results Screen" alt="Search Results Screen">
  <img src="assets/screenshots/6.png" width="178" title="Filtered Genre Screen" alt="Filtered Genre Screen">
</p>

### 3. User Profile & Personalization
Managing account details and content lists.

<p align="center">
  <img src="assets/screenshots/7.png" width="187" title="Profile View Screen" alt="Profile View Screen">
  <img src="assets/screenshots/8.png" width="179" title="Watch List and History" alt="Watch List and History">
  <img src="assets/screenshots/9.png" width="181" title="Edit Profile Screen" alt="Edit Profile Screen">
</p>
<p align="center">
  <img src="assets/screenshots/10.png" width="188" title="Change Avatar Screen" alt="Change Avatar Screen">
</p>

---
## 📂 Project Architecture

The project follows a **Feature-based Clean Architecture** to ensure maintainability:

- **`core/`**: Contains shared utilities, themes, and global configurations.
- **`features/`**: The heart of the app, divided by functionality:
    - **`auth/`**: Handles Login, Registration, and Password Recovery.
        - `data/`: Repositories and data sources.
        - `presentation/`: UI screens.
        - `providers/`: Logic and state management for authentication.
    - **`onboarding/`**: Initial user walkthrough experience.
    - **`home/`**: Main dashboard and navigation.
    - **`details/`**: Detailed views for app content.
    - **`edit_profile/`**: User profile management.
- **`widgets/`**: Reusable UI components used across multiple features.

---

## 🚀 Key Technologies

- **State Management**: `flutter_bloc` & `provider`.
- **Navigation**: `auto_route` (Generator-based routing).
- **Dependency Injection**: `get_it` & `injectable` (Setup in `di.dart`).
- **Backend**: Firebase Auth & Cloud Firestore.
- **Networking**: `dio` with `pretty_dio_logger`.
- **UI Responsiveness**: `flutter_screenutil`.

---

## 🛠️ Getting Started

### 1. Code Generation
This project uses `build_runner`. After adding new routes or injectable services, run:
```bash
flutter pub run build_runner build --delete-conflicting-outputs