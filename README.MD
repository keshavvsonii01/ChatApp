🌐 CONNEXT — Real-Time Chat WebApp

CONNEXT is a modern full-stack real-time chat web application built with React, Node.js, Express, MongoDB, and Socket.io.
It allows users to connect, communicate, and share messages instantly with live updates — all wrapped in a clean, responsive, and interactive UI built using TailwindCSS.

🚀 Features

✅ User Authentication — Secure JWT-based login and signup
✅ Real-Time Messaging — Instant chat updates using Socket.io
✅ Online/Offline Status — Track connected users in real time
✅ Cloudinary Integration — Image upload support for user profiles or messages
✅ Responsive UI — Optimized for both desktop and mobile screens
✅ Toast Notifications — Instant feedback using react-hot-toast
✅ Scalable Architecture — Clean separation of frontend and backend logic

🧠 Tech Stack

Frontend
⚛️ React 19
⚡ Vite with TailwindCSS
🔥 React Hot Toast
🔗 React Router DOM 7
💬 Socket.io Client 4
🌐 Axios for HTTP requests
🎨 TailwindCSS 4

Backend
🚀 Express 5
🧱 MongoDB + Mongoose 8
🔐 JWT (jsonwebtoken) for authentication
🔑 bcryptjs for password hashing
☁️ Cloudinary for image uploads
🌍 CORS configuration
💻 Socket.io 4.8 for real-time connections
🔄 Nodemon for live server reload during development

📁 Folder Structure

CONNEXT
│
├── backend
│ ├── server.js
│ ├── config
│ ├── controllers
│ ├── models
│ ├── routes
│ ├── utils
│ └── .env
│
├── frontend
│ ├── src
│ │ ├── components
│ │ ├── pages
│ │ ├── context
│ │ ├── utils
│ │ └── App.jsx
│ ├── tailwind.config.js
│ ├── vite.config.js
│ └── package.json
│
└── README.txt

🧩 Installation & Setup Guide

Follow these steps to set up and run CONNEXT on your local machine 👇

🖥️ Step 1: Clone the Repository
git clone https://github.com/avvii/ChatApp.git

cd connext

⚙️ Step 2: Setup the Backend
Navigate to the backend folder
cd backend

📦 Install dependencies
npm install

⚙️ Create a .env file in the backend folder and add these environment variables

PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

▶️ Run the backend server
npm run dev
Backend will start on http://localhost:5000

💻 Step 3: Setup the Frontend
Navigate to the frontend folder
cd ../frontend

📦 Install dependencies
npm install

⚙️ Configure Backend URL
Make sure your Axios base URL or Socket connection points to your backend
Example:
const socket = io("http://localhost:5000
", {
query: { userId: currentUser._id },
});

▶️ Start the frontend
npm run dev
Frontend will run on http://localhost:5173

🌐 Step 4: Run Both Together
Frontend → http://localhost:5173

Backend → http://localhost:5000

Open the frontend in your browser and start using CONNEXT 🎉

🔌 Socket.io Integration

Socket.io enables live, real-time communication between users.

Example client-side connection:
import { io } from "socket.io-client";

const socket = io("http://localhost:5000
", {
query: { userId: currentUser._id },
});

socket.on("connect", () => {
console.log("Connected to Socket.io server");
});

The backend manages user connections, online status, and broadcasts messages to active users.


💡 Future Improvements

💬 Group chat functionality
🔔 Push notifications
📁 File and media sharing
🟢 Message read receipts
📱 PWA support for mobile users
🧠 AI-assisted auto-replies (future idea)

🧑‍💻 Author

👨‍💻 Avishi — Full Stack Developer
Building interactive web experiences with modern JavaScript stacks.

GitHub: https://github.com/avvii


🪪 License

This project is licensed under the MIT License.
Feel free to use, modify, and build upon it.

⭐ If you like this project, don’t forget to star the repo!

“CONNEXT — Connecting people, one message at a time.”
