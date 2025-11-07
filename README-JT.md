# Jira-Tracker 07/11/2025
A comprehensive Jira-like issue tracker and project management website using SQLite
---
---
## 🖥 Screenshots  

| Page      | Preview |
|-----------|---------|
| Dashboard      | ![Dashboard](https://github.com/user-attachments/assets/13f3a877-3c2f-4d1a-9494-783690d1e84f) |
| Projects   | ![Projects](https://github.com/user-attachments/assets/80116275-a33f-402f-a0dc-a4572634e60b) |
| Issues   | ![Issues](https://github.com/user-attachments/assets/fbd9605e-5716-4292-a128-a96c473df149) |
| Issues Page   |![Issue_Card](https://github.com/user-attachments/assets/928cfebf-ae8d-4472-90f7-d0d9662f4ab1)  |
| Reports   | ![Reports](https://github.com/user-attachments/assets/7e4c7463-0951-4c0d-980f-afbf12fb2e7d) |
| Settings   | ![Settings](https://github.com/user-attachments/assets/3b86a018-de2b-4bb8-a9a2-108b7dca1a37) |

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
├── 📁 public/								# Static assets
│   ├── logo.png							# Logo banner
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
    │   ├── ThemeContext.jsx				# Light/dark theme management
    │   └── NotificationContext.jsx			# Notification state
    ├── 📁 components/						# React components organized by feature
    │   ├── 📁 auth/						# Authentication components
    │   │   ├── Login.jsx					# Login form component
    │   │   └── Register.jsx				# Registration form component
    │   ├── 📁 common/						# Reusable UI components
    │   │   ├── Loading.jsx					# Loading spinner
    │   │   ├── Modal.jsx					# Modal dialog component
    │   │   ├── AvatarUpload.jsx			# Avatar upload component
    │   │   ├── SearchBar.jsx				# Search input with styling  (⚠️ Create)
    │   │   ├── SearchBar.css				# Search bar specific styles  (⚠️ Create)
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
    │   │   ├── Layout.jsx					# Main layout wrapper
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
    │   ├── useSocket.js					# WebSocket hook (⚠️ Create)
    │   ├── useLocalStorage.js				# Local storage persistence
    │   ├── useApi.js						# API call abstraction (⚠️ Create)
    │   └── useDebounce.js					# Debounced input handling (⚠️ Create)
    ├── 📁 services/						# External service integrations
    │   ├── api.js							# REST API client
    │   └── socket.js						# WebSocket service (⚠️ Create)
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



