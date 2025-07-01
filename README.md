# 🐦 AI Twitter Poster with MCP

An AI-powered agent built using the **Model Context Protocol (MCP)** that can generate and post tweets directly to your Twitter account.

## 🚀 Features

* Accepts user input or topics to generate tweet content
* Posts tweets to your Twitter account using the Twitter API v2
* Uses Model Context Protocol for LLM interaction
* Lightweight and developer-friendly

---

## ⚠️ Usage Disclaimer

> **Important:** This project interacts with the Twitter (X) API to publish tweets on behalf of a user account. Please follow the rules below to avoid penalties:

* This tool is for educational and experimental purposes only.
* Do **not** use this agent to spam, mass-post, or distribute misleading content.
* Make sure your Twitter account complies with **Twitter’s Developer Agreement and Policy**: [https://developer.twitter.com/en/developer-terms/agreement](https://developer.twitter.com/en/developer-terms/agreement)
* Twitter may **suspend or permanently ban** accounts that:

  * Use automated bots without proper labeling
  * Violate rate limits
  * Post spammy or low-quality content

By using this tool, you accept full responsibility for any consequences from violating Twitter’s terms.

---

## 🧠 How It Works

1. The MCP server listens for AI agent requests
2. The agent sends generated tweet content to the server
3. The server authenticates with the Twitter API and posts the tweet

---

## 🛠️ Tech Stack

* **Node.js** + **Express** — REST server
* **@modelcontextprotocol/sdk** — LLM agent protocol
* **Twitter API v2** — for posting tweets
* **Axios** — HTTP client for API requests
* **dotenv** — environment variable handling

---

## 📁 Project Structure

```
AI-AGENT-MPC-SERVER/
├── client/
│   ├── index.js              # Client or MCP initiator (if used)
│   ├── package.json
│   ├── .env
│   └── node_modules/
├── server/
│   ├── index.js              # Express + MCP server setup
│   ├── mpc.tool.js           # Tool for posting to Twitter
│   ├── package.json
│   ├── .env
│   └── node_modules/
├── .gitignore
├── README.md
```

---

## 🔧 Setup Instructions

### 1. Clone the repo

```bash
git clone https://github.com/NamanGarg11/Ai-TwitterPoster-mpc
cd ai-twitter-agent-mpc-server
```

### 2. Install dependencies (client and server)

```bash
cd client && npm install
cd ../server && npm install
```

### 3. Create `.env` files in both folders if needed

```env
# server/.env
TWITTER_BEARER_TOKEN=your_twitter_api_token_here
```

> Get this token from [developer.twitter.com](https://developer.twitter.com/en/portal/dashboard).

### 4. Run the server

```bash
cd server
node index.js
```

---

## 📬 Example Request (via MCP client)

```json
{
  "tool": "post_to_twitter",
  "parameters": {
    "text": "Just built my first AI agent that tweets for me using MCP! 🚀 #AI #TwitterBot"
  }
}
```

## 🧩 Future Improvements

* Add error handling for rate limits
* Support media uploads
* Build a frontend UI to input topics
* Add queue and logs of tweets

---

## 🤝 Contributing

Pull requests and stars are welcome! Feel free to fork and build upon it.

---

## 📜 License

MIT License
