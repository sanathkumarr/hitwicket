
# Turn-Based Chess-Like Game

This is a turn-based chess-like game built using Node.js for the server-side and React for the client-side. The game supports real-time multiplayer interactions using WebSockets (Socket.io) and includes features like move history tracking, chat, and spectator mode.

## Project Structure

- **client/**: Contains the React-based frontend code.
- **server/**: Contains the Node.js-based backend code.

## Prerequisites

Before running the application, ensure you have the following installed on your machine:

- [Node.js](https://nodejs.org/) (v14.x or higher)
- [npm](https://www.npmjs.com/) (comes with Node.js)
- [Git](https://git-scm.com/)

## Setup Instructions

### 1. Clone the Repository

First, you need to clone the repository to your local machine using Git:

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### 2. Install Dependencies

#### Server

Navigate to the `server` directory and install the required packages:

```bash
cd server
npm install
```

This command will install all the necessary Node.js packages listed in the `package.json` file, including:

- **express**: A minimal and flexible Node.js web application framework.
- **socket.io**: A library for real-time web applications.
- **cors**: A middleware to enable Cross-Origin Resource Sharing (CORS).
- **dotenv**: A module to load environment variables from a `.env` file into `process.env`.

#### Client

Navigate to the `client` directory and install the required packages:

```bash
cd ../client
npm install
```

This command will install all the necessary packages for the React frontend, including:

- **react**: A JavaScript library for building user interfaces.
- **react-dom**: This package serves as the entry point to the DOM and server renderers for React.
- **axios**: A promise-based HTTP client for making requests to the server.
- **socket.io-client**: A client library for Socket.io.

### 3. Set Up Environment Variables

For the server, create a `.env` file in the `server` directory with the following content:

```bash
PORT=5000
```

This sets the server to run on port 5000 by default.

### 4. Running the Application

#### Start the Server

To start the Node.js server, navigate to the `server` directory and run:

```bash
npm start
```

The server will start and be available at `http://localhost:5000`.

#### Start the Client

To start the React frontend, navigate to the `client` directory and run:

```bash
npm start
```

The client will be available at `http://localhost:3000`.

### 5. Connect Client to Server

The client is pre-configured to connect to the server running on `http://localhost:5000`. If you are running the server on a different port or deploying to a remote server, update the WebSocket connection URL in the client code.

In the `client/src/config.js` (or equivalent file where the server URL is configured):

```javascript
export const SERVER_URL = "http://localhost:5000"; // Update this if necessary
```

### 6. Access the Game

Open your browser and go to `http://localhost:3000` to start playing the game.

## Features

- **Multiplayer Support**: Players can join and play from different devices.
- **Real-Time Communication**: Game state updates and chat messages are communicated in real-time.
- **Spectator Mode**: Users can join the game as spectators and view the game progress.
- **Move History**: The game tracks and displays the history of all moves.
- **Restart Game**: Players can restart the game at any time.

## Folder Structure

- **client/**
  - `src/`: Contains all the React components and related code.
  - `index.css`: The main CSS file for styling the application.

- **server/**
  - `server.js`: The main server file that handles WebSocket communication, game state management, and HTTP requests.

## Troubleshooting

If you encounter issues while setting up or running the project, consider the following steps:

- **Check Node.js and npm versions**: Ensure you have the required versions installed.
- **Port Conflicts**: If ports 3000 or 5000 are already in use, you can change the ports in the `.env` file for the server or modify the `package.json` for the client.
- **CORS Issues**: If you encounter CORS errors, make sure the server is correctly configured to accept requests from the client.

## Contributing

If you'd like to contribute to the project, feel free to fork the repository and submit a pull request.

## License

This project is licensed under the MIT License.
