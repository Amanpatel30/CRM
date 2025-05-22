# Installation Instructions

> **Note:** This project is based on [IDURAR Open Source ERP & CRM](https://github.com/idurar/idurar-erp-crm). We acknowledge and appreciate the original work by the IDURAR team.

## Project Structure
This project is organized into two main folders:

1. `/frontend` - Contains the React.js application
2. `/backend` - Contains the Node.js/Express.js API server

## Getting started

#### Step 1: Clone the repository

```bash
git clone <your-repository-url>
cd <your-repository-name>
```

#### Step 2: Create Your MongoDB Account and Database Cluster

- Create your own MongoDB account by visiting the MongoDB website and signing up for a new account.

- Create a new database or cluster by following the instructions provided in the MongoDB documentation. Remember to note down the "Connect to your application URI" for the database, as you will need it later. Also, make sure to change `<password>` with your own password

- add your current IP address to the MongoDB database's IP whitelist to allow connections (this is needed whenever your ip changes)

#### Step 3: Edit the Environment File

- Create a file named `.env` in the `/backend` directory.

  This file will store environment variables for the project to run.

#### Step 4: Update MongoDB URI

In the .env file, add the following line:

```
DATABASE="your-mongodb-uri"
```

Replace "your-mongodb-uri" with the actual URI of your MongoDB database.

#### Step 5: Install Backend Dependencies

In your terminal, navigate to the /backend directory

```bash
cd backend
```

Run the following command to install the backend dependencies:

```bash
npm install
```

This command will install all the required packages specified in the package.json file.

#### Step 6: Run Setup Script

While still in the /backend directory of the project, execute the following command to run the setup script:

```bash
npm run setup
```

This setup script may perform necessary database migrations or any other initialization tasks required for the project.

#### Step 7: Run the Backend Server

In the same terminal, run the following command to start the backend server:

```bash
npm run dev
```

This command will start the backend server, and it will listen for incoming requests.

#### Step 8: Install Frontend Dependencies

Open a new terminal window , and run the following command to install the frontend dependencies:

```bash
cd frontend
```

```bash
npm install
```

#### Step 9: Run the Frontend Server

After installing the frontend dependencies, run the following command in the same terminal to start the frontend server:

```bash
npm run dev
```

This command will start the frontend server, and you'll be able to access the website on localhost:3000 in your web browser.

## Troubleshooting

If you encounter an OpenSSL error while running the frontend server, follow these additional steps:

This is caused by the node.js V17 compatible issues with OpenSSL. Try one of these solutions:

1. Upgrade to Node.js v20.

2. Enable legacy OpenSSL provider:

   - On Unix-like (Linux, macOS, Git bash, etc.)
     ```bash
     export NODE_OPTIONS=--openssl-legacy-provider
     ```

   - On Windows command prompt:
     ```bash
     set NODE_OPTIONS=--openssl-legacy-provider
     ```

   - On PowerShell:
     ```bash
     $env:NODE_OPTIONS = "--openssl-legacy-provider"
     ```

After trying the above solutions, run:
```bash
npm run dev
```

> If you still facing issue, then follow [this stackoverflow thread](https://stackoverflow.com/questions/69692842/error-message-error0308010cdigital-envelope-routinesunsupported). It has so many different types of opinions. You definitely have solution after going through the thread.