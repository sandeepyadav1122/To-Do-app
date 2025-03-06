# Modern Todo App

A modern, minimalistic Todo App built with Next.js, React, Tailwind CSS, and TypeScript. This project provides a clean and user-friendly interface for managing tasks efficiently.

## Features

- **Task Management**: Add, edit, and delete tasks easily.
- **Dark Mode Support**: Seamless theme switching between light and dark mode.
- **Smooth Transitions**: Optimized animations for a better user experience.
- **Fully Responsive**: Works across all devices.
- **State Management**: Efficiently manages state using React hooks.

## Technologies Used

- [Next.js 14](https://nextjs.org/)
- [React 18](https://react.dev/)
- [Tailwind CSS](https://tailwindcss.com/)
- [TypeScript](https://www.typescriptlang.org/)
- [Framer Motion](https://www.framer.com/motion/) (For animations)
- [Lucide React](https://lucide.dev/) (For icons)

## Installation

To set up the project locally, follow these steps:

```sh
# Clone the repository
git clone https://github.com/sandeepyadav1122/To-Do-app.git

# Navigate into the project directory
cd modern-todo-app

# Install dependencies
npm install
```

## Running the Project

Start the development server:

```sh
npm run dev
```

The app will be available at `http://localhost:3000/`.

## Folder Structure

```
modern-todo-app/
├── components/      # Reusable UI components
├── pages/           # Next.js pages (Routing)
├── styles/          # Global CSS and Tailwind setup
├── public/          # Static assets
├── package.json     # Dependencies and scripts
└── tsconfig.json    # TypeScript configuration
```

## Code Explanation

### `page.tsx`

```tsx
import TodoApp from "@/components/todo-app"

export default function Home() {
  return (
    <main className="min-h-screen flex items-center justify-center p-4 bg-gradient-to-br from-slate-50 to-slate-100 dark:from-slate-900 dark:to-slate-800 transition-colors duration-300">
      <TodoApp />
    </main>
  )
}
```

- This is the main entry point of the application.
- It renders the `TodoApp` component inside a styled `<main>` container.
- Implements smooth color transitions for dark/light mode support.

### `globals.css`

```css
@tailwind base;
@tailwind components;
@tailwind utilities;

:root {
  --foreground-rgb: 0, 0, 0;
  --background-start-rgb: 248, 250, 252;
  --background-end-rgb: 241, 245, 249;
}

.dark {
  --foreground-rgb: 255, 255, 255;
  --background-start-rgb: 15, 23, 42;
  --background-end-rgb: 30, 41, 59;
}
```

- Defines global styles and theme colors.
- Implements smooth transitions for UI elements.

### `tailwind.config.js`

```js
module.exports = {
  darkMode: ["class"],
  content: [
    "./pages/**/*.{js,ts,jsx,tsx,mdx}",
    "./components/**/*.{js,ts,jsx,tsx,mdx}",
    "./app/**/*.{js,ts,jsx,tsx,mdx}",
    "*.{js,ts,jsx,tsx,mdx}",
  ],
  theme: {
    extend: {
      colors: {
        primary: {
          DEFAULT: "hsl(var(--primary))",
          foreground: "hsl(var(--primary-foreground))",
        },
      },
      animation: {
        "fade-in": "fadeIn 0.3s ease-in-out",
      },
      keyframes: {
        fadeIn: {
          "0%": { opacity: 0 },
          "100%": { opacity: 1 },
        },
      },
    },
  },
  plugins: [require("tailwindcss-animate")],
}
```

- Configures Tailwind CSS with dark mode support.
- Defines custom animations and color themes.

## Screenshots


![Image](https://github.com/user-attachments/assets/fad1cca1-b783-4046-8308-0feec698c68f)

## Use Cases

1. **Personal Task Management**: Organize daily tasks and track progress.
2. **Team Collaboration**: Use shared lists for team productivity.
3. **Project Planning**: Manage deadlines and project milestones.

## Future Enhancements

- **User Authentication**: Implement login/signup functionality.
- **Database Integration**: Persist tasks using a database.
- **Advanced Filters**: Categorize tasks based on priority and deadlines.

## Contributing

Contributions are welcome! Feel free to open issues and submit pull requests.


