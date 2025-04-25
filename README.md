## Express.JS Installation Guide

Express.js is a minimal and flexible Node.js web application framework. Follow these steps to install and set up Express.js:

### Prerequisites

Ensure you have the latest Node.js installed. Download it from [Node.js](https://nodejs.org/).

To check your **Node.js & npm** version:

```bash
node -v  # Should show Node.js version (e.g., v18.x or higher)
npm -v   # Should show npm version (e.g., 9.x or higher)
```

### Create a New Project

Open the terminal and type this command with your project name:

```bash
mkdir my-project && cd my-project
```

Then, open the project folder with VS Code:

```bash
code .
```

### NPM Initialize in the Project

```bash
npm init -y
```

This creates a `package.json` file.

### Install Express.js

```bash
npm install express
```

### Create an `index.js` Example File

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

### Run the Server

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



## **📌 License**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## **🤝 Contributing**

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
