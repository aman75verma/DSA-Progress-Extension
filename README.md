# 🚀 Code Uploader - Chrome Extension

This Chrome extension allows users to **upload solved coding problems from LeetCode and GeeksforGeeks directly to GitHub**. It's a productivity tool for students and developers who want to automatically organize their coding practice in GitHub repositories.

---

## 🌟 Features

- ✅ Extracts the problem title, code, and language.
- ✅ Supports LeetCode and GeeksforGeeks platforms.
- ✅ Automatically creates a structured folder format on GitHub: `solutions/YYYY/MMMM/DD/problem-title.ext`.
- ✅ Uses a **fine-grained GitHub token** for secure API access.
- ✅ Floating draggable button for triggering uploads.
- ✅ Saves GitHub credentials locally for convenience.

---

## 🧩 Files & Structure

```bash
.
├── manifest.json         # Chrome extension manifest (v3)
├── popup.html            # UI for GitHub configuration
├── popup.css             # Styling for the popup
├── popup.js              # Logic for saving GitHub credentials
├── background.js         # Handles API requests and uploads code to GitHub
├── content.js            # Injected into problem pages to scrape and trigger upload
```

---

## 🛠️ How to Use

### 1. Clone or Create a GitHub Repo

Before using this extension, create a GitHub repository where all your solved problems will be uploaded.

---


### 2. Generate Fine-Grained GitHub Token

1. Go to [GitHub Tokens Settings](https://github.com/settings/tokens?type=beta).
2. Click on **"Generate new token (fine-grained)"**.
3. Set the repository access to your newly created repo.
4. Under "Permissions", allow **`Contents: Read and Write`**.
5. Copy the token and store it somewhere safe.

---

### 3. Load the Extension

1. Open `chrome://extensions/`
2. Enable **Developer mode** (top-right corner).
3. Click **"Load unpacked"**.
4. Select the folder containing this project (`manifest.json` should be inside).

---

### 4. Configure GitHub Details

1. Click on the extension icon.
2. Fill in your **GitHub username**, **repository name**, and **fine-grained token**.
3. Click **Save Data**.

---

### 5. Upload Your Solutions 🚀

- Visit a problem page on LeetCode or GeeksforGeeks.
- A **"Upload to GitHub"** button will appear.
- Click the button after solving a problem — it will upload your code to your repo.

---
### POPUP UI


![Alt Text](/Popup.png)





---
## 📂 Folder Structure on GitHub

Your solutions will be pushed in this format:

```
solutions/
          └── 2025/june/26/
              └── two-sum.cpp
```

---

## ✅ Tech Used

- JavaScript (Vanilla)
- Chrome Extensions API (Manifest V3)
- GitHub REST API
- Local Chrome Storage

---

## 📌 Permissions Used

```json
"permissions": [
  "storage",
  "identity",
  "scripting",
  "alarms"
]
```

---

## 🔒 Security Note

- Your GitHub token is stored **locally only** (in `chrome.storage.local`).
- The extension does **not transmit** your token to any server except GitHub API.

---

## 🧠 Credits

Made with ❤️ for developers who want to automate and organize their practice smartly.
