# 🚀 Lead Management System

## 🌟 Project Overview

The Lead Management System is an advanced web application designed to collect, score, and prioritize potential customer leads. Built for a property sales hackathon, this system demonstrates how companies can efficiently manage their sales pipeline by focusing on the most promising prospects.

## ✨ Key Features

* **Smart Lead Collection**: Intuitive form to gather essential information from potential customers.
* **Advanced Scoring Algorithm**: Sophisticated multi-factor scoring system to prioritize leads (score 1-5).
* **Interactive Dashboard**: Real-time lead management interface with filtering and sorting capabilities.
* **Detailed Lead Analysis**: Comprehensive visualization of lead scores with breakdown of contributing factors.
* **Business Rules Integration**: Special handling for VIP customers, urgent needs, and seasonal factors.

## 🛠️ Technologies Used

### Frontend

* 🌐 React.js
* 🎨 Tailwind CSS for styling
* 🎞️ Framer Motion for animations
* 🔀 React Router for navigation
* 📡 Axios for API requests

### Backend

* 💻 Node.js
* 🚦 Express
* 🗃️ MongoDB for data storage
* 🌐 RESTful API architecture

## 🚧 Getting Started

### Prerequisites

* 🧩 Node.js (v14.0.0 or higher)
* 📦 npm (v6.0.0 or higher)
* 🗄️ MongoDB (local or Atlas connection)

### 💻 Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/gitYourbits/drCode-LeadManager.git
   cd drCode-LeadManager
   ```
2. Install backend dependencies:

   ```bash
   cd backend
   npm install
   ```
3. Configure environment variables:

   ```bash
   cp .env.example .env
   ```
4. Generate Prisma client:

   ```bash
   npx prisma generate
   ```
5. Install frontend dependencies:

   ```bash
   cd ../frontend
   npm install
   ```
6. Start the application:

   ```bash
   npm run dev
   ```

## 📝 Usage

### Creating a New Lead

* 📝 Fill out the lead form with customer information.
* ✅ Complete optional questions for better lead scoring.
* 🚀 Submit the form to process the lead.

### Managing Leads

* 📊 View all leads in the dashboard.
* 🔍 Sort by priority, date, or other attributes.
* 🔄 Filter leads based on various criteria.

### Analyzing Lead Scores

The system displays:

* 🌟 Overall priority score (1-5)
* 🔎 Breakdown of scoring factors
* 📊 Visual representation of each factor's contribution

## ⚙️ Advanced Scoring System

The scoring system utilizes advanced algorithms like:

* 🧠 **Hierarchical Fuzzy Logic**
* 📈 **Analytic Hierarchy Process (AHP)**
* 🗳️ **Weighted Sum Model (WSM)**
* 🛠️ **Contextual Adjustment Algorithm**
* 🔄 **Tie-Breaking Mechanism**

## 🗂️ Folder Structure

```
lead-management-system/
├── backend/              # Node.js Express backend
├── frontend/             # React frontend application
└── README.md             # Project documentation
```

## 🙏 Acknowledgments

This project was developed for the Xeno Internship.
