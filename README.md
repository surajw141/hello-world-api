# Hello World API and Web Interface

This project implements a "Hello World" API and a web interface for interacting with it. The API returns "Hello World" messages in multiple languages based on a query parameter, and the web interface allows users to select a language and display the appropriate greeting message.

## Project Versions

### Hello World API V1
 
   The initial version supported a basic "Hello World" API that returned greeting messages in English, French, and Hindi.

### Hello World API V2 (Enhanced)
  
   This version introduces the following enhancements:

1. Dynamic Language Support:
   
- Added a /languages endpoint to fetch available languages dynamically. 
- Languages are stored in an external languages.json file, simplifying the addition of new languages.

2. Dynamic API Link Handling:
   
- Frontend now fetches API links from a config.json file, making it resilient to backend URL/IP changes.
3. Improved Scalability: 
-   Adding a new language requires only an update to languages.json without modifying the backend or frontend code.



## Project Structure

### Hello World API V1

- **hello_world_api.py**: Flask-based backend API (Version 1).
- **hello-world-app/**: React app for frontend (Version 1).

- **index.html**: Basic HTML hosting for the V1 app.

- **surajw141-hello-world-api-v1.zip**: Archived files for V1.


### Hello World API V2
- **hello_world_api.py**: Flask-based backend API (Enhanced Version).

- **languages.json**: External file containing language data for scalability.

- **hello-world-app/**: React app for frontend (Enhanced Version).

- **V2-surajw141-hello-world-api.zip**: Archived files for V2.


## Prerequisites

### Backend (Flask API)
1. **Python 3.7+**: Ensure Python 3.7 or higher is installed. You can download it from [Python's official website](https://www.python.org/).
2. **Flask**: A Python web framework to run the API server.
3. **Flask-CORS** (optional): If you plan to deploy the frontend and backend separately, this will enable Cross-Origin Resource Sharing (CORS).


### Frontend (React App)
1. **Node.js** (16+ recommended): Install Node.js and npm (comes bundled with Node.js) from [Node.js official website](https://nodejs.org/).
   ```bash
   sudo apt install -y nodejs
   ```


## Setup Instructions

### Step 1: Clone the Repository
   ```bash
   git clone <https://github.com/surajw141/hello-world-api.git>
   cd hello-world-app
   ```


## 2. Set Up the Backend (Flask API)
### Navigate to the V2 backend directory:
```bash
cd "Hello World API V2"
```


### Create a virtual environment and activate it:

```bash
python3 -m venv venv  
source venv/bin/activate  
```

### Install dependencies:
```bash
pip install flask flask-cors python-dotenv requests  

```

### Start the API server
```bash
python3 hello_world_api.py  
```

## 3.  Set up the Frontend (React App)

 ### 1. Install React dependencies: 
 Navigate to your frontend folder and install dependencies.

   ```bash
   cd hello-world-app
   npm install
   npm start
   ```

##   How to Add a New Language

1. **Update languages.json**:
  
   Add the new language and greeting to **languages.json**. For example, to add Marathi:

```json
{
  "Marathi": "Namaskar Jag"
}

```
2. **Frontend Updates**:

   No changes required; the dropdown updates dynamically.

3. **Backend Updates**:
   
   The API automatically supports the new language via the /languages and /message endpoints.


## How to change API Link for Dynamic Handling:
- Replaced hardcoded API links in the React frontend with a **config.json** file located in **public** folder.
  
  ```json
   {
    "api_base_url": "http://192.168.6.5:5000"
   }
  ```

-  This ensures that if the backend IP or URL changes, the frontend automatically adapts without manual code changes.


## Access the App

1. Open the browser and navigate to the React app at http://localhost:3000.
2. Select a language from the dropdown to see the greeting message.


This enhanced version ensures better scalability and ease of maintenance while preserving all functionality from the previous version.

