# devops-cd

This project is a simple Express.js application deployed on an EC2 instance using GitHub Actions for Continuous Deployment. The application includes a basic view and static files for a more interactive web interface.

## Features

- **Express.js Application**: Includes routes and a view rendering system using EJS templates.
- **Static File Serving**: Serves images, CSS, and other assets from the /public directory.
- **CD Pipeline**: Configured with GitHub Actions to automatically deploy updates to an EC2 instance.

## File Structure

├── app.js          
├── views/
│   └── index.ejs     
├── public/
│   ├── css/
│   │   └── styles.css
│   ├── images/
│   │   └── chill.webp
└── package.json


## Routes

- **Home (/)**: Renders a basic HTML view using EJS with a welcoming message and static image.

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/Rodd-droid/devops-cd.git
cd devops-cd
```

### 2. Install Dependencies

Install the required dependencies:

```bash
npm install
```

### 3. Run Locally

Start the application locally:

```bash
npm start
```

This will expose the app at http://localhost:3000.

### 4. Continuous Deployment with GitHub Actions

- **Triggers**: Deployment is triggered on every push to the main branch.
- **Deployment Steps**: Deployment is triggered on every push to the main branch.
  - Checkout code from GitHub.
  - Connect to the EC2 instance via SSH.
  - Pull the latest changes, install dependencies, and restart the server using PM2.

### Dependencies

The application requires the following dependencies, listed in the package.json file:

- express: Web framework for building Node.js web applications.

### Usage Example

```bash
# Test the home route
curl http://localhost:3000/
```

### Author
Project developed by Rodrigo Quilumba.