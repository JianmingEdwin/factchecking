# VeritasCheck — AI Fact Verification

A single-file web application that uses **Claude AI + live web search** to verify claims against mainstream media sources. Fully deployable on GitHub Pages — no server required.

---

## Features

- 🔍 **Live web search** via Claude's built-in tool — checks Reuters, BBC, AP, NYT, scientific journals, etc.
- 📰 **5 verdict types**: TRUE · FALSE · MISLEADING · PARTIALLY TRUE · UNVERIFIABLE
- 📋 **Full reasoning** with confidence level (HIGH / MEDIUM / LOW)
- 🔗 **Source citations** with outlet name, description, URL, and stance
- ⚠ **Context notes** for nuance and caveats
- 🔑 **API key stored locally** in localStorage — never sent anywhere except Anthropic
- 📱 Fully responsive

---

## Deploy to GitHub Pages (2 minutes)

### Option A — Upload directly
1. Create a new GitHub repository
2. Upload `index.html` to the root of the repo
3. Go to **Settings → Pages → Source: Deploy from a branch → main / root**
4. Your app will be live at `https://YOUR_USERNAME.github.io/REPO_NAME/`

### Option B — Git CLI
```bash
git init
git add index.html README.md
git commit -m "Initial commit"
git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git
git push -u origin main
```
Then enable Pages in repo Settings → Pages.

---

## Getting an Anthropic API Key

1. Sign up at https://console.anthropic.com
2. Go to **API Keys → Create Key**
3. Copy the key (starts with `sk-ant-...`)
4. Paste it into the API key field on the app and click **Save Key**

Your key is stored only in your browser's localStorage and is never sent anywhere except directly to Anthropic's API.

---

## Usage

1. Open the deployed app
2. Enter and save your Anthropic API key
3. Type or paste any claim or statement
4. Press **Verify Claim** (or Ctrl/Cmd+Enter)
5. Read the verdict, reasoning, and sources

---

## Technical Notes

- Single HTML file — no build step, no npm, no backend server required
- Uses claude-sonnet-4-20250514 with the web_search_20250305 tool
- The anthropic-dangerous-direct-browser-access header enables direct browser-to-API calls
- All processing is client-side

---

## License

MIT
