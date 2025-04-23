# 🧠 X Post Creator – MCP Server

A simple and powerful **Model Context Protocol (MCP)** server that enables AI assistants to create posts on **X (formerly Twitter)** via a streamlined API interface. This server makes it easy to integrate post creation functionality into your AI workflows.

---

## 📄 Overview

This server provides a lightweight, Express-based implementation of the MCP server pattern. It acts as a bridge between AI-generated content and X’s posting APIs, securely handling requests and formatting responses with care.

---

## 🚀 Features

- ⚡ **Express-based MCP server implementation**
- 🐦 **X (Twitter) post creation functionality**
- 🔐 **Authentication with X API credentials**
- 🛠️ **Error handling and formatted JSON responses**

---

## ⚙️ Quick Start

1. **Clone the repository**

   ```bash
   git clone https://github.com/your-username/x-post-creator-mcp-server.git
   cd x-post-creator-mcp-server

2. **Install dependencies**

   ```bash
      npm install

3. **Create a .env file in the root directory with your X API credentials:**

   ```bash
    X_API_KEY=your_api_key
    X_API_SECRET=your_api_secret
    X_ACCESS_TOKEN=your_access_token
    X_ACCESS_SECRET=your_access_secret
   
4. **Start the server**
   
    ```bash
        node server.js
---

## 📦 Requirements

- **Node.js v16+**
- **X (Twitter) Developer Account** with appropriate API keys
- Required packages:
  - `express`
  - `@modelcontextprotocol/sdk`
  - `twitter-api-v2`
  - `dotenv`
  - `zod`

---

## 🧪 Usage

Test the tool with `curl`:

```bash
curl -X POST http://localhost:3001/messages?sessionId=test-session \
  -H "Content-Type: application/json" \
  -d '{
    "method": "tool",
    "params": {
      "name": "createPost",
      "arguments": {
        "status": "Testing my MCP server for X posts!"
      }
    }
  }'
