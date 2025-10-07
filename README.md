# 🍳 Flavoriz - Recipe Blog Platform

A modern, full-stack recipe sharing platform built with Vue.js and NestJS. Discover, share, and explore delicious recipes from around the world with an intuitive and beautiful user interface.

## ✨ Features

### 🏠 **Home & Discovery**

- **Hero Section**: Beautiful landing page with featured recipes
- **Popular Recipes**: Discover trending and popular recipes
- **Search & Filter**: Advanced filtering by tags, cooking time, and ingredients
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices

### 👤 **User Management**

- **Authentication**: Secure user registration and login
- **JWT Authentication**: Token-based authentication with cookies
- **User Profiles**: Personal profile pages with recipe collections
- **Bookmark System**: Save and organize favorite recipes

### 📝 **Recipe Management**

- **Recipe Creation**: Add new recipes with detailed instructions
- **Recipe Viewing**: Beautiful recipe detail pages with step-by-step instructions
- **Recipe Listing**: Paginated recipe browsing with search functionality
- **Tag System**: Organize recipes with custom tags
- **Image Support**: Recipe images for visual appeal

## 🛠️ Tech Stack

### Frontend

- **Vue 3** - Progressive JavaScript framework
- **TypeScript** - Type-safe development
- **Vite** - Fast build tool and dev server
- **Vue Router** - Client-side routing
- **Pinia** - State management
- **Tailwind CSS** - Utility-first CSS framework

### Backend

- **NestJS** - Progressive Node.js framework
- **MongoDB** - NoSQL database
- **JWT** - JSON Web Token authentication

## 🚀 Getting Started

### Prerequisites

- Node.js (v18 or higher)
- MongoDB (local or cloud instance)
- npm or yarn package manager

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/flavoriz.git
   cd flavoriz
   ```

2. **Install dependencies**

   ```bash
   # Install server dependencies
   cd server
   npm install

   # Install client dependencies
   cd ../client
   npm install
   ```

3. **Environment Setup**

   Create a `.env` file in the `server` directory:

   ```env
   MONGODB_URI=mongodb://localhost:27017/flavoriz
   JWT_SECRET=your-super-secret-jwt-key
   JWT_EXPIRES_IN=7d
   ```

4. **Start the development servers**

   **Terminal 1 - Backend Server:**

   ```bash
   cd server
   npm run dev
   ```

   Server will run on `http://localhost:3000`

   **Terminal 2 - Frontend Client:**

   ```bash
   cd client
   npm run dev
   ```

   Client will run on `http://localhost:5173`

## 📁 Project Structure

```
flavoriz/
├── client/                 # Vue.js frontend application
│   ├── src/
│   │   ├── components/     # Reusable Vue components
│   │   │   ├── Home/       # Home page components
│   │   │   ├── Profile/    # User profile components
│   │   │   ├── Recipes/    # Recipe-related components
│   │   │   └── ui/         # UI component library
│   │   ├── views/          # Page components
│   │   ├── router/         # Vue Router configuration
│   │   ├── stores/         # Pinia state management
│   │   └── helper/         # Utility functions
│   └── public/             # Static assets
├── server/                 # NestJS backend application
│   ├── src/
│   │   ├── auth/           # Authentication module
│   │   ├── recipes/        # Recipes module
│   │   ├── schemas/        # MongoDB schemas
│   │   └── main.ts         # Application entry point
│   └── dist/               # Compiled JavaScript
└── README.md
```

