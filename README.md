# Digital Concession

A digital bus concession management system designed to simplify student concession applications, administrative approval, and digital pass verification.

The project consists of a mobile application for students, an administrative web dashboard, and backend services for application processing and database operations.

## Features

### Student Mobile Application

* Submit bus concession applications.
* Enter personal, educational, and travel information.
* Upload supporting documents.
* Track application submission and success status.
* Access digital concession-related screens.
* Generate or display QR-based pass information through the relevant application screens.

### Administrative Dashboard

* View and review concession applications.
* Inspect submitted application information.
* Approve or reject applications through the review interface.
* Manage the application review workflow.

### Backend and Database

* Express.js backend services.
* MongoDB database integration.
* API endpoints for application operations.
* Centralized application data management.

## Technology Stack

| Component          | Technologies                   |
| ------------------ | ------------------------------ |
| Mobile application | Expo, React Native, TypeScript |
| Navigation         | Expo Router                    |
| Admin dashboard    | React, Vite, JavaScript        |
| Backend            | Node.js, Express.js            |
| Database           | MongoDB                        |
| API communication  | HTTP and Axios                 |
| QR functionality   | React Native QR code libraries |

## Repository Structure

```text
Digital_Concession/
├── Mobile-App/
│   ├── src/
│   ├── assets/
│   ├── public/
│   ├── server/
│   ├── scripts/
│   ├── package.json
│   └── README.md
├── Web-App/
│   ├── src/
│   ├── public/
│   ├── server.js
│   ├── package.json
│   └── README.md
├── .gitignore
├── LICENSE
└── README.md
```

This is a simplified view of the repository. Some configuration, asset, and implementation files are omitted.

## Prerequisites

Install the following before running the project:

* Node.js and npm
* MongoDB, either a local server or a hosted MongoDB deployment
* An Expo-compatible development environment
* Expo Go or an appropriate Android/iOS development environment for mobile testing

## Getting Started

Clone the repository:

```bash
git clone https://github.com/techistt/Digital_Concession.git
cd Digital_Concession
```

### 1. Start the Mobile Application Backend

Open a terminal:

```bash
cd Mobile-App/server
npm install
```

Configure the backend environment variables using the names expected by the server implementation. Add your MongoDB connection string and any other required configuration to a local environment file.

Start the backend using the script defined in its `package.json`. If the package defines a `start` script, run:

```bash
npm start
```

Otherwise, if the server entry point is `server.js`, run:

```bash
node server.js
```

### 2. Start the Mobile Application

Open another terminal:

```bash
cd Mobile-App
npm install
npx expo start
```

Follow the Expo CLI instructions to launch the application on a supported device, emulator, or web browser.

For a physical device, configure the API base URL to use your computer's reachable LAN IP address rather than `localhost`.

### 3. Start the Administrative Dashboard

Open another terminal:

```bash
cd Web-App
npm install
```

Configure the environment variables required by the dashboard and its backend.

Start the frontend development server:

```bash
npm run dev
```

If the administrative backend is required, start it in a separate terminal:

```bash
npm start
```

The frontend and backend may use different ports. Ensure that the frontend's API configuration matches the actual backend address.

## Environment Configuration

Never commit database credentials, API keys, private signing keys, or local environment files.

Depending on the component, environment variables may include:

* MongoDB connection string
* Backend port
* API base URL
* Authentication or signing secrets, if implemented

Consult the relevant source files to determine the exact environment variable names expected by each component.

For local development, create the appropriate environment files for each application. If you provide example environment files in the repository, use placeholders rather than real credentials.

## Application Workflow

1. A student enters the required personal, educational, and travel details.
2. The student submits the concession application and supporting documents.
3. The backend processes the application and stores the relevant information in MongoDB.
4. An administrator reviews the submitted application.
5. The administrator approves or rejects the application.
6. Approved applications can be associated with the digital concession and verification workflow implemented in the application.

The exact status transitions and verification behavior depend on the current implementation.

## Security Considerations

* Never commit database credentials, API keys, or private signing keys.
* Validate submitted data on the backend.
* Restrict administrative operations to authorized users.
* Protect uploaded identity documents and personal information.
* Use HTTPS in production.
* Ensure QR codes contain only the information necessary for verification.
* Validate QR authenticity on the backend instead of trusting client-side data alone.

## Development Status

This repository contains the mobile application, administrative dashboard, and backend code for the Digital Concession project.

Some workflows may require further integration, testing, or production hardening. Verify each feature against the current implementation before deploying the system for real users.

## Contributing

1. Fork the repository.
2. Create a feature branch.
3. Implement and test your changes.
4. Commit your work with a descriptive message.
5. Open a pull request describing the changes.

## License

See the repository's `LICENSE` file for licensing terms.
