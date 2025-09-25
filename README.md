# GenAIArchitect

Accepts a company name as input.
Extracts or generates its stock code.
Uses News search tools in LangChain to fetch news about the company.
Sends the news to an LLM (Google Gemini-2.0-flash) to generate a structured sentiment profile.
Outputs the result as a JSON object.
Uses mlflow for tracing, prompt debugging, and monitoring

## Set up Instructions for Google Gemini key:
Login to https://aistudio.google.com/prompts/new_chat
Click on "Get API key"
A Gemini API key will get generated
load the key in the .env file and access it.

## Set up the ML FLow Tracking URL:
Install MLflow.

`!pip install mlflow`

Start the Tracking Server
Run the MLflow tracking server to establish a central location for your tracking data:

mlflow server 
`--host 127.0.0.1 --port 8080`

Set the Tracking URI
To make your MLflow client connect to the running tracking server, set the tracking URI in your Python code: 

`import mlflow
mlflow.set_tracking_uri("http://20.75.92.162:5000")`
