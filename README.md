# RandomIdeas App

A full-stack application for sharing and managing random ideas. Built with Node.js, Express, MongoDB, and a modern JavaScript frontend bundled with Webpack.

## Features

- **RESTful API**: Create, read, update, and delete ideas.
- **Frontend Interface**: Interactive UI for idea management.
- **MongoDB Integration**: Persistent storage for ideas.
- **Modular Architecture**: Organized codebase with clear separation of concerns.

## Technologies Used

- **Backend**: Node.js, Express
- **Database**: MongoDB
- **Frontend**: Vanilla JavaScript, HTML, CSS
- **Bundler**: Webpack
- **Version Control**: Git

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/en) installed on your machine
- [MongoDB](https://www.mongodb.com/) instance or URI.

### Installation

1. Clone the repository:

```bash
git clone https://github.com/ericstober/randomideas-app.git
cd randomideas-app
```

2. Install backend dependencies:

```bash
npm install
```

3. Install frontend dependencies:

```bash
cd client
npm install
```

4. Configure environment variables:

- Rename `env-example` to `.env` in the root directory.
- Add your MongoDB URI:

```env
MONGO_URI=your_mongodb_uri
```

## Running the Application

### Backend (Expres Server)

Start the server with:

```bash
npm start
```

For development with automatic restarts (Nodemon):

```bash
npm run dev
```

Server will run at `http://localhost:5000`

### Frontend (Webpack Dev Server)

In the `client` directory

```bash
npm run dev
```

Frontend will be availabe at `http://localhost:3000`

To build frontend production files

```bash
npm run build
```

The production build will be put into the `public` folder, which is served by Express.

## REST API Endpoints

### Ideas

| Endpoint       | Description    | Method | Body                    |
| -------------- | -------------- | ------ | ----------------------- |
| /api/ideas     | Get all ideas  | GET    | None                    |
| /api/ideas/:id | Get idea by id | GET    | None                    |
| /api/ideas     | Add idea       | POST   | { text, tag, username } |
| /api/ideas/:id | Update idea    | PUT    | { text, tag, username } |
| /api/ideas/:id | Delete idea    | DELETE | username                |

**Note**: When updating or deleting, the username must match the username of the idea creator.

## Project Structure

```
randomideas-app/
├── client/ # Frontend source code
├── config/ # Configuration files
├── models/ # Mongoose models
├── routes/ # Express route handlers
├── public/ # Static assets
├── .env-example # Environment variable template
├── server.js # Entry point for the backend
├── package.json # Backend dependencies and scripts
```

## License

This project is licensed under the MIT License.
