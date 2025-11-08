# Jira-Tracker 08/11/2025
A comprehensive Jira-like issue tracker and project management website
---
---
## 🖥 Screenshots  

| Page      | Preview |
|-----------|---------|
| Dashboard      | ![Dashboard](https://github.com/user-attachments/assets/3ef41759-d46d-41ea-8f79-c2d530389400) |
| Projects   | ![Projects](https://github.com/user-attachments/assets/d7adbd55-a1fe-4a47-ac96-662951a4ef5b) |
| Issues   | ![Issues](https://github.com/user-attachments/assets/79970c64-a591-40a7-b58f-14f4eb471b11) |
| Issues Card   | ![Issue_Card](https://github.com/user-attachments/assets/7191748f-83b9-42f3-9540-c2844c39052c) |
| Reports   | ![Reports](https://github.com/user-attachments/assets/e93a52bc-6eba-4a30-b25c-0a83dac52f3f) |
| Settings   |  ![Settings](https://github.com/user-attachments/assets/fa8060de-f457-4e03-993e-2179abdf9c16) |

---

```
frontend/
├── package.json							# Frontend dependencies & build scripts
├── vite.config.js							# Vite build tool configuration
├── postcss.config.js						# PostCSS processing config
├── tailwind.config.js						# Tailwind CSS customization
├── index.html								# Application entry HTML
├── netlify.toml							# Netlify deployment configuration
├── .env									# Development environment variables
├── .env.production							# Production environment variables
├── 📁 netlify/
│    ├── 📁 functions/
│    └── send-email.js						# Email function
├── 📁 public/								# Static assets
│   ├── favicon.ico							# Site favicon
│   ├── favicon-32x32.png					# Standard favicon size
│   └── apple-touch-icon.png				# iOS home screen icon
└── 📁 src/
    ├── main.jsx							# React application entry point
    ├── App.jsx								# Root application component
    ├── index.css							# Global styles & CSS imports
    ├── 📁 config/							# Application configuration
    │   └── firebase.js						# Firebase client configuration
    ├── 📁 contexts/						# React context providers
    │   ├── AuthContext.jsx					# Authentication state management
    │   ├── SocketContext.jsx				# WebSocket connections
    │   ├── ThemeContext.jsx				# Light/dark theme management
    │   └── NotificationContext.jsx			# Notification state
    ├── 📁 components/						# React components organized by feature
    │   ├── 📁 auth/						# Authentication components
    │   │   ├── Login.jsx					# Login form component
    │   │   └── Register.jsx				# Registration form component
    │   ├── 📁 common/						# Reusable UI components
    │   │   ├── Loading.jsx					# Loading spinner 
    │   │   ├── Modal.jsx					# Modal dialog componen
    │   │   ├── AvatarUpload.jsx			# Avatar upload component
    │   │   ├── SearchBar.jsx				# Search input with styling
    │   │   ├── SearchBar.css				# Search bar specific styles
    │   │   ├── Button.jsx					# Reusable button
    │   │   ├── Input.jsx					# Reusable input field
    │   │   └── Select.jsx					# Reusable select dropdown
    │   ├── 📁 dashboard/					# Dashboard features
    │   │   └── Dashboard.jsx				# Main dashboard component
    │   ├── 📁 issues/						# Issue management
    │   │   ├── Issues.jsx					# Issues list view
    │   │   ├── IssueDetail.jsx				# Single issue detail view
    │   │   ├── IssueCard.jsx				# Issue card for lists
    │   │   ├── CreateIssue.jsx				# Issue creation form
    │   │   ├── IssueFilters.jsx			# Filtering and sorting
    │   │   └── IssueView.jsx				# View toggle (kanban/list)
    │   ├── 📁 layout/						# Application layout
	│   │   ├──Footer.jsx					# Footer
    │   │   ├── Header.jsx					# Top navigation header
    │   │   ├── Sidebar.jsx					# Navigation sidebar
    │   │   └── ThemeToggle.jsx				# Theme switcher
    │   ├── 📁 projects/					# Project management
    │   │   ├── Projects.jsx				# Projects list view
    │   │   ├── ProjectDetail.jsx			# Project detail page
    │   │   ├── ProjectCard.jsx				# Project card component
    │   │   ├── ProjectSettings.jsx			# Project configuration
    │   │   ├── CreateProject.jsx			# Project creation form
    │   │   └── ProjectMembers.jsx			# Team member management
    │   ├── 📁 reports/						# Analytics & reporting
    │   │   ├── Reports.jsx					# Reports dashboard
    │   │   ├── BurndownChart.jsx			# Sprint burndown visualization
    │   │   ├── VelocityChart.jsx			# Team velocity tracking
    │   │   └── Analytics.jsx				# Advanced analytics
    │   ├── 📁 settings/					# User & app settings
    │   │   └── Settings.jsx				# Settings management
    │   ├── 📁 sprints/						# Sprint planning
    │   │   ├── Sprints.jsx					# Sprints overview
    │   │   ├── SprintBoard.jsx				# Kanban board view
    │   │   ├── CreateSprint.jsx			# Sprint creation
    │   │   └── SprintBacklog.jsx			# Backlog management
    │   ├── 📁 users/						# User management
    │   │   └── Users.jsx					# User list and profiles
    │   ├── 📁 workflow/					# Workflow configuration
    │   │   ├── WorkflowManagement.jsx		# Workflow editor
    │   │   ├── StatusManager.jsx			# Status management
    │   │   ├── IssueTypeManager.jsx		# Issue type configuration
    │   │   ├── WorkflowSchemeManager.jsx	# Scheme management
    │   │   └── TransitionManager.jsx		# State transitions
    │   ├── 📁 comments/					# Comment system
    │   │   └── Comments.jsx				# Comment threading
    │   └── 📁 notifications/				# Notification system
    │       └── NotificationToast.jsx		# Toast notifications
    ├── 📁 hooks/							# Custom React hooks
    │   ├── useAuth.js						# Authentication hook 
    │   ├── useLocalStorage.js				# Local storage persistence
    │   └── useEmailServise.js				# Email
    ├── 📁 services/						# External service integrations
    │   └── api.js							# REST API client
    └── 📁 utils/							# Utility functions
        ├── constants.js					# Application constants
        ├── helpers.js						# Common utility functions
        └── formatters.js					# Data formatting
```
---

### Frontend: ###
- cd frontend
- npm install (installs package.json node_modules)
- npm run dev

### Production for Netlify ###
- cd frontend
- npm run build

### Frontend and Backend ###
- Frontend hosted on Netlify https://app.netlify.com/
- Backend hosted on Firebase
---

## Deployment ##
### Deploy to Netlify ###
- Go to app.netlify.com dashboard

- Site settings → Build & deploy

- Set build settings:

- Base directory: frontend

- Build command: npm run build

- Publish directory: frontend/dist

---

```
// Import the functions you need from the SDKs you need
import { initializeApp } from "firebase/app";
import { getAnalytics } from "firebase/analytics";
// TODO: Add SDKs for Firebase products that you want to use
// https://firebase.google.com/docs/web/setup#available-libraries

// Your web app's Firebase configuration
// For Firebase JS SDK v7.20.0 and later, measurementId is optional
const firebaseConfig = {
  apiKey: "AIzaSyBxOvm4kYzzTNsYHE1qzwmLuPtFL5Z4xEY",
  authDomain: "jira-tracker-68ac8.firebaseapp.com",
  projectId: "jira-tracker-68ac8",
  storageBucket: "jira-tracker-68ac8.firebasestorage.app",
  messagingSenderId: "966222397325",
  appId: "1:966222397325:web:e003f1f2f184b7358587c4",
  measurementId: "G-4LXKCDT7KV"
};

// Initialize Firebase
const app = initializeApp(firebaseConfig);
const analytics = getAnalytics(app);


.env
VITE_FIREBASE_API_KEY=AIzaSyBxOvm4kYzzTNsYHE1qzwmLuPtFL5Z4xEY
VITE_FIREBASE_AUTH_DOMAIN=jira-tracker-68ac8.firebaseapp.com
VITE_FIREBASE_PROJECT_ID=jira-tracker-68ac8
VITE_FIREBASE_STORAGE_BUCKET="jira-tracker-68ac8.firebasestorage.app
VITE_FIREBASE_MESSAGING_SENDER_ID966222397325
VITE_FIREBASE_APP_ID=1:966222397325:web:e003f1f2f184b7358587c4
VITE_APP_NAME=Jira Tracker

```
---


## Summary

Your Jira Tracker application is now **complete and ready for deployment**! Here's what you have:

### ✅ Complete Application Features:
- **User Authentication** - Registration, login, profile management
- **Project Management** - Create, edit, delete projects with team members
- **Issue Tracking** - Full issue lifecycle with advanced filtering and sorting
- **Sprint Management** - Agile sprints with burndown charts and velocity tracking
- **Reporting & Analytics** - Comprehensive reports and metrics
- **File Uploads** - Avatar support
- **Real-time Updates** - Live data synchronization
- **Responsive Design** - Mobile-friendly interface
- **Dark/Light Theme** - User preference support

### ✅ Technical Implementation:
- **Frontend**: React 18 + Vite + Tailwind CSS
- **Backend**: Firebase (Auth, Firestore, Storage)
- **Deployment**: Netlify ready
- **Security**: Comprehensive Firebase security rules
- **Performance**: Optimized builds and lazy loading

### ✅ Deployment Ready:
- Environment variables configured
- Netlify configuration complete
- Build scripts ready
- Security rules implemented
