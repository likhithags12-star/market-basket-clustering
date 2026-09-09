# market-basket-clustering
Market Basket Analysis and Customer Segmentation web application using K-Means clustering, React, Vite, Tailwind CSS, and data visualization.
Market Basket Analysis with Customer Clustering

A frontend-based Machine Learning web application that analyzes customer transaction data and automatically groups customers into meaningful segments using the K-Means Clustering algorithm.

The application transforms raw transaction data into customer purchasing features, performs clustering, visualizes customer segments, analyzes purchasing behavior, and generates downloadable reports.

Features
Interactive analytics dashboard
K-Means customer segmentation
Automatic customer grouping
Cluster performance analysis
Purchase and category analysis
Adjustable number of clusters from 2 to 6
Data visualization using charts
Customer feature engineering
Clustering metrics including Inertia and Silhouette Score
Business-friendly customer segment names
Downloadable PDF segmentation reports
Fully frontend-based application
No backend or external API required
How It Works

The application follows this Machine Learning pipeline:

Load Transaction Data
Process Customer Transactions
Create Customer Features
Normalize the Features
Apply K-Means Clustering
Generate Customer Segments
Calculate Cluster Performance Metrics
Visualize Results
Generate PDF Reports
Customer Features Used

The system analyzes customer behavior using features such as:

Purchase Frequency
Total Spending
Average Basket Value
Total Quantity Purchased
Number of Unique Products
Number of Unique Categories
Recency of Purchase
Category Spending Preferences

These features are used to identify customers with similar purchasing behavior.

Customer Segments

Based on customer behavior, the application can generate business-friendly segments such as:

High Value Shoppers
Frequent Buyers
Premium Buyers
Budget Shoppers
Low Engagement Shoppers
Occasional Shoppers

Segment names are automatically generated based on spending, purchase frequency, basket value, and customer engagement.

Machine Learning Algorithm

This project uses a custom implementation of K-Means Clustering.

The implementation includes:

K-Means++ Initialization
Lloyd's Algorithm
Feature Normalization
Centroid Calculation
Customer Assignment
Inertia Calculation
Silhouette Score Calculation

The default number of clusters is K = 4, and users can change the number of clusters from 2 to 6.

Dataset

The application uses transaction-level data stored in:

public/data/transactions.csv

The dataset contains information such as:

Transaction ID
Customer ID
Transaction Date
Product ID
Product Name
Category
Quantity
Unit Price
Total Amount

The application automatically converts transaction-level data into customer-level features before performing clustering.

Technologies Used
Frontend
React
Vite
Tailwind CSS
Machine Learning
Custom K-Means Clustering Implementation
Feature Engineering
Data Normalization
Silhouette Score
Inertia Calculation
Data Processing
PapaParse
Data Visualization
Recharts
Report Generation
jsPDF
html2canvas
Project Structure
market-basket-clustering/
│
├── public/
│   └── data/
│       └── transactions.csv
│
├── src/
│   ├── components/
│   │   ├── ChartCard.jsx
│   │   ├── ClusterVisualization.jsx
│   │   ├── CustomerDetails.jsx
│   │   ├── CustomerTable.jsx
│   │   ├── Header.jsx
│   │   ├── ReportButton.jsx
│   │   ├── SegmentCard.jsx
│   │   ├── Sidebar.jsx
│   │   └── StatCard.jsx
│   │
│   ├── pages/
│   │   ├── Dashboard.jsx
│   │   ├── CustomerSegments.jsx
│   │   ├── PurchaseAnalysis.jsx
│   │   └── ClusterPerformance.jsx
│   │
│   ├── ml/
│   │   ├── clustering.js
│   │   ├── kmeans.js
│   │   └── preprocessing.js
│   │
│   ├── services/
│   │   └── dataset.js
│   │
│   └── utils/
│       ├── customerFeatures.js
│       ├── segmentInsights.js
│       ├── reportGenerator.js
│       ├── currency.js
│       └── colors.js
│
├── package.json
├── vite.config.js
└── README.md
Installation and Setup

Clone the repository:

git clone <your-repository-url>

Navigate to the project folder:

cd market-basket-clustering

Install dependencies:

npm install

Start the development server:

npm run dev

Open the local URL shown in the terminal.

Application Pages
Dashboard

Provides an overview of:

Customer statistics
Transaction statistics
Spending behavior
Customer segments
Important business insights
Customer Segments

Displays:

K-Means customer clusters
Segment details
Customer information
Cluster visualization
Adjustable number of clusters
Purchase Analysis

Analyzes:

Customer purchases
Product preferences
Category preferences
Spending patterns
Cluster Performance

Evaluates clustering quality using:

Inertia
Silhouette Score
Cluster sizes
Segment statistics
PDF Report

The application can generate a downloadable PDF report containing:

Transaction summary
Customer summary
Current number of clusters
Segment statistics
Customer insights
Top product categories
Inertia score
Silhouette score
Purchase analysis
Customer segmentation visualization
Using Your Own Dataset

You can replace the existing dataset located at:

public/data/transactions.csv

Make sure your CSV file contains the following columns:

transaction_id
customer_id
transaction_date
product_id
product_name
category
quantity
unit_price
total_amount

The application automatically processes the data and calculates recency based on the latest transaction date available in the dataset.

Project Objective

The main objective of this project is to help businesses understand customer purchasing behavior by grouping customers with similar characteristics.

The generated customer segments can help businesses with:

Personalized marketing
Customer retention
Targeted promotions
Product recommendations
Customer behavior analysis
Business decision-making
Future Improvements

Possible future enhancements include:

Upload custom datasets directly from the interface
Additional clustering algorithms
Real-time data processing
Customer purchase prediction
Product recommendation system
Backend database integration
User authentication
Advanced Machine Learning models
