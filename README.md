 My Awesome Node.js App

 Description
This is a simple Node.js application using Express.js, packaged in a lightweight Docker container. The app serves a basic welcome message when accessed at the root URL.

 Prerequisites
Before running the application, ensure you have the following installed:
- [Docker](https://www.docker.com/get-started)
- [Node.js](https://nodejs.org/en) (Optional, if running locally without Docker)

 Project Structure
```
.
├── Dockerfile
├── package.json
├── src/server.js
```

 Installation & Usage
 Running Locally (Without Docker)
1. Clone the repository:
   ```sh
   git clone <repository-url>
   cd <project-folder>
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Start the server:
   ```sh
   node server.js
   ```
4. Open your browser and visit: `http://localhost:3000`

---

 Running with Docker
1. Build the Docker image:
   ```sh
   docker build -t my-app .
   ```
2. Run the container:
   ```sh
   docker run -p 3000:3000 my-app
   ```
3. Open your browser and visit: `http://localhost:3000`

---

 Dockerfile Breakdown
- Base Image: Uses `node:19-alpine` for a lightweight setup.
- Copy Dependencies: Copies `package.json` and `package-lock.json` to `/usr/app/`.
- Copy Source Code: Copies application files from `src/` to `/usr/app/`.
- Set Working Directory: Changes to `/usr/app/`.
- Install Dependencies: Runs `npm install`.
- Start App: Uses `CMD ["node", "server.js"]` to launch the app.


Developed by Abdulbadie 🚀

