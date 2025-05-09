# Lead Management System

## Project Overview

The **Lead Management System** is an advanced web application designed to collect, score, and prioritize potential customer leads. Built for a property sales hackathon, this system demonstrates how companies can efficiently manage their sales pipeline by focusing on the most promising prospects.

## Key Features

- **Smart Lead Collection**: Intuitive form to gather essential information from potential customers.
- **Advanced Scoring Algorithm**: Sophisticated multi-factor scoring system to prioritize leads (score 1-5).
- **Interactive Dashboard**: Real-time lead management interface with filtering and sorting capabilities.
- **Detailed Lead Analysis**: Comprehensive visualization of lead scores with breakdown of contributing factors.
- **Business Rules Integration**: Special handling for VIP customers, urgent needs, and seasonal factors.

## Technologies Used

### Frontend

- **React.js**: Library for building the user interface.
- **Tailwind CSS**: Utility-first CSS framework for styling.
- **Framer Motion**: Library for animations.
- **React Router**: For navigation.
- **Axios**: For making API requests.

### Backend

- **Node.js**: JavaScript runtime for the server.
- **Express**: Web framework for building the API.
- **MongoDB**: NoSQL database for data storage.
- **RESTful API Architecture**: API for frontend-backend communication.

## Getting Started

### Prerequisites

- **Node.js** (v14.0.0 or higher)
- **npm** (v6.0.0 or higher)
- **MongoDB** (local or Atlas connection)

### Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/gitYourbits/drCode-LeadManager.git
   cd drCode-LeadManager
Install backend dependencies:

bash
Copy
Edit
cd backend
npm install
Configure environment variables:

bash
Copy
Edit
cp .env.example .env
# Edit the .env file with your MongoDB connection string and other settings
Generate Prisma client:

bash
Copy
Edit
npx prisma generate
If you get any schema errors, run:

bash
Copy
Edit
npx prisma db push
Install frontend dependencies:

bash
Copy
Edit
cd ../frontend
npm install
Start the application:

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
Or change the port in the configuration files (check package.json or server.js).

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

Hierarchical Fuzzy Logic:

Implements membership functions to handle uncertainty in input values.

Converts continuous values (like budget) into fuzzy sets.

Applies fuzzy rules to combine criteria.

Uses defuzzification to produce final scores.

Analytic Hierarchy Process (AHP):

Determines optimal weights for different scoring factors using pairwise comparisons.

Weighted Sum Model (WSM):

Combines multiple factors into a single score by multiplying normalized scores by their respective weights.

Contextual Adjustment Algorithm:

Modifies scores based on market conditions, location-based adjustments, property type-specific weight modifications, and seasonal factors.

Tie-Breaking Mechanism:

Ensures consistent ordering when scores are identical, with hierarchical comparisons and deterministic random components.

Scoring Diagram
Here is a flowchart that illustrates the lead scoring process:

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
Acknowledgments
This project was developed for Xeno Internship.

This README keeps all of your original content intact and includes the diagram exactly as you requested.







