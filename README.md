<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lead Management System</title>
</head>
<body>
    <h1>Lead Management System</h1>

    <h2>Project Overview</h2>
    <p>The Lead Management System is an advanced web application designed to collect, score, and prioritize potential customer leads. Built for a property sales hackathon, this system demonstrates how companies can efficiently manage their sales pipeline by focusing on the most promising prospects.</p>

    <hr>

    <h2>Key Features</h2>
    <ul>
        <li><strong>Smart Lead Collection:</strong> Intuitive form to gather essential information from potential customers.</li>
        <li><strong>Advanced Scoring Algorithm:</strong> Sophisticated multi-factor scoring system to prioritize leads (score 1-5).</li>
        <li><strong>Interactive Dashboard:</strong> Real-time lead management interface with filtering and sorting capabilities.</li>
        <li><strong>Detailed Lead Analysis:</strong> Comprehensive visualization of lead scores with breakdown of contributing factors.</li>
        <li><strong>Business Rules Integration:</strong> Special handling for VIP customers, urgent needs, and seasonal factors.</li>
    </ul>

    <hr>

    <h2>Technologies Used</h2>
    <h3>Frontend</h3>
    <ul>
        <li>React.js</li>
        <li>Tailwind CSS for styling</li>
        <li>Framer Motion for animations</li>
        <li>React Router for navigation</li>
        <li>Axios for API requests</li>
    </ul>

    <h3>Backend</h3>
    <ul>
        <li>Node.js</li>
        <li>Express</li>
        <li>MongoDB for data storage</li>
        <li>RESTful API architecture</li>
    </ul>

    <hr>

    <h2>Getting Started</h2>

    <h3>Prerequisites</h3>
    <ul>
        <li>Node.js (v14.0.0 or higher)</li>
        <li>npm (v6.0.0 or higher)</li>
        <li>MongoDB (local or Atlas connection)</li>
    </ul>

    <h3>Installation</h3>
    <p>Follow these steps to get the application running locally:</p>
    <ol>
        <li>Clone the repository:
            <pre><code>git clone https://github.com/gitYourbits/drCode-LeadManager.git
cd drCode-LeadManager</code></pre>
        </li>
        <li>Install backend dependencies:
            <pre><code>cd backend
npm install</code></pre>
        </li>
        <li>Configure environment variables:
            <pre><code>cp .env.example .env
# Edit the .env file with your MongoDB connection string and other settings</code></pre>
        </li>
        <li>Generate Prisma client:
            <pre><code>npx prisma generate
# This creates the Prisma client code required by the application
# If you get any schema errors, you may need to run:
npx prisma db push</code></pre>
        </li>
        <li>Install frontend dependencies:
            <pre><code>cd ../frontend
npm install</code></pre>
        </li>
        <li>Start the application:
            <ul>
                <li>In the backend directory:
                    <pre><code>npm run dev</code></pre>
                </li>
                <li>In the frontend directory (in a new terminal):
                    <pre><code>npm run dev</code></pre>
                </li>
            </ul>
        </li>
    </ol>

    <h3>Access the Application</h3>
    <ul>
        <li>Frontend: <a href="http://localhost:5173" target="_blank">http://localhost:5173</a></li>
        <li>Backend API: <a href="http://localhost:3000" target="_blank">http://localhost:3000</a></li>
    </ul>

    <hr>

    <h2>Troubleshooting Common Issues</h2>

    <h3>Prisma Client Not Found</h3>
    <p>If you see errors like "Cannot find module '@prisma/client'" or "You need to run prisma generate":</p>
    <pre><code>cd backend
npx prisma generate</code></pre>

    <h3>Database Connection Issues</h3>
    <p>If you experience database connection problems:
        <ul>
            <li>Check that your MongoDB instance is running.</li>
            <li>Verify the connection string in the .env file.</li>
            <li>Try running:
                <pre><code>npx prisma db push</code></pre>
            </li>
        </ul>
    </p>

    <h3>Port Already in Use</h3>
    <p>If you see "Port already in use" errors:</p>
    <pre><code>netstat -ano | findstr :[PORT]
taskkill /PID [PID] /F</code></pre>
    <p>Or change the port in the configuration (check package.json or server.js files).</p>

    <hr>

    <h2>Usage</h2>

    <h3>Creating a New Lead</h3>
    <ul>
        <li>Fill out the lead form with customer information.</li>
        <li>Complete optional questions for better lead scoring.</li>
        <li>Submit the form to process the lead.</li>
    </ul>

    <h3>Managing Leads</h3>
    <ul>
        <li>View all leads in the dashboard.</li>
        <li>Sort by priority, date, or other attributes.</li>
        <li>Click on a lead to see detailed analysis.</li>
        <li>Filter leads based on various criteria.</li>
    </ul>

    <h3>Analyzing Lead Scores</h3>
    <p>The system displays:
        <ul>
            <li>Overall priority score (1-5)</li>
            <li>Breakdown of scoring factors</li>
            <li>Visual representation of each factor's contribution</li>
            <li>Business rules applied to the lead</li>
        </ul>
    </p>

    <hr>

    <h2>Advanced Scoring System</h2>

    <p>The Lead Management System employs a sophisticated scoring algorithm that considers multiple factors:</p>
    <ul>
        <li><strong>Profit Potential:</strong> Based on property type, budget, and expected commission.</li>
        <li><strong>Urgency:</strong> How soon the customer needs to make a purchase.</li>
        <li><strong>Intent:</strong> Measured through engagement with optional questions.</li>
        <li><strong>Interest Level:</strong> Based on specific property interest.</li>
        <li><strong>Customer Type:</strong> New vs. returning customer.</li>
    </ul>

    <hr>

    <h2>Key Algorithms Implementation</h2>

    <p>The system leverages several advanced algorithms to achieve accurate prioritization:</p>

    <ul>
        <li><strong>Hierarchical Fuzzy Logic:</strong> Implements membership functions to handle uncertainty in input values.</li>
        <li><strong>Analytic Hierarchy Process (AHP):</strong> Determines optimal weights for different scoring factors.</li>
        <li><strong>Weighted Sum Model (WSM):</strong> Combines multiple factors into a single score.</li>
        <li><strong>Contextual Adjustment Algorithm:</strong> Modifies scores based on market conditions.</li>
        <li><strong>Tie-Breaking Mechanism:</strong> Ensures consistent ordering when scores are identical.</li>
    </ul>

    <hr>

    <h2>Data Flow Through Scoring System</h2>
    <pre><code>
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
</code></pre>

    <hr>

    <h2>Project Structure</h2>
    <pre><code>
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
</code></pre>

    <hr>

    <h2>License</h2>
    <p>This project is licensed under the MIT License.</p>
</body>
</html>


Acknowledgments

This project was developed for the Xeno Internship.







