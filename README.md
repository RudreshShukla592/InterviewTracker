# Interview Practice Tracker

A simple and lightweight **Interview Practice Tracker** built with React and Tailwind CSS to help track DSA, interview, and machine-coding preparation.

🔗 **Live Demo:** [Interview Practice Tracker](https://interview-tracker-inky.vercel.app/?utm_source=chatgpt.com)

## Features

- Add interview practice questions
- Categorize questions into:
  - DSA
  - Interview
  - Machine Coding
- Set question difficulty:
  - Easy
  - Medium
  - Hard
- Mark questions as completed or pending
- Delete questions
- Search questions by title
- Filter questions by:
  - Category
  - Difficulty
  - Completion status
- View overall preparation progress
- View total question counts by category
- Persist questions using browser `localStorage`
- Responsive UI built with Tailwind CSS

## Tech Stack

- **React**
- **Tailwind CSS**
- **Context API** – global question state management
- **React Hook Form** – form handling and validation
- **Lucide React** – icons
- **LocalStorage** – client-side data persistence
- **Vercel** – deployment

## Getting Started

### 1. Clone the repository

```bash
git clone git@github.com:RudreshShukla592/InterviewTracker.git
```

### 2. Navigate into the project

```bash
cd interview-practice-tracker
```

### 3. Install dependencies

```bash
npm install
```

### 4. Start the development server

```bash
npm run dev
```

The application will be available at the local URL shown by Vite, usually:

```text
http://localhost:5173
```

## Build for Production

```bash
npm run build
```

To preview the production build locally:

```bash
npm run preview
```

## How It Works

The application keeps the complete list of questions as the main source of truth using React Context API.

Filtering is handled separately to create a display list based on the selected search, category, difficulty, and completion filters.

Question data is persisted in the browser's `localStorage`, so refreshing the page does not remove previously added questions.

The basic data flow is:

```text
Questions
    ↓
Context API
    ↓
Search / Filters
    ↓
Filtered Questions
    ↓
Question List
    ↓
Question Cards
```

## Assumptions

- The tracker is intended for a **single user**.
- No backend or database is required.
- Question data is stored only in the browser's `localStorage`.
- Data is therefore specific to the browser/device being used.
- Clearing browser storage will remove the saved questions.
- No authentication or user accounts are implemented.
- Question IDs are generated using `Date.now()`.
- Completion status is represented using a boolean `isCompleted` field.
- The application is designed as a simple personal productivity tool rather than a multi-user interview platform.

## Project Structure

```text
src/
├── components/
│   ├── Dashboard/
│   │   ├── Dashboard.jsx
│   │   ├── Stats.jsx
│   │   └── ProgressBar.jsx
│   │
│   ├── QuestionForm/
│   │   └── QuestionForm.jsx
│   │
│   ├── Filters/
│   │   └── Filters.jsx
│   │
│   └── QuestionList/
│       ├── QuestionList.jsx
│       └── QuestionCard.jsx
│
├── context/
│   └── MyContext.jsx
│
├── App.jsx
└── main.jsx
```

## Future Improvements

Some possible improvements for a future version:

- Edit existing questions
- Add notes or solution links
- Add interview/company tags
- Add sorting options
- Add question difficulty statistics
- Export/import questions
- Add backend persistence
- Add authentication and user accounts
- Add dark mode

## License

This project is built for learning and personal use.
