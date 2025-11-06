# Jira-Tracker 05/11/2025
A comprehensive Jira-like issue tracker and project management website using SQLite
---
---
## 🖥 Screenshots  

| Page      | Preview |
|-----------|---------|
| Dashboard      | ![Dashboard](https://github.com/user-attachments/assets/6273e013-48d1-4912-97d9-19b538eb850f) |
| Projects   | ![Projects](https://github.com/user-attachments/assets/1af2986d-1405-4836-ad09-f413c0a4a728) |
| Issues   | ![Issues](https://github.com/user-attachments/assets/71fbdab5-6320-4c91-b50d-ce4a82176337) |
| Issues Page   | ![Issue_Page](https://github.com/user-attachments/assets/447c0130-14b9-410e-8d2d-cba3f63cc50d) |
| Reports   | ![Reports](https://github.com/user-attachments/assets/06bcac83-8242-431a-879a-8398e4969cfe) |
| Settings   | ![Settings](https://github.com/user-attachments/assets/5b9c9235-dc88-4e12-a886-dab6f39ac274) |

---
## Backend ##

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
    │   ├── SocketContext.jsx				# WebSocket connections (⚠️ Create)
    │   ├── ThemeContext.jsx				# Light/dark theme management (⚠️ Create)
    │   └── NotificationContext.jsx			# Notification state (⚠️ Create)
    ├── 📁 components/						# React components organized by feature
    │   ├── 📁 auth/						# Authentication components
    │   │   ├── Login.jsx					# Login form component
    │   │   └── Register.jsx				# Registration form component
    │   ├── 📁 common/						# Reusable UI components
    │   │   ├── Loading.jsx					# Loading spinner (⚠️ Create)
    │   │   ├── Modal.jsx					# Modal dialog component (⚠️ Create)
    │   │   ├── AvatarUpload.jsx			# Avatar upload component
    │   │   ├── SearchBar.jsx				# Search input with styling
    │   │   ├── SearchBar.css				# Search bar specific styles
    │   │   ├── Button.jsx					# Reusable button (⚠️ Create)
    │   │   ├── Input.jsx					# Reusable input field (⚠️ Create)
    │   │   └── Select.jsx					# Reusable select dropdown (⚠️ Create)
    │   ├── 📁 dashboard/					# Dashboard features
    │   │   └── Dashboard.jsx				# Main dashboard component
    │   ├── 📁 issues/						# Issue management
    │   │   ├── Issues.jsx					# Issues list view
    │   │   ├── IssueDetail.jsx				# Single issue detail view
    │   │   ├── IssueCard.jsx				# Issue card for lists
    │   │   ├── CreateIssue.jsx				# Issue creation form
    │   │   ├── IssueFilters.jsx			# Filtering and sorting
    │   │   └── IssueView.jsx				# View toggle (kanban/list) (⚠️ Create)
    │   ├── 📁 layout/						# Application layout
    │   │   ├── Layout.jsx					# Main layout wrapper
    │   │   ├── Header.jsx					# Top navigation header
    │   │   ├── Sidebar.jsx					# Navigation sidebar
    │   │   └── ThemeToggle.jsx				# Theme switcher (⚠️ Create)
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
    │   │   └── SprintBacklog.jsx			# Backlog management (⚠️ Create)
    │   ├── 📁 users/						# User management
    │   │   └── Users.jsx					# User list and profiles
    │   ├── 📁 workflow/					# Workflow configuration (⚠️ Create)
    │   │   ├── WorkflowManagement.jsx		# Workflow editor
    │   │   ├── StatusManager.jsx			# Status management
    │   │   ├── IssueTypeManager.jsx		# Issue type configuration
    │   │   ├── WorkflowSchemeManager.jsx	# Scheme management
    │   │   └── TransitionManager.jsx		# State transitions
    │   ├── 📁 comments/					# Comment system
    │   │   └── Comments.jsx				# Comment threading
    │   └── 📁 notifications/				# Notification system
    │       └── NotificationToast.jsx		# Toast notifications (⚠️ Create)
    ├── 📁 hooks/							# Custom React hooks
    │   ├── useAuth.js						# Authentication hook (⚠️ Create)
    │   ├── useSocket.js					# WebSocket hook (⚠️ Create)
    │   ├── useLocalStorage.js				# Local storage persistence
    │   ├── useApi.js						# API call abstraction
    │   └── useDebounce.js					# Debounced input handling
    ├── 📁 services/						# External service integrations
    │   ├── api.js							# REST API client
    │   └── socket.js						# WebSocket service (⚠️ Create)
    └── 📁 utils/							# Utility functions
        ├── constants.js					# Application constants
        ├── helpers.js						# Common utility functions
        └── formatters.js					# Data formatting (⚠️ Create)
```
---
### Backend: ###
- cd backend
- npm install  (installs package.json node_modules)
- npm run init-db
- npm run dev

### Frontend: ###
- cd frontend
- npm install (installs package.json node_modules)
- npm run dev

### Production for Netlify ###
- cd frontend
- npm run build

### Updating Database ###
- cd backend
- npm run init-db

### Frontend and Backend ###
- Frontend hosted on Netlify https://app.netlify.com/
- Backend hosted on Render https://render.com/

### Default Login ###
- 👤 Admin: admin@jira.com / admin123
- 👤 Admin: user@jira.com / user123
---

## Deployment ##
### Deploy to Netlify ###
- Go to app.netlify.com dashboard

- Site settings → Build & deploy

- Set build settings:

- Base directory: frontend

- Build command: npm run build

- Publish directory: frontend/dist

- Environment variables:
```
VITE_API_URL = https://jira-tracker-backend-w2t5.onrender.com/api
```
---

### Deploy to Render.com (Backend) ###
- Go to Render.com dashboard

- Click "New +" → "Web Service"

- Connect your GitHub repository

- Configure Web Service:

- Build Settings:

- Name: jira-tracker-backend

- Environment: Node

- Region: Choose closest to you

- Branch: main (or your production branch)

- Root Directory: backend

- Build Command: chmod +x render-build.sh && ./render-build.sh

- Start Command: npm start

- Environment Variables (in Render dashboard):

```
NODE_ENV=production
JWT_SECRET=7ece0cf59177a4922b54aba50699e61bc084117ec1632bce457c14a92e4db138
DB_PATH=./database/jira.db
CLIENT_URL=https://jira-tracker.netlify.app

```
---


