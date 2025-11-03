<img width="1920" height="1080" alt="tutor-connect (2)" src="https://github.com/user-attachments/assets/fed992f9-c202-48e5-815e-33cd65ca68db" />


## 1. Overview



**TutorConnect** is a modern tutoring platform developed by **W.I.L Enterprise**. It connects students with verified tutors for one-on-one or group learning sessions.  

The platform focuses on accessibility, personalized learning, and efficient session management.  

Students can discover tutors based on subject expertise, book sessions, complete quizzes, track their progress, and communicate directly within the app.

<div style="display: inline-block; width: 28%; vertical-align: top; text-align: right;">
  <img src="https://github.com/user-attachments/assets/9d3fafb7-df1f-4c5b-81c9-1b92be362c1e" 
       alt="TutorConnect Graphic" 
       width="230" 
       style="border-radius: 12px; margin-left: 16px; margin-top: 8px;">
</div>

---

## 2. Team & Roles

**W.I.L Enterprise Team**

- **Quellon Naicker** — Team Lead / Full-Stack Developer  
- **Sajana Bidesi** — Project Manager / Full-Stack Developer  
- **Jadin Naicker** — Frontend Developer  
- **Emma Mae Atkison** — Frontend Developer  
- **Jose Gonzalves** — Backend Developer  
- **Ayushkar Ramkisson** — Backend Developer  
- **Kian Campbell** — Full-Stack Developer  

Each member contributed to the planning, design, development, and testing of TutorConnect, ensuring a seamless workflow and consistent coding standards across all modules.

---

## 3. Functional Requirements (Core Features)

- **User Authentication** — Secure registration and login for students, tutors, and admins.  
- **Tutor Discovery** — Search and filter tutors by subject, rating, and availability.  
- **Session Booking** — Students can schedule, reschedule, or cancel tutoring sessions.  
- **Calendar Management** — Integrated session calendar for students and tutors.  
- **Real-Time Chat** — In-app messaging between students and tutors.  
- **Quizzes & Assessments** — Students can take adaptive quizzes to measure progress.  
- **YouTube Player Integration** — Embedded learning videos and tutorials.  
- **Location Services** — Find local tutors or display nearby tutoring centers.  
- **Notifications** — Reminders for upcoming sessions and new messages.  
- **Admin Dashboard** — Manage users, approve tutors, and monitor app activity.

---

## 4. Technology Stack

**Frontend:**  
React Native (Expo) — Mobile development for iOS & Android  
React + Next.js — Web version for cross-platform access  

**Backend:**  
Express.js — REST API handling routes, logic, and middleware  
Node.js — Core runtime environment  

**Database:**  
Firebase — Authentication, storage, and real-time database services  

**Additional Tools & Services:**  
Render — API hosting  
GitHub — Version control and collaboration  
Jira — Task tracking and sprint management  
Discord & WhatsApp — Team communication  

![Architecture](https://github.com/user-attachments/assets/194c01cb-5606-4725-85e6-7c1d649a4c04)

---

## 5. System Architecture

The TutorConnect system follows a layered architecture that separates concerns between frontend, backend, and database components.  

**Architecture Flow:**  
Frontend (React / React Native) → API Gateway (Express.js) → Database (Firebase)  

Data flows securely through the REST API to ensure synchronization between mobile and web clients.  
Each layer handles its own logic, improving scalability, maintainability, and debugging efficiency.

![Architecture Diagram](https://github.com/user-attachments/assets/4bac3773-bf26-4bb1-8382-54b8497ce441)

---

## 6. Installation & Setup

### Step 1: Clone the repository

```bash
git clone https://github.com/W-I-L-Enterprise/ReactExpo.git
cd TutorConnect
```

Step 2: Backend Setup
cd backend

# App dependencies
```npm install helmet
npm install nodemailer
npm install dotenv
npm install cohere-ai
```

# Testing
```
npm install --save-dev jest
npm install --save-dev supertest
```

Step 3: Frontend Setup
```
cd frontend
```

# Core Expo + RN libs
```
npx expo install expo@latest
npx expo install --fix -- --legacy-peer-deps
npx expo upgrade
```

# Expo modules
```
npx expo install expo-document-picker expo-file-system/legacy
npx expo install expo-font @expo-google-fonts/poppins
npx expo install expo-linking expo-web-browser
npx expo install react-native-screens react-native-safe-area-context
npx expo install expo-blur
npx expo install react-native-webview
npx expo install lottie-react-native
```

# React Navigation
```
npm install @react-navigation/native @react-navigation/native-stack
```

# React Native community libs
```
npm install @react-native-async-storage/async-storage @react-native-community/netinfo
npm install react-native-chart-kit react-native-svg
npm install react-native-markdown-display
npm install react-native-worklets --legacy-peer-deps
npm install axios
npm install react-native-youtube-iframe
npm install lottie-react   # optional for web
```

# Testing (frontend)
```
npm install --save-dev jest jest-environment-jsdom
```

# Pin versions for Expo SDK compatibility
```
npm pkg set dependencies.react=19.1.0
npm pkg set dependencies."react-dom"=19.1.0
npm pkg set dependencies."react-native"=0.81.5
npm pkg set dependencies."expo-linking"="~8.0.8"
npm pkg set dependencies."expo-web-browser"="~15.0.8"
npm pkg set dependencies."react-native-reanimated"="~4.1.1"
npm pkg set dependencies."react-native-webview"="13.15.0"
npm pkg set dependencies."react-native-worklets"="0.5.1"
npm pkg set dependencies.metro="~0.81.0"
npm pkg set dependencies."metro-config"="~0.81.0"
```

# Dev tooling
```
npm pkg set devDependencies."@types/react"="~19.1.10"
npm pkg set devDependencies.typescript="~5.9.2"
npm pkg set devDependencies."eslint-config-expo"="~10.0.0"

# Remove problematic Lottie package
npm rm @lottiefiles/dotlottie-react

# Babel config (for Reanimated)
cat > babel.config.js << 'EOF'
module.exports = function (api) {
  api.cache(true);
  return {
    presets: ['babel-preset-expo'],
    plugins: ['react-native-reanimated/plugin'],
  };
};
EOF
```

# Finalize
```
npm install
npx expo install --fix -- --legacy-peer-deps
npx expo start --clear
```

Step 4: Run the Application
# Start backend
```
cd backend
npm start
```

# Start frontend (mobile/web)
```
cd frontend
npx expo start
```

Step 5: Environment Variables

Create a .env file in both backend and frontend directories.

Step 6: Testing

Run unit and integration tests using Jest or Supertest.
```
npm test
```
Step 7: Notes

For mobile development, install Expo Go on your device and scan the QR code from your terminal after running:
```
npx expo start
```

If dependencies conflict, re-run:
```
npx expo install --fix -- --legacy-peer-deps
```

For API updates, ensure backend changes are redeployed on Render before syncing with the frontend.
