# Remote Code Executor

Remote Code Executor is a web-based application that enables users to write, execute, and test code snippets in multiple programming languages directly from their browser. The platform provides an interactive coding environment, supporting languages such as Python, JavaScript, and more.

## Features

- **Multi-language Support**: Write and execute code in various programming languages, including Python and JavaScript.
- **Real-time Output**: View the results of your code execution instantly within the browser.
- **User Authentication**: Secure login and registration system to manage user sessions.
- **Responsive Design**: Accessible and user-friendly interface compatible with desktops, tablets, and mobile devices.

## Technologies Used

- **Frontend**: React.js, HTML5, CSS3
- **Backend**: Node.js, Express.js
- **Code Execution Environment**: Docker
- **Database**: MongoDB

## Prerequisites

Before setting up the project locally, ensure you have the following installed:

- Node.js (v14.x or later)
- Docker
- MongoDB

## Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/Mayurrathod1/Remote_Code_Executor.git
   cd Remote_Code_Executor
   ```

2. **Install Backend Dependencies**:

   ```bash
   cd backend
   npm install
   ```

3. **Install Frontend Dependencies**:

   ```bash
   cd ../frontend
   npm install
   ```

4. **Configure Environment Variables**:

   - Create a `.env` file in the `backend` directory.
   - Add the following variables:

     ```env
     PORT=5000
     MONGO_URI=your_mongodb_connection_string
     JWT_SECRET=your_jwt_secret_key
     ```

5. **Build Docker Images for Code Execution**:

   - Navigate to the `docker-files` directory:

     ```bash
     cd ../docker-files
     ```

   - Build the Docker images:

     ```bash
     docker build -t python-executor -f PythonDockerfile .
     docker build -t javascript-executor -f JavaScriptDockerfile .
     ```

## Usage

1. **Start the Backend Server**:

   - Navigate to the `backend` directory:

     ```bash
     cd backend
     ```

   - Start the server:

     ```bash
     npm start
     ```

2. **Start the Frontend Application**:

   - Navigate to the `frontend` directory:

     ```bash
     cd ../frontend
     ```

   - Start the application:

     ```bash
     npm start
     ```

3. **Access the Application**:

   - Open your browser and navigate to `http://localhost:3000` to start writing and executing code.
