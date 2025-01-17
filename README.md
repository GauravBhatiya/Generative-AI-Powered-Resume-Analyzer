# Generative AI-Powered Resume Analyzer


This project extracts key information from resumes stored in a Google Drive folder.
The information is processed using Google’s Generative AI model and saved in an Excel file for easy analysis and reporting.

## Technologies Used

- **Python**: The primary language for implementing the script.
- **Google Drive API**: For accessing and downloading resumes from Google Drive.
- **Generative AI Model (Google gemini-1.5-flash)**: To process and extract structured data from resumes.
- **Pandas**: For data manipulation and saving to an Excel file.
- **OpenPyXL**: For writing data into `.xlsx` files.

## Requirements

### Software Requirements

1. **Python 3.8+**
2. **Google Cloud Service Account**
   - A Google Cloud project with access to the **Google Drive API**.
   - Follow [this guide](https://cloud.google.com/docs/authentication/getting-started) to set up a service account and download the `.json` credentials file and put into working       
     directory.
3. **Google Gemini API**
   - Follow [this guide](https://ai.google.dev/gemini-api/docs/models/gemini#gemini-1.5-flash) to set up API

   
# **Set Up Google Cloud Service Account**

  Before you can use the Google Drive API and Generative AI model, you need to set up a Google Cloud Service Account with the appropriate permissions.
  
  ### Follow these steps:
  
  1. **Go to Google Cloud Console:**
     - Visit [Google Cloud Console](https://console.cloud.google.com/).
  
  2. **Create a new project**:
     - Click on **"Select a project"** at the top and then click **"New Project"**.
     - Give your project a name and click **Create**.
  
  3. **Enable Google Drive API for the project**:
     - In the Cloud Console, navigate to the **API & Services > Library** section.
     - Search for **"Google Drive API"**.
     - Click on the **Google Drive API** result and enable it for your project.
     - Same for ** Generative Language API **
  
  4. **Create a Service Account**:
     - In the Cloud Console, go to **IAM & Admin > Service Accounts**.
     - Click on **"Create Service Account"**.
     - Provide a name for your Service Account (e.g., `ResumeExtractorServiceAccount`).
     - Set the **Role** to **"Project > Owner"** to ensure it has the necessary permissions for Google Drive access.
  
  5. **Generate and Download Credentials**:
     - After creating the Service Account, click on it and go to the **Keys** tab.
     - Click on **Add Key > Create new key**.
     - Choose **JSON** as the key type and download the generated `.json` file.
  
  6. **Save the `.json` file**:
     - Save the downloaded `.json` credentials file in your project directory (e.g., `credentials/service_account.json`).
  
  ### Permissions
  
  - **Google Drive API** permissions: Your Service Account must have **read access** to the Google Drive folder where the resumes are stored.
  - **Share the folder**: Ensure that the **Service Account email** (found in the `.json` credentials file) has access to the relevant Google Drive folder.
  
  Once you have completed these steps, you will have a **Service Account** with the necessary credentials to access Google Drive and use the API to download and process resumes.
   

# Python Libraries

Install the required libraries using the following command:
  - google-auth
  - google-auth-httplib2
  - google-auth-oauthlib
  - google-api-python-client
  - openpyxl
  - pandas
  - google-generativeai
