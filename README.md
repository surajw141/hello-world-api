# Hello World API and Web Interface

This project implements a simple "Hello World" API and a web interface for interacting with it. The API returns "Hello World" messages in English, French, and Hindi, based on a query parameter, and the web interface allows users to select a language and display the appropriate greeting message.

## Project Structure

- **hello_world_api.py**: Flask-based backend API that provides the greeting message.
- **HelloWorld.js**: React component to call the API and display the greeting message.
- **App.js**: Main entry point for the React app, which renders the HelloWorld component.
- **index.html**: Basic HTML file to host the React app.
- **README.md**: Documentation for setup, dependencies, and usage.

## Prerequisites

### Backend (Flask API)
1. **Python 3.7+**: Ensure Python 3.7 or higher is installed. You can download it from [Python's official website](https://www.python.org/).
2. **Flask**: A Python web framework to run the API server.
3. **Flask-CORS** (optional): If you plan to deploy the frontend and backend separately, this will enable Cross-Origin Resource Sharing (CORS).


### Frontend (React App)
1. **Node.js** (16+ recommended): Install Node.js and npm (comes bundled with Node.js) from [Node.js official website](https://nodejs.org/).
   ```bash
   sudo apt install -y nodejs


## Setup Instructions

### Step 1: Clone the Repository
   ```bash
   git clone <https://github.com/surajw141/hello-world-api.git>
   cd hello-world-app
   ```


## 2. Set Up the Backend (Flask API)

### Create a Virtual Environment and get flask
```bash
python3 -m venv venv
source venv/bin/activate
pip3 install flask flask-cors python-dotenv
pip3 install requests
```


### Frontend (React App)
1. **Node.js** (16+ recommended): Install Node.js and npm (comes bundled with Node.js) from [Node.js official website](https://nodejs.org/).

   ```bash
   sudo apt install -y nodejs

2. Verify Node.js Installation: Check that Node.js and npm were installed successfully.
   ```bash
   node -v
   npm -v
   
3. Install React dependencies: Navigate to your frontend folder and install dependencies.
   ```bash
   cd frontend
   npm install
