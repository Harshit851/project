
GUIDED STEPS TO GENERATE GEMINI AI STUDIO AND BIGQUERY API KEY

Created by: Harshit Verma



HOW TO GENERATE A BIGQUERY API KEY

BigQuery is a fully-managed enterprise data warehouse on GCP. To interact with BigQuery programmatically, you need to enable the BigQuery API and generate credentials, typically using an API key or a service account.

Prerequisites:

•	A Google Cloud account

•	A GCP project

•	Billing enabled on your project (required for BigQuery)

•	Access to the Google Cloud Console



Steps to Generate a BigQuery API Key

Step 1: Go to Google Cloud Console

•	Open https://console.cloud.google.com/

•	Sign in with your Google account.
 

Step 2: Search “BigQuery API” in search box

Step 3: Enable the BigQuery API

1.	Go to the BigQuery API page.
   
2.	Click “Enable” if it's not already enabled for your project.
 

Step 4: Create a Service Account (for programmatic access)
1.	Go to Navigation Menu > IAM & Admin > Service Accounts.
2.	Click “Create Service Account”.
3.	Fill in: Name (e.g., bigquery-access) & ID auto-fills
4.	Click Create and Continue.
5.	In the permissions step, search and add:
6.	BigQuery Admin (or BigQuery Data Viewer for read-only)
7.	Click “Done”

Step 5: Create & Download Service Account Key
1.	In the service account list, click on your newly created service account.
2.	Go to the "Keys" tab.
3.	Click "Add Key" > "Create new key".
4.	Choose JSON, then click Create.

 
json key file will be downloaded. Save it securely.
Click back to main key menu in service account you can see your active key
 

Step 6: Test BigQuery API Access (Python Example)
Use Bash command “pip install google-cloud-bigquery”
 
Step 7: Use the python script to test Bigquery api Access
Don’t forget to replace the .json file path 
 




HOW TO GENERATE A GEMINI API KEY
This guide walks you through the process of generating an API key for accessing the Gemini API by Google AI. This is useful for integrating Gemini into applications like chatbots, dashboards, and more.

 
Prerequisites:

•	A Google account

•	Access to Google AI Studio (https://aistudio.google.com/)

•	Internet connection and a modern browser

Step-by-Step Instructions
Step 1: Access Google AI Studio
1.	Open your preferred web browser.
2.	Navigate to https://aistudio.google.com/
3. Sign in using your Google account if prompted.
 

Step 2: Create a New API Key
1. Click 'Get API Key’ on the top left corner under “Google AI Studio”.
2. Click “Create API Key” below the code in the blue box 
3.	A dialog box will appear prompting you to select or create a project:
   
•	Choose an existing project from the list.

• click on "Create a new project", enter a Project Name, and confirm by clicking "Create".


After selecting the project the your API keys will be listed below
 
Points to remember

•	Copy the generated API key.

•	Store it securely using environment variables or a secret manager.

•	Never expose your API key in public code or repositories.

Using the API Key in Your Application
Example (Python):
“import google.generativeai as genai
genai.configure(api_key="YOUR_GEMINI_API_KEY")”

Don’t forget to replace your API key in the code
