# 🚀 React Emoji Dictionary - Jenkins CI/CD Deployment

This project is a **React-based Emoji Dictionary App** automatically built and deployed using **Jenkins** with **Docker** support.

## 🧠 Project Overview

This simple React app displays an emoji list with names and meanings. It is deployed using a Jenkins CI/CD pipeline, which:

1. Checks out the code from GitHub
2. Installs dependencies
3. Builds the React app
4. Copies build files to a host directory served by Nginx

---

## 📁 Project Structure

```
.
├── Jenkinsfile
├── public/
├── src/
│   ├── components/
│   │   ├── App.jsx
│   │   └── dict.jsx
│   ├── emojipedia.jsx
│   └── index.jsx
├── dist/ (auto-generated)
└── dist_for_deploy/ (auto-generated)
```

---

## ⚙️ Setup Instructions

1. **Clone this repo**
   `git clone https://github.com/your-username/emoji-dictionary.git`

2. **Set up Jenkins** with:

   * Docker installed
   * Node.js inside Docker
   * Nginx running on host, serving `/home/<user>/jenkins-react-deploy`

3. **Trigger Jenkins build** to automatically build and deploy the app.

✅ Replace `<user>` with your actual Linux username in Jenkinsfile.

---

## 👨‍💻 Tech Stack

* **React**
* **Jenkins**
* **Docker**
* **Nginx**

---

## 📷 Preview

*(Add a screenshot of the deployed app here)*