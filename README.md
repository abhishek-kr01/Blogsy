---

## ✅ `README.md` — For Blogsy (MERN + AI Blog Platform)

```markdown
# 📝 Blogsy – AI-Powered Blogging Platform

**Blogsy** is a modern, full-stack blogging application built using the **MERN stack**. It enables admins to create, manage, and publish blog content efficiently with the help of an integrated AI content generator powered by Gemini. Users can browse categorized blogs, search content, and interact via comments — all in a clean, responsive UI.

---

## 🚀 Features

### ✅ User-Side

- Browse all published blogs
- View detailed blog posts
- Search blog content by title
- Explore blogs by category
- Read AI-generated articles

### 🔐 Admin Panel

- Admin login authentication
- Add new blogs with Quill editor
- Auto-generate content using Gemini API
- Upload blog thumbnail via ImageKit
- View dashboard analytics
- Moderate and approve/delete comments
- Toggle publish status of any blog

---

## 🛠 Tech Stack

| Area         | Technology                              |
| ------------ | --------------------------------------- |
| Frontend     | React.js, Tailwind CSS, Vite            |
| Backend      | Node.js, Express.js                     |
| Database     | MongoDB (with Mongoose)                 |
| AI Support   | Gemini API (Google AI)                  |
| Auth         | JWT-based middleware                    |
| File Upload  | ImageKit + Multer                       |
| Editor       | Quill.js (Rich Text Editor)             |
| State Mgmt   | React Context                           |
| Notification | react-hot-toast                         |
| Deployment   | Vercel (Client) & Render/Other (Server) |

---

## 📂 Folder Structure

```

BLOGSY/
├── client/                # React Frontend
│   ├── public/
│   ├── src/
│   │   ├── assets/
│   │   ├── components/
│   │   │   └── admin/
│   │   ├── context/
│   │   ├── pages/
│   │   │   └── admin/
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── .env
│
├── server/                # Express Backend
│   ├── configs/           # DB, Gemini, ImageKit configs
│   ├── controllers/       # Logic handlers
│   ├── middleware/        # Auth & Multer
│   ├── models/            # Blog & Comment schemas
│   ├── routes/            # blogRoutes & adminRoutes
│   ├── server.js
│   └── .env
└── README.md

```

---

## ⚙️ Setup Instructions

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/abhishek-kr01/Blogsy.git
cd blogsy
```

---

### 2️⃣ Set Up Backend

```bash
cd server
npm install
```

#### Create `server/.env` file:

```env
MONGODB_URI=your_mongodb_connection_string

# ImageKit (for blog thumbnails)
IMAGEKIT_PUBLIC_KEY=your_imagekit_public_key
IMAGEKIT_PRIVATE_KEY=your_imagekit_private_key
IMAGEKIT_URL_ENDPOINT=your_imagekit_endpoint

# Gemini API
GEMINI_API_KEY=your_gemini_api_key
```

#### Run the backend:

```bash
npm run dev
```

---

### 3️⃣ Set Up Frontend

```bash
cd ../client
npm install
```

#### Create `client/.env` file:

```env
VITE_BASE_URL=http://localhost:5000
```

#### Run the frontend:

```bash
npm run dev
```

---

## 🔑 Admin Panel Access

- Visit: `http://localhost:5173/admin`
- Login credentials are verified using the `/api/admin/login` route.
- Authenticated routes are protected using JWT.

---

## 🧠 AI Blog Generation

- Click "Generate with AI" in the blog editor.
- It uses your `GEMINI_API_KEY` to fetch content ideas and text.
- Output is injected directly into the Quill editor.

---

## 💾 API Routes Overview

### Blog Routes (`/api/blog`)

- `POST /add` – Add a new blog (with image)
- `GET /all` – Fetch all published blogs
- `GET /:blogId` – Fetch single blog by ID
- `POST /add-comment` – Add comment
- `POST /comments` – Get comments
- `POST /toggle-publish` – Publish/unpublish a blog
- `POST /generate` – Generate content using AI

### Admin Routes (`/api/admin`)

- `POST /login` – Admin login
- `GET /blogs` – Get all blogs (admin view)
- `GET /comments` – Get all comments
- `POST /approve-comment` – Approve comment
- `POST /delete-comment` – Delete comment
- `GET /dashboard` – Get blog & comment stats

---

## 🙋‍♂️ Author

Built with ❤️ by **Abhishek Kumar**

- 🔗 [LinkedIn](https://www.linkedin.com/in/abhishek-kumar-6202249339ak/)
- 🔗 [GitHub](https://github.com/abhishek-kr01)
