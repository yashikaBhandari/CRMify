Lead Management System
Project Overview
The Lead Management System is an advanced web application designed to collect, score, and prioritize potential customer leads. Built for a property sales hackathon, this system demonstrates how companies can efficiently manage their sales pipeline by focusing on the most promising prospects.

Key Features
Smart Lead Collection: Intuitive form to gather essential information from potential customers.

Advanced Scoring Algorithm: Sophisticated multi-factor scoring system to prioritize leads (score 1-5).

Interactive Dashboard: Real-time lead management interface with filtering and sorting capabilities.

Detailed Lead Analysis: Comprehensive visualization of lead scores with a breakdown of contributing factors.

Business Rules Integration: Special handling for VIP customers, urgent needs, and seasonal factors.

Technologies Used
Frontend
React.js

Tailwind CSS for styling

Framer Motion for animations

React Router for navigation

Axios for API requests

Backend
Node.js

Express

MongoDB for data storage

RESTful API architecture

Getting Started
Prerequisites
Node.js (v14.0.0 or higher)

npm (v6.0.0 or higher)

MongoDB (local or Atlas connection)

Installation
Clone the repository

bash
Copy
Edit
git clone https://github.com/gitYourbits/drCode-LeadManager.git
cd drCode-LeadManager
Install backend dependencies

bash
Copy
Edit
cd backend
npm install
Configure environment variables

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
# If you get any schema errors, you may need to run:
npx prisma db push
Install frontend dependencies

bash
Copy
Edit
cd ../frontend
npm install
Start the application

In the backend directory:

bash
Copy
Edit
npm run dev
In the frontend directory (in a new terminal):

bash
Copy
Edit
npm run dev
Access the application
Frontend: http://localhost:5173

Backend API: http://localhost:3000

Troubleshooting Common Issues
Prisma Client Not Found
If you see errors like "Cannot find module '@prisma/client'" or "You need to run prisma generate":

bash
Copy
Edit
cd backend
npx prisma generate
Database Connection Issues
If you experience database connection problems:

Check that your MongoDB instance is running.

Verify the connection string in the .env file.

Try running:

bash
Copy
Edit
npx prisma db push
Port Already in Use
If you see "Port already in use" errors:

Find the process using the port:

Windows: netstat -ano | findstr :[PORT]

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

Analyzing Lead Scores
The system displays:

Overall priority score (1-5).

Breakdown of scoring factors.

Visual representation of each factor's contribution.

Business rules applied to the lead.

Advanced Scoring System
The Lead Management System employs a sophisticated scoring algorithm that considers multiple factors:

Profit Potential: Based on property type, budget, and expected commission.

Urgency: How soon the customer needs to make a purchase.

Intent: Measured through engagement with optional questions.

Interest Level: Based on specific property interest.

Customer Type: New vs. returning customer.

Key Algorithms Implementation
The system leverages several advanced algorithms to achieve accurate prioritization:

Hierarchical Fuzzy Logic: Implements membership functions to handle uncertainty in input values.

Converts continuous values (like budget) into fuzzy sets.

Applies fuzzy rules to combine criteria.

Uses defuzzification to produce final scores.

Analytic Hierarchy Process (AHP): Determines optimal weights for different scoring factors.

Structured technique for organizing criteria in hierarchical form.

Uses pairwise comparisons of criteria importance.

Calculates the principal eigenvector to derive weights.

Weighted Sum Model (WSM): Combines multiple factors into a single score.

Multiplies normalized scores by their respective weights.

Sums the weighted scores to produce a final value.

Converts the raw score to a 1-5 priority level.

Contextual Adjustment Algorithm: Modifies scores based on market conditions.

Location-based priority adjustments.

Property type-specific weight modifications.

Seasonal factors that influence buying behavior.

Tie-Breaking Mechanism: Ensures consistent ordering when scores are identical.

Hierarchical comparison of individual factors.

Deterministic random component for identical inputs.

Data Flow Through Scoring System
plaintext
Copy
Edit
┌─────────────────┐                        
│   Input Data    │  Budget, urgency, property interest, etc.
└────────┬────────┘                        
         │                                
         ▼                                
┌─────────────────┐  Low Budget: μ=0.0     
│  Fuzzification  │  Medium Budget: μ=0.6  
│                 │  High Budget: μ=0.2     
└────────┬────────┘                        
         │                                
         ▼                                
┌─────────────────┐  Profit: 40%           
│  AHP Weighting  │  Urgency: 25%          
│                 │  Intent: 15%           
└────────┬────────┘  Interest: 10%          
         │         Customer Type: 5%        
         ▼         Sentiment: 5%           
┌─────────────────┐                        
│  Weighted Sum   │  WSM = ∑(Weight_i × Score_i)
│     Model       │  Example: 0.4×4 + 0.25×5 + 0.15×3 + ...
└────────┬────────┘  Raw Score = 3.95     
         │                                
         ▼                                
┌─────────────────┐                        
│   Contextual    │  Location Adjustment: +0.5 for Mumbai
│   Adjustment    │  Season Adjustment: +0.5 (Festival season)
└────────┬────────┘  Adjusted Score = 4.95
         │                                
         ▼                                
┌─────────────────┐                        
│  Tie-Breaking   │  If scores are identical, use hierarchical
│                 │  comparison of individual factors
└────────┬────────┘                        
         │                                
         ▼                                
┌─────────────────┐                        
│  Final Priority │  Final Result: Priority Level 5
│     Score       │  Action: Immediate follow-up within 1 hour
└─────────────────┘
For detailed documentation on the scoring algorithm, see SCORING_DOCUMENTATION.md.

Project Structure
plaintext
Copy
Edit
lead-management-system/
├── backend/              # Node.js Express backend
│   ├── controllers/      # API route controllers
│   ├── models/           # Database models
│   ├── routes/           # API route definitions
│   └── server.js         # Main server file
├── frontend/             # React frontend application
│   ├── public/           # Static assets
│   ├── src/              # Source code
│   │   ├── components/   # React components
│   │   ├── services/     # API services
│   │   ├── App.jsx       # Main application component
│   │   └── main.jsx      # Entry point
│   └── package.json      # Frontend dependencies
└── README.md             # Project documentation







