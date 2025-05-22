# Modern Todo List Application

A full-stack Todo List application built with React, TypeScript, and Node.js. This application features advanced task management with Slack integration for notifications and Google's Gemini AI API for intelligent task summarization.

## 🚀 Features

- ✨ Create, Read, Update, and Delete todos
- 🎯 Set priority levels (low, medium, high)
- 📅 Add due dates to tasks
- ✅ Mark tasks as completed
- 🎨 Modern and responsive UI
- 🌈 Visual priority indicators
- 📱 Mobile-friendly design
- 🤖 AI-Powered Task Summarization using Gemini API
- 💬 Slack Integration Features:
  - Receive task notifications in your Slack channel
  - Daily task summaries
  - Due date reminders
  - Priority task alerts

## 🏗️ Tech Stack

### Frontend
- React with TypeScript
- Material-UI (MUI) for styling
- Vite for build tooling

### Backend
- Node.js with TypeScript
- Express.js
- Prisma ORM
- SQLite database

### Integrations
- 🤖 Google Gemini API for AI task summarization
- 💬 Slack API for notifications and reminders

## 📦 Project Structure

```
todo-list/
├── frontend/                # React frontend application
│   ├── src/
│   │   ├── components/     # React components
│   │   ├── App.tsx        # Main application component
│   │   └── main.tsx       # Application entry point
│   └── package.json
│
└── backend/                # Node.js backend application
    ├── src/
    │   ├── controllers/   # Request handlers
    │   ├── routes/        # API routes
    │   ├── services/      # Business logic
    │   └── types/         # TypeScript types
    └── package.json
```

## 🚀 Getting Started

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Sahith53/todo-list.git
   cd todo-list
   ```

2. Install Backend Dependencies:
   ```bash
   cd backend
   npm install
   ```

3. Set up the database:
   ```bash
   npx prisma migrate dev
   ```

4. Install Frontend Dependencies:
   ```bash
   cd ../frontend
   npm install
   ```

### Running the Application

1. Start the Backend Server:
   ```bash
   cd backend
   npm run dev
   ```

2. Start the Frontend Development Server:
   ```bash
   cd frontend
   npm run dev
   ```

The application will be available at `http://localhost:5173`

## 🎯 API Endpoints

### Todos
- `GET /api/todos` - Get all todos
- `POST /api/todos` - Create a new todo
- `PUT /api/todos/:id` - Update a todo
- `DELETE /api/todos/:id` - Delete a todo

### Summary
- `GET /api/summary` - Get AI-generated summary of all tasks
- `GET /api/summary/daily` - Get daily task summary
- `GET /api/summary/priority` - Get summary of priority tasks

### Slack Integration
- `POST /api/slack/notify` - Send task notification to Slack
- `POST /api/slack/summary` - Send task summary to Slack

## 💡 Usage

1. **Creating a Todo**
   - Click the "Add Todo" button
   - Fill in the title, description, priority, and due date
   - Click "Save" to create the todo

2. **Updating a Todo**
   - Click the edit icon on any todo
   - Modify the details in the popup form
   - Click "Save" to update

3. **Completing a Todo**
   - Click the checkbox next to the todo title
   - The todo will be marked as completed

4. **Deleting a Todo**
   - Click the delete icon on any todo
   - Confirm the deletion

### Task Summarization
- Click the "Generate Summary" button to get an AI-powered overview of your tasks
- Summaries include:
  - Task grouping by priority
  - Upcoming deadlines
  - Progress tracking
  - Time management suggestions

### Slack Integration
1. **Setting up Slack**
   - Go to Settings
   - Click "Connect to Slack"
   - Authorize the application
   - Select your preferred notification channel

2. **Notification Settings**
   - Configure notification preferences
   - Set summary delivery schedule
   - Choose priority levels for notifications
   - Enable/disable specific notification types

## 🎨 UI Features

- Color-coded priority levels
- Clean and intuitive interface
- Responsive design for all screen sizes
- Visual feedback for actions
- Sort and filter capabilities

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👤 Author

Sahith53

## 🙏 Acknowledgments

- Material-UI for the beautiful components
- React community for the amazing tools
- All contributors who help improve this project

## 🔐 Environment Setup

Create a `.env` file in the backend directory with the following variables:

```env
# Database
DATABASE_URL="file:./dev.db"

# Gemini AI API
GEMINI_API_KEY=your_gemini_api_key

# Slack Integration
SLACK_BOT_TOKEN=your_slack_bot_token
SLACK_SIGNING_SECRET=your_slack_signing_secret
SLACK_CHANNEL_ID=your_channel_id
```
