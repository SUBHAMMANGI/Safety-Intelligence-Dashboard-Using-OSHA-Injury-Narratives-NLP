📊 Safety Intelligence Dashboard Using OSHA Injury Narratives & NLP
This repository contains a Safety Intelligence Dashboard for SEG, built using Power BI and Python. The project uses NLP analysis on OSHA injury narratives and machine-related safety data to predict and visualize safety risks.

📌 Features
NLP analysis on OSHA injury narratives to identify common injury patterns

Data preprocessing and feature engineering using Python

Interactive Power BI dashboard to visualize injury data and trends

Model for predicting hand injuries related to machinery based on historical data

Data visualization for injury types, frequency, and trends

🛠️ Installation
To run this project, you will need Python Power BI installed.

1️⃣ Clone the repository
sh
Copy
git clone https://github.com/yourusername/safety-intelligence-dashboard.git
cd safety-intelligence-dashboard
2️⃣ Install dependencies
Install the Python libraries required for the project:

sh
Copy
pip install -r requirements.txt
3️⃣ Power BI Setup
Open the Safety_Intelligence_Dashboard.pbix file in Power BI.

Import the hand_injuries_with_machines.csv dataset to load the safety data into the dashboard.

📂 Dataset
The dataset used in the project contains injury data related to hand injuries and machinery. You can find the dataset used in this project here:

hand_injuries_with_machines.csv: Contains information on injuries and machinery association.

🚀 Usage
Run the Python script to preprocess data and perform NLP analysis:

sh
Copy
python Safety.ipynb
Power BI Dashboard
Open the Safety_Intelligence_Dashboard.pbix file in Power BI.

Load the dataset into Power BI.

Interact with the dashboard to view insights on hand injuries and related machinery.

📊 Model Architecture
The model consists of:

Data preprocessing (handling missing data, feature scaling)

NLP for text analysis (extracting meaningful insights from injury narratives)

Power BI dashboard for visualizations (showing injury types, trends, and predictive insights)

📉 Results
The dashboard provides interactive visualizations of:

Injury statistics by machine type

Trends in hand injuries over time

Predicted injury likelihood based on historical data

📜 License project is licensed under the MIT License.
🤝 Contributing
Feel free to submit a pull request or open an issue to suggest improvements.

📬 Contact
For any queries, reach out to:

Email: subhammangi27@gmail.com

GitHub: SUBHAMMANGI
