# ERP & CRM System

An open-source ERP (Enterprise Resource Planning) and CRM (Customer Relationship Management) system built with the MERN stack:

- MongoDB - Document database
- Express.js - Node.js web framework
- React.js - Client-side JavaScript framework
- Node.js - JavaScript web server

## Credits

This project is based on [IDURAR Open Source ERP & CRM](https://github.com/idurar/idurar-erp-crm) created by IDURAR team. We acknowledge and appreciate their work in developing the original application.

## Project Structure

This project is organized into two main folders:

### Frontend
- Contains the React.js application with Ant Design
- Includes documentation and feature descriptions
- Located in the `/frontend` directory

### Backend
- Contains the Node.js/Express.js API server
- Handles database operations with MongoDB
- Located in the `/backend` directory

## Features

- Invoice Management
- Payment Management
- Quote Management
- Customer Management
- Modern UI with Ant Design Framework
- Responsive design for mobile and desktop

## Getting started

1. Clone this repository
2. Set up MongoDB:
   - Create a MongoDB database
   - Add your IP address to the MongoDB whitelist

3. Configure environment variables:
   - Create a `.env` file in the `/backend` directory
   - Add `DATABASE="your-mongodb-uri"`

4. Install backend dependencies:
   ```bash
   cd backend
   npm install
   ```

5. Run the setup script:
   ```bash
   npm run setup
   ```

6. Start the backend server:
   ```bash
   npm run dev
   ```

7. In a new terminal, install frontend dependencies:
   ```bash
   cd frontend
   npm install
   ```

8. Start the frontend server:
   ```bash
   npm run dev
   ```

9. Access the application at `http://localhost:3000`

## License

This project is released under the MIT License.
