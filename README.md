# Signup App – Part 2

A Flutter app that builds on the Part 1 signup form to create a complete, multi-screen signup flow.

---

## Screens

### 1. Welcome Screen
- Animated fade-in and slide-up intro
- Pulsing "Get Started" button
- Uses `Navigator.push()` to navigate to the signup screen so the user can go back if needed

### 2. Signup Screen
- All Part 1 validation logic (name, email, password)
- Date picker for birth date
- Password visibility toggle
- Loading spinner before navigating to success

### 3. Success Screen
- Personalized message using the user's name
- Animated bouncing checkmark
- "Back to Start" button that clears the navigation stack back to the welcome screen

---

## File Structure

```
lib/
  main.dart                  # App entry point, named routes
  screens/
    welcome_screen.dart      # Animated intro screen
    signup_screen.dart       # Enhanced signup form
    success_screen.dart      # Completion screen
```

---

## How to Run

1. Clone the repository:
```bash
git clone https://github.com/samia21-04/signup_app.git
```

2. Navigate into the project:
```bash
cd signup_app
```

3. Install dependencies:
```bash
flutter pub get
```

4. Run the app:
```bash
flutter run
```

---

## How to Build APK

```bash
flutter build apk
```

Output will be at:
```
build/app/outputs/flutter-apk/app-release.apk
```

---

## Navigation Flow

```
Welcome Screen
     ↓  (Get Started)
Signup Screen
     ↓  (Sign Up — replaces Signup in stack)
Success Screen
     ↓  (Back to Start — clears stack)
Welcome Screen
```

> The success screen **replaces** the signup screen so the user cannot navigate back to a form they already submitted.

---

## Built With

- [Flutter](https://flutter.dev/)
- Dart