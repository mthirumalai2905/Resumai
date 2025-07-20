# 🧠 ResumeMind – AI-Powered Resume Review

**ResumeMind** is an AI-powered resume review web application that helps users improve their resumes using intelligent feedback. Built with **React 17**, **React Router**, and **Puter**, this app combines frontend simplicity with powerful cloud and AI features.

---

## 🚀 Features

- 🖼 Upload and preview resume (PDF/image)
- 🧠 AI-generated feedback including:
  - Resume Summary
  - ATS (Applicant Tracking System) Score
  - Detailed suggestions
- ☁️ Cloud file storage and resume image rendering
- ⚙️ Virtual compute to run AI models for analysis
- 🔐 User authentication and route protection
- 📦 Key-value store for metadata and feedback
- 🌐 React Router-based navigation

---

## 🧠 How It Works

### 1. Upload & Display
- Users upload a PDF resume
- It's stored using Puter’s file system
- Converted to image and displayed via secure `Blob` URLs

### 2. AI Feedback (Virtual Compute)
- Once uploaded, an AI model is triggered via Puter’s virtual compute
- The model analyzes the resume and returns:
  - Summary section
  - ATS score with suggestions
  - Detailed analysis

### 3. Storage
- Resume file and image are stored using `fs` API (Puter)
- Feedback and metadata stored using `kv` (key-value store)

### 4. Authentication
- Uses `auth` from Puter
- If not authenticated, user is redirected to login before viewing the resume page

---

## 🔐 Auth Flow

```text
If not authenticated:
  → redirect to /auth?next=/resume/:id

If authenticated:
  → load resume image, PDF, and AI feedback

## 🔧 Getting Started

Follow the steps below to set up and run the ResumeMind project locally:

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/resumemind.git
cd resumemind
npm install
npm run dev
