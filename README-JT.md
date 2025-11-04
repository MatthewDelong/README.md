# Jira-Tracker
A comprehensive Jira-like issue tracker and project management website using SQLite
---
## 🖥 Screenshots  

| Page      | Preview |
|-----------|---------|
| Dashboard      | ![Dashboard](https://github.com/user-attachments/assets/c56499a7-b651-48ae-a14f-76bedd278e38) |
| Projects   | ![Projects](https://github.com/user-attachments/assets/ad686dcb-d22f-47ea-af00-a0b62698d9a7)|
| Issues   | ![Issues](https://github.com/user-attachments/assets/1007d1c7-c6d7-4860-ad21-5097b9c5dfbe) |
| Weather   | ![Reports](https://github.com/user-attachments/assets/10ca6c31-7f70-446f-aade-36538bda0988) |


## Backend ##

```
backend/
├── server.js                          # Main server file (you already have this)
├── render-build.sh                    # Render Build Script
├── package.json                       # Backend dependencies
├── .env                               # Environment variables
├── models/
│   ├── User.js                        # User model
│   ├── Project.js                     # Project model
│   ├── Issue.js                       # Issue model
│   ├── Sprint.js                      # Sprint model
│   └── Workflow.js                    # Workflow model
├── routes/
│   ├── auth.js                        # Authentication routes
│   ├── projects.js                    # Project management routes
│   ├── issues.js                      # Issue management routes
│   ├── users.js                       # User management routes
│   ├── sprints.js                     # Sprint management routes
│   ├── comments.js                    
│   ├── attachments.js                 # File attachment routes (❌ Not working)
│   ├── reports.js                     # Reporting routes
│   ├── workflow.js                    # Workflow routes
│   └── search.js
├── middleware/
│   ├── auth.js                        # Authentication middleware
│   ├── upload.js                      # File upload middleware
│   ├── validation.js
│   └── errorHandler.js                # Error handling middleware
├── config/
│   ├── database.js                    # Database configuration
│   └── email.js                       # Email configuration (❌ Not working)
├── database/
│   ├── init.js                        # Database initialization
│   └── jira.db                        # SQLite database file
├── uploads/
│   ├── attachments/                   # Store uploaded attachments (❌ missing - create folder)
│   └── avatars/                       # Store user avatars (❌ missing - create folder)
└── utils/
    ├── helpers.js                     # Utility functions
    └── notifications.js               # Notification utilities (❌ Not working)
```
---
## Frontend ##
```
    frontend/
├── package.json                       # Frontend dependencies
├── vite.config.js                     # Vite configuration
├── postcss.config.js  
├── tailwind.config.js  
├── index.html                         # Main HTML file
├── netlift.toml                       # Configuration file that specifies how Netlify builds and deploy
├── .env                               # Frontend environment variables
├── .env.production                    # Frontend production environment variables
├── public/
│   ├── favicon.ico                    # Icon
│   ├── favicon-32x32.png              # Icon
│	└── apple-touch-icon.png           # Icon
└── src/
    ├── main.jsx                       # React entry point
    ├── App.jsx                        # Main App component
    ├── index.css                      # Global styles
    ├── contexts/
    │   ├── AuthContext.jsx            # Authentication context
    │   ├── SocketContext.jsx          # Socket.io context (❌ missing - create)
    │   ├── ThemeContext.jsx           # Theme context (❌ missing - create)
    │   └── NotificationContext.jsx    # Notification context (❌ missing - create)
    ├── components/
    │   ├── Layout/
    │   │   ├── Layout.jsx             # Main layout component
    │   │   ├── Header.jsx             # Page header
    │   │   ├── Sidebar.jsx            # Navigation sidebar
    │   │   └── ThemeToggle.jsx        # Dark/light theme toggle (❌ missing - create)
	│   ├── comments/
    │   │   └── Comments.jsx           # Commenting
    │   ├── Auth/
    │   │   ├── Login.jsx              # Login form
    │   │   └── Register.jsx           # Registration form
    │   ├── Dashboard/
    │   │   └── Dashboard.jsx          # Dashboard component
    │   ├── Projects/
    │   │   ├── Projects.jsx           # Projects list
    │   │   ├── ProjectDetail.jsx      # Project details
    │   │   ├── ProjectCard.jsx        # Project card component
    │   │   ├── CreateProject.jsx      # Create project form
    │   │   └── ProjectMembers.jsx     # Project members management
    │   ├── Issues/
    │   │   ├── Issues.jsx             # Issues list
    │   │   ├── IssueDetail.jsx        # Issue details
    │   │   ├── IssueCard.jsx          # Issue card component
    │   │   ├── CreateIssue.jsx        # Create issue form
    │   │   ├── IssueFilters.jsx       # Issue filtering
    │   │   └── IssueView.jsx          # Issue view (kanban/list) (❌ missing - create)
    │   ├── Sprints/
    │   │   ├── Sprints.jsx            # Sprints list
    │   │   ├── SprintBoard.jsx        # Sprint board (kanban)
    │   │   ├── CreateSprint.jsx       # Create sprint form
    │   │   └── SprintBacklog.jsx      # Sprint backlog (❌ missing - create)
    │   ├── Workflow/ (❌ missing - create)
    │   │   ├── WorkflowManagement.jsx # Workflow management
    │   │   ├── StatusManager.jsx      # Status management
    │   │   ├── IssueTypeManager.jsx   # Issue type management
    │   │   ├── WorkflowSchemeManager.jsx # Workflow scheme management
    │   │   └── TransitionManager.jsx  # Transition management
    │   ├── Reports/
    │   │   ├── Reports.jsx            # Reports dashboard
    │   │   ├── BurndownChart.jsx      # Burndown chart
    │   │   ├── VelocityChart.jsx      # Velocity charta
    │   │   └── Analytics.jsx          # Analytics dashboard
    │   ├── Users/
    │   │   └── Users.jsx              # Users
    │   ├── Common/ 
    │   │   ├── Loading.jsx            # Loading spinner (❌ missing - create)
    │   │   ├── Modal.jsx              # Modal dialog (❌ missing - create)
    │   │   ├── SearchBar.jsx          # Search component 
    │   │   ├── SearchBar.css          # Search component 
    │   │   ├── Button.jsx             # Reusable button (❌ missing - create)
    │   │   ├── Input.jsx              # Reusable input (❌ missing - create)
    │   │   └── Select.jsx             # Reusable select (❌ missing - create)
    │   └── Notifications/
    │       └── NotificationToast.jsx  # Notification toast (❌ missing - create)
    ├── hooks/
    │   ├── useAuth.js                 # Authentication hook (❌ missing - create)
    │   ├── useSocket.js               # Socket.io hook (❌ missing - create)
    │   ├── useLocalStorage.js         # Local storage hook
    │   ├── useApi.js                  # API call hook
    │   └── useDebounce.js             # Debounce hook
    ├── services/
    │   ├── api.js                     # API service functions
    │   └── socket.js                  # Socket service (❌ missing - create)
    └── utils/
        ├── constants.js               # App constants
        ├── helpers.js                 # Utility functions
        └── formatters.js              # Data formatting functions (❌ missing - create)
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
