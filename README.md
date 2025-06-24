<h1 align="center">Relay — Real-Time Full-Stack Messaging Platform</h1>
<p align="center"><a href="#project-description">Project Description</a> - <a href="#key-features">Key Features</a> - <a href="#technology-stack">Tech Stack</a> - <a href="#Getting Started">Getting Started</a></p>

<img src="" alt="" align="center" width="auto" height="auto">

## Project Description

**Relay** is a fully functional, real-time messaging platform built with a modern tech stack. It allows users to sign up, log in, view other users, and exchange messages instantly. The app supports both text and media messages, and provides a responsive, dark-themed interface for a polished user experience.

The backend securely manages user authentication and session handling, while the frontend offers a smooth messaging experience with dynamic updates and media previews.

## Key Features

**User Authentication:**

*   Secure sign up and login using **bcryptjs** for password hashing.
*   **JWT-based** token system stored in HTTP-only cookies for session protection.
*   Option to persist sessions or expire on browser close.

**Real Time Messaging**:

*   Instant delivery of messages using **WebSockets**.
*   Automatic message updates between users without needing refresh.

**Media Sharing:**

*   Supports sending images and videos in chat.
*   Media files are uploaded to **Cloudinary** and rendered with inline previews.

**User Presence:**

*   Dynamically displays which users are currently online.
*   User list updates in real time based on socket connection state.

**Polished UI/UX:**

*   Built with **TailwindCSS**, **Radix UI**, and **ShadCN** components.
*   Dark mode styling across all pages.
*   Profile dropdown with logout and user info options.

**Modular Architecture:**

*   Backend uses **Express.js** (ESM) with clear separation of routes, controllers, models, and middlewares.
*   Frontend uses Next.js App Router, with context for global user state, organized components, and axios-based API communication.

## Tech Stack

| Layer        | Technology                                  |
| ------------ | ------------------------------------------- |
| Frontend     | Next.js 14, TailwindCSS, ShadCN, Radix UI   |
| Backend      | Express.js, **bcryptjs** for password hashing, JWT, Cookie Parser |
| Database     | MongoDB with Mongoose ODM                   |
| Realtime     | Native WebSockets                           |
| Media Upload | Cloudinary                                  |
| Auth         | JWT + HTTP-only Cookies                     |

## Getting Started

To get this project up and running locally, follow the steps below.

**1.Clone the repository**
```
git clone https://github.com/ManchalaSashank/Relay.git
cd relay
```

**2.Install Dependencies(Backend)**
```
cd server
npm install
```
Now create .env file inside your /server folder with the following content
```
PORT=4000  
MONGO_URL=your_mongodb_connection_string
JWT_SECRET=your_super_secret_key
CLIENT_URL=http://localhost:3000

# Cloudinary (for media uploads)
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
```
To get your Cloudinary credentials, go to https://cloudinary.com/ and register your account.
Then under the API keys section, find the necessary credentials and use them.

Now start the server
```
node index.js
```

**3.Install Dependencies(Frontend)**
```
cd ../client
npm install
```
Now start the Frontend
```
npm run dev
```
Open http://localhost:3000 with your browser to see the result.


