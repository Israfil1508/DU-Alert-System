# DU Alert - Flutter Frontend

A Flutter-based campus safety platform for DU (Dhaka University) that allows students to report incidents, receive alerts, and connect with proctors and admin.

## Prerequisites

- Flutter SDK (3.10.3 or higher)
- Dart 3.10.3+

## Project Structure

```
lib/
├── core/                    # App-wide utilities
│   ├── constants/          # API, colors, strings
│   ├── services/           # API, location, notification services
│   └── theme/              # App theming
├── features/               # Feature-based architecture
│   ├── auth/              # Login, register, password recovery
│   ├── dashboard/         # User dashboards
│   ├── sos/               # SOS alerts
│   ├── complaint/         # Report complaints
│   └── admin/             # Admin panel
├── screens/               # Global screens
├── routes/                # Route definitions
├── shared/                # Shared widgets and models
└── state/                 # State management providers
```

## Setup

1. Install dependencies:

```bash
flutter pub get
```

2. Run app:

```bash
# Android/iOS emulator
flutter run

# Web
flutter run -d chrome

# Linux/Windows/macOS
flutter run -d <device>
```

## Features

- **Authentication**: Register, login, OTP verification
- **Forgot Password**: Reset password via OTP
- **Alerts**: Create and view campus-wide alerts
- **Notifications**: Real-time notifications for alerts
- **Admin Panel**: Manage users and roles
- **Role-based UI**: Student, Proctor, Admin dashboards

## API Configuration

Update `lib/core/constants/api_constants.dart` to change backend URL:

```dart
class ApiConstants {
  static const String baseUrl = 'http://your-backend-url/api';
}
```

For Android emulator: `http://10.0.2.2:3000/api`
For iOS simulator: `http://localhost:3000/api`

## Build Release

```bash
# Android APK
flutter build apk --split-per-abi

# iOS IPA
flutter build ios

# Web
flutter build web
```
