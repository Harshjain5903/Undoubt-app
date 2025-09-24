# 📱 UnDoubt — Anonymous Q&A Platform for Students

UnDoubt is a **Flutter-based mobile app** designed to be a safe and judgment-free space where college students can ask questions about classes, professors, or campus life **anonymously**.  
The app organizes discussions into “classrooms” and delivers a **real-time chat-like Q&A experience** using Firebase.

---

## 🚀 Features
- 🔒 **Anonymous Q&A** — Post and answer without revealing your identity.  
- 🏫 **Classroom-Specific Feeds** — Create or join classrooms using unique codes.  
- 🔑 **Google Sign-In** — Firebase Authentication secures logins while keeping user identities private in the app.  
- 🖼️ **Image Sharing** — Attach images to questions/answers (e.g., lecture slides, problem statements).  
- ⚡ **Real-Time Updates** — Live classroom discussions powered by Firestore listeners.  
- 🎨 **Clean UI** — Minimal, user-focused design for distraction-free Q&A.

---

## 🛠️ Tech Stack

**Frontend:**  
- Flutter (Dart)

**Backend & Cloud (Firebase):**  
- Firebase Authentication — Secure Google Sign-In  
- Cloud Firestore — NoSQL database for users, classrooms, and chats  
- Firebase Storage — Image upload and serving  

**Key Packages:**  
- `google_sign_in` — Google OAuth login  
- `firebase_auth`, `cloud_firestore`, `firebase_storage` — Firebase integration  
- `image_picker` — Access camera/gallery  
- `random_string` — Generate unique classroom codes  
- `shared_preferences` — Store login session locally  
- `fluttertoast`, `photo_view` — User notifications and image zoom/pan  

**Development Tools:**  
- VS Code  
- Xcode (for iOS builds)  
- CocoaPods (iOS dependency manager)  
- Git & GitHub (version control)

---

## 📱 User Flow

1. **Login:**  
   - User signs in with Google.  
   - Firebase Authentication issues a UID (anonymous inside app).  

2. **Classrooms:**  
   - **Create Classroom:** Enter a class name → app generates a unique code → new Firestore document created.  
   - **Join Classroom:** Enter code → Firestore lookup → join if valid.  

3. **Ask/Answer Questions:**  
   - Users post text and/or images.  
   - Images uploaded to Firebase Storage, link stored in Firestore.  

4. **Real-Time Updates:**  
   - Firestore listeners instantly sync questions and answers across all devices in the classroom.

---

## 🧑‍💻 Setup Instructions

> This project requires [Flutter SDK](https://flutter.dev/docs/get-started/install) and a Firebase project.

1. Clone the repository:
   ```bash
   git clone https://github.com/Harsh
