# 🧠 Chainlit Application Setup Guide

This README provides step-by-step instructions to set up, configure, and run a Python application that uses [Chainlit](https://docs.chainlit.io/) with Azure OpenAI integration and optional email notification support via Logic Apps.

---

## 📌 Prerequisites

- Python 3.8 or later installed on your machine.
- Internet connection for installing packages and calling external APIs.
- Optional: Azure subscription with access to Azure OpenAI and Logic Apps.

---

## 📁 Step 1: Create a Python Virtual Environment

A **virtual environment** is a best practice in Python that allows you to manage dependencies separately from your system Python.

### ✅ Create the environment

Open your terminal or command prompt and run:

```bash
python -m venv venv
```

### ✅ Active the environment
On Windows:

```bash
venv\Scripts\activate
```

On macOS/Linux:
```bash
source venv/bin/activate
```

Once activated, your terminal prompt should change to show (venv) — indicating the virtual environment is active.

## 📦 Step 2: Install Required Dependencies
Install the dependencies listed in the requirements.txt file using pip:

```bash
pip install -r requirements.txt
```
# Notes
📄 requirements.txt includes all the necessary libraries (e.g., Chainlit, Azure SDKs) your app needs to run.


## 🔐 Step 3: Create and Configure a .env File
The .env file contains environment variables used by your app for authentication and configuration. Create a file named .env in the project root folder and paste the following content:

```.env
AZURE_OPENAI_ENDPOINT=wss://<your-endpoint>.openai.azure.com
AZURE_OPENAI_DEPLOYMENT=gpt-4o-realtime-preview
AZURE_OPENAI_API_KEY= # Leave empty if using Entra ID Authentication (RECOMMENDED)
LOGIC_APPS_URL= # Logic Apps URL to send emails (optional)
```
# 🔍 Explanation of Environment Variables:
- AZURE_OPENAI_ENDPOINT:
Your Azure OpenAI WebSocket endpoint. Replace <your-endpoint> with your actual Azure region endpoint.
Example:
```plaintext
AZURE_OPENAI_ENDPOINT=wss://eastus2.openai.azure.com
```
- AZURE_OPENAI_DEPLOYMENT:
The deployment name of your Azure OpenAI model, such as gpt-4o-realtime-preview.

- AZURE_OPENAI_API_KEY (Optional):
API Key for Azure OpenAI. Leave this field blank if you're using Microsoft Entra ID authentication, which is more secure and recommended.

- LOGIC_APPS_URL (Optional):
This is the URL of your Logic Apps workflow that handles sending emails. If left empty, email functionality will be disabled.

## 🚀 Step 4: Run the Chainlit App
Use the following command to start the application with Chainlit:

```bash
chainlit run app.py
```
This will:
- Load the Python script app.py
- Read the environment variables from .env
- Launch a local web UI where you can interact with your app

## 🧪 Example Use Case
Your app.py likely connects to Azure OpenAI’s real-time GPT-4o service, processes user input, and optionally sends email alerts or summaries via Logic Apps if LOGIC_APPS_URL is provided.

## 🧯 Troubleshooting
- Command not found?
Ensure Python and pip are added to your system PATH.

- chainlit: command not found?
Ensure Chainlit is installed (it should be in requirements.txt). Otherwise, manually install with:

```bash
pip install chainlit
```
- Environment variables not working?
Make sure .env is in the same folder where you run chainlit, and that python-dotenv is installed.

# 📝 Notes
- This guide assumes the main application file is named app.py.
- Keep your .env file private — never commit it to version control.
- For production deployment, additional security and hosting steps are needed.

## 📚 Resources
- [Chainlit Docs](https://docs.chainlit.io/)
- [Azure OpenAI Docs](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/)
- [Microsoft Entra ID](https://learn.microsoft.com/en-us/entra/)
- [Logic Apps](https://learn.microsoft.com/en-us/azure/logic-apps)