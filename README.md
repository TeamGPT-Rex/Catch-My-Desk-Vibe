# 🖥️ Catch My Desk Vibe

> Upload your desk photo — AI reveals your persona, playlist and perfect desk reward.

---

## 🚀 Deploy in 5 minutes (GitHub + Vercel)

### Step 1 — Create a GitHub repository

1. Go to [github.com/new](https://github.com/new)
2. Name it `catch-my-desk-vibe`
3. Set it to **Public**
4. Click **Create repository**
5. Follow the instructions shown to push an existing folder:

```bash
cd catchmydeskvibe
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/catch-my-desk-vibe.git
git push -u origin main
```

---

### Step 2 — Deploy on Vercel

1. Go to [vercel.com](https://vercel.com) and sign in with GitHub
2. Click **Add New → Project**
3. Import your `catch-my-desk-vibe` repository
4. Vercel auto-detects Vite — just click **Deploy**
5. ✅ Your site is live at `https://catch-my-desk-vibe.vercel.app`

---

### Step 3 — Update the site anytime

Whenever you have an updated `App.jsx`:

```bash
cp /path/to/new/App.jsx src/App.jsx
git add src/App.jsx
git commit -m "update game"
git push
```

Vercel redeploys automatically in ~30 seconds. ✨

---

### Step 4 (optional) — Add a custom domain

1. In Vercel → your project → **Settings → Domains**
2. Add your domain (e.g. `catchmydeskvibe.com`)
3. Follow the DNS instructions for your registrar

---

## 🔑 Important: Anthropic API Key

The AI desk analysis calls `api.anthropic.com` from the browser.
This works in the Claude artifact environment automatically, but on your
own domain you need to handle the API key securely.

**Recommended approach:** create a small serverless function on Vercel
that proxies the request, keeping your key server-side:

```
/api/analyze.js   ← Vercel serverless function (keeps key secret)
```

Create `/api/analyze.js`:

```js
export default async function handler(req, res) {
  const response = await fetch('https://api.anthropic.com/v1/messages', {
    method: 'POST',
    headers: {
      'Content-Type': 'application/json',
      'x-api-key': process.env.ANTHROPIC_API_KEY,
      'anthropic-version': '2023-06-01',
    },
    body: JSON.stringify(req.body),
  });
  const data = await response.json();
  res.json(data);
}
```

Then in `App.jsx`, change the fetch URL from:
```js
"https://api.anthropic.com/v1/messages"
```
to:
```js
"/api/analyze"
```

Add your key in Vercel → Settings → Environment Variables:
```
ANTHROPIC_API_KEY = sk-ant-...
```

---

## 🛠️ Local development

```bash
npm install
npm run dev
# → http://localhost:5173
```

## 📦 Build for production

```bash
npm run build
# → outputs to /dist folder
```
