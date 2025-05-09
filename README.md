
# Lead Management System

Welcome to the Lead Management System, an advanced web application designed to streamline and optimize the lead management process. This application helps businesses efficiently collect, score, and prioritize leads, allowing for better sales and customer relationship management.

## Features

* Intuitive and easy-to-use interface for lead collection.
* Advanced lead scoring system based on predefined criteria.
* Real-time updates and lead status monitoring.
* Comprehensive dashboard for visualizing lead data.
* Detailed insights and analytics to track lead quality.

## Technologies Used

* Frontend: React.js, Tailwind CSS, Framer Motion
* Backend: Node.js, Express, MongoDB
* API Communication: Axios
* Database Management: Prisma

## Installation and Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/gitYourbits/drCode-LeadManager.git
   ```
2. Navigate to the project directory:

   ```bash
   cd drCode-LeadManager
   ```
3. Install backend dependencies:

   ```bash
   cd backend
   npm install
   cp .env.example .env
   npx prisma generate
   ```
4. Install frontend dependencies:

   ```bash
   cd ../frontend
   npm install
   npm run dev
   ```

## Troubleshooting

* If Prisma client not found, run:

  ```bash
  npx prisma generate
  ```
* For database connection issues:

  * Check if MongoDB is running.
  * Verify your connection string.

## Usage

* Start the backend server:

  ```bash
  npm run start
  ```
* Access the application at `http://localhost:5173`.
* Use the dashboard to view, sort, and manage leads.
* Create new leads through the input form.

Usage
Creating a New Lead
Fill out the lead form with customer information.

Complete optional questions for better lead scoring.

Submit the form to process the lead.

Managing Leads
View all leads in the dashboard.

Sort by priority, date, or other attributes.

Click on a lead to see detailed analysis.

Filter leads based on various criteria.

Analyzing Lead Scores
The system displays:

Overall priority score (1-5).

Breakdown of scoring factors.

Visual representation of each factor's contribution.

Business rules applied to the lead.

## Project Structure

```
lead-management-system/
├── backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   └── server.js
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── services/
│   │   ├── App.jsx
│   │   └── main.jsx
└── README.md
```

## Contact

For any issues or suggestions, feel free to reach out at [yashikabhandari01@gmail.com](mailto:yashikabhandari01@gmail.com) or connect with me on [LinkedIn](https://www.linkedin.com/in/yashika-bhandari-ab7a74253/).

Filter leads based on various criteria.
