<h1 align="center">Lead Management System</h1>
<h2 align="center">An Advanced Web Application for Efficient Lead Management</h2>
<img align="center" alt="Lead Management" width="400" src="https://www.example.com/your-image-link.gif" />

<h3 align="center">This web application allows businesses to collect, score, and prioritize leads to streamline their sales process and focus on the most promising prospects.</h3>

- 🔭 I’m currently working on **Lead Management Systems and Advanced Scoring Algorithms**
- 🌱 I’m currently learning **React.js, Node.js, MongoDB, and Advanced Algorithms**
- 💬 Ask me about **Lead Scoring, Business Rules Integration, and Web Development**
- 📫 How to reach me **yashikabhandari01@gmail.com**

<h3 align="left">Connect with me:</h3>
<p align="left">
  <a href="https://www.linkedin.com/in/yashika-bhandari-ab7a74253/" target="blank">
    <img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="Yashika Bhandari" height="30" width="40" />
  </a>
  <a href="https://www.leetcode.com/yashika-bhandari" target="blank">
    <img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/leet-code.svg" alt="Yashika Bhandari" height="30" width="40" />
  </a>
  <a href="https://github.com/yashikaBhandari" target="blank">
    <img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/github.svg" alt="Yashika Bhandari" height="30" width="40" />
  </a>
</p>

<h3 align="left">Technologies Used:</h3>
<p align="left">
  <a href="https://reactjs.org/" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original-wordmark.svg" alt="react" width="40" height="40"/>
  </a>
  <a href="https://nodejs.org/" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" alt="nodejs" width="40" height="40"/>
  </a>
  <a href="https://expressjs.com" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/express/express-original-wordmark.svg" alt="express" width="40" height="40"/>
  </a>
  <a href="https://www.mongodb.com/" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mongodb/mongodb-original-wordmark.svg" alt="mongodb" width="40" height="40"/>
  </a>
  <a href="https://tailwindcss.com/" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/tailwindcss/tailwindcss-plain-wordmark.svg" alt="tailwindcss" width="40" height="40"/>
  </a>
  <a href="https://axios-http.com/" target="_blank" rel="noreferrer">
    <img src="https://axios-http.com/favicon.ico" alt="axios" width="40" height="40"/>
  </a>
</p>

<h3 align="left">Project Overview:</h3>
<p align="left">
  The **Lead Management System** is a web application designed for property sales. It allows companies to efficiently collect, score, and prioritize potential leads using a sophisticated algorithm.
</p>

<h3 align="left">Key Features:</h3>
<ul>
  <li>Intuitive Lead Collection Form</li>
  <li>Advanced Lead Scoring Algorithm (Score 1-5)</li>
  <li>Interactive Dashboard for Lead Management</li>
  <li>Detailed Lead Analysis with Visual Representation</li>
  <li>Business Rules Integration for VIP, Urgency, and Seasonality</li>
</ul>

<h3 align="left">Technologies Used:</h3>
<h4>Frontend:</h4>
<ul>
  <li>React.js</li>
  <li>Tailwind CSS</li>
  <li>Framer Motion</li>
  <li>React Router</li>
  <li>Axios</li>
</ul>

<h4>Backend:</h4>
<ul>
  <li>Node.js</li>
  <li>Express</li>
  <li>MongoDB</li>
  <li>RESTful API Architecture</li>
</ul>

<h3 align="left">Getting Started:</h3>
<p align="left">
  <b>Prerequisites:</b>
  <ul>
    <li>Node.js (v14.0.0 or higher)</li>
    <li>npm (v6.0.0 or higher)</li>
    <li>MongoDB (local or Atlas connection)</li>
  </ul>
</p>

### Installation

1. **Clone the repository**  
   ```bash
   git clone https://github.com/gitYourbits/drCode-LeadManager.git
Navigate to the project directory

bash
Copy
Edit
cd drCode-LeadManager
Install backend dependencies

bash
Copy
Edit
cd backend
npm install
Configure environment variables
Copy the example environment file and configure your MongoDB connection string.

bash
Copy
Edit
cp .env.example .env
# Edit the .env file with your MongoDB connection string and other settings
Generate Prisma client

bash
Copy
Edit
npx prisma generate
# This creates the Prisma client code required by the application
Install frontend dependencies

bash
Copy
Edit
cd ../frontend
npm install
Start the application
Run the backend server in one terminal:

bash
Copy
Edit
# In the backend directory
npm run dev
Run the frontend server in another terminal:

bash
Copy
Edit
# In the frontend directory
npm run dev
Access the Application
Frontend: http://localhost:5173

Backend API: http://localhost:3000

Troubleshooting Common Issues
Prisma Client Not Found
If you encounter errors like "Cannot find module '@prisma/client'" or "You need to run prisma generate":

bash
Copy
Edit
cd backend
npx prisma generate
Database Connection Issues
If you experience database connection problems:

Check that your MongoDB instance is running.

Verify the connection string in the .env file.

Run:

bash
Copy
Edit
npx prisma db push
Port Already in Use
If you see "Port already in use" errors:

Find the process using the port:

Windows:

bash
Copy
Edit
netstat -ano | findstr :[PORT]
Kill the process:

bash
Copy
Edit
taskkill /PID [PID] /F
Or change the port in the configuration (check package.json or server.js files).

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
