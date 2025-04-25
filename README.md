# 🔴🟠🟡 Express.JS Installation Guide

Express.js is a minimal and flexible Node.js web application framework. Follow these steps to install and set up Express.js:

## **🟪🟦🟩 Prerequisites**

Ensure you have the latest Node.js installed. Download it from [Node.js](https://nodejs.org/).

To check your **Node.js & npm** version:

```bash
node -v  # Should show Node.js version (e.g., v18.x or higher)
npm -v   # Should show npm version (e.g., 9.x or higher)
```

### **❏❏❏ Create a New Project**

Open the terminal and type this command with your project name:

```bash
mkdir my-project && cd my-project
```

Then, open the project folder with VS Code:

```bash
code .
```

## **🟪🟦🟩 Install Express.JS in the Project**

### **❏❏❏ NPM Initialize in the Project**

```bash
npm init -y
```

This creates a `package.json` file.

### **❏❏❏ Install Express.js**

```bash
npm install express
```

### **❏❏❏ Create an `index.js` Example File**

```js
const express = require("express");
const app = express();

app.get("/", (req, res) => {
  res.send("Hello, World!");
});

app.listen(3000, () => {
  console.log("Server is running on port 3000");
});
```

## **🟪🟦🟩 Run the Server**

Modify the `package.json` file in your project and update the **scripts section**:

```json
"scripts": {
    "dev": "node index.js",
    "build": "node index.js"
},
```

To run the **Node.js server**, execute the following command:

```bash
npm run dev   # Development Mode
npm run build # Production Mode
```

Open `http://localhost:3000/` in a browser to see the output.

---

# **🔴🟠🟡 Recommended: Nodemon (VSCode Plugin)**

Nodemon automatically restarts your **Node.js** app when file changes are detected.

## **🟪🟦🟩 Install Nodemon Globally**

```bash
npm install -g nodemon
```

or install it as a **dev dependency** for a project:

```bash
npm install --save-dev nodemon
```

## **🟪🟦🟩 Run Nodemon**

Modify the `"scripts"` section in your **`package.json`** file:

```json
"scripts": {
  "start": "node index.js",
  "dev": "nodemon index.js"
},
```

Now, you can start the server using:

```bash
npm run dev
```

---

# **🔴🟠🟡 VS Code - Debug Configuration**

## **🟪🟦🟩 Create a Debug Configuration**

1. Open **VS Code**.
2. Go to **Run and Debug** (`Ctrl + Shift + D`).
3. Click **"create a `launch.json` file"**.
4. Select **"Node.js"**.
5. Replace the content of `launch.json` with:

```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "node",
      "request": "launch",
      "name": "Launch with Nodemon",
      "runtimeExecutable": "nodemon",
      "program": "${workspaceFolder}/index.js",
      "restart": true,
      "console": "integratedTerminal",
      "internalConsoleOptions": "neverOpen"
    }
  ]
}
```

Save the file.

## **🟪🟦🟩 Test and Debug**

- Add `console.log()` statements in your `index.js` file.
- Modify and **save** the file to check if Nodemon **automatically restarts**.
- Start debugging in VS Code using **F5**.

---

# **🔴🟠🟡 Essential Node.JS Packages**

| Package Name     | Description                 | Install Command                     |
| ---------------- | --------------------------- | ----------------------------------- |
| **express**      | Web framework for Node.js   | `npm install express`               |
| **nodemon**      | Auto-restarts server        | `npm install -g nodemon`            |
| **dotenv**       | Loads environment variables | `npm install dotenv`                |
| **cors**         | Enables CORS                | `npm install cors`                  |
| **mongoose**     | MongoDB ODM                 | `npm install mongoose`              |
| **mysql2**       | MySQL driver                | `npm install mysql2`                |
| **pg**           | PostgreSQL client           | `npm install pg`                    |
| **bcrypt**       | Password hashing            | `npm install bcrypt`                |
| **jsonwebtoken** | JWT authentication          | `npm install jsonwebtoken`          |
| **multer**       | File uploads middleware     | `npm install multer`                |
| **axios**        | HTTP client                 | `npm install axios`                 |
| **socket.io**    | WebSockets                  | `npm install socket.io`             |
| **jest**         | Testing framework           | `npm install --save-dev jest`       |
| **supertest**    | HTTP assertions             | `npm install --save-dev supertest`  |
| **mocha & chai** | Testing framework           | `npm install --save-dev mocha chai` |
| **eslint**       | Linter                      | `npm install eslint --save-dev`     |

## **🟪🟦🟩 Useful NPM Commands**

| Command                    | Description                         |
| -------------------------- | ----------------------------------- |
| `npm install <package>`    | Installs a package locally          |
| `npm install -g <package>` | Installs a package globally         |
| `npm uninstall <package>`  | Removes a package                   |
| `npm update`               | Updates all installed packages      |
| `npm list`                 | Lists installed packages            |
| `npm run <script>`         | Runs a script from `package.json`   |
| `npm audit`                | Checks for security vulnerabilities |

### **❏❏❏ Update NPM (if needed):**

```bash
npm install -g npm@latest
```

---

# **📌 License**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

# **🤝 Contributing**

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

# **📞 Contact**

For support or inquiries, email us at [support@example.com](mailto:support@example.com).
