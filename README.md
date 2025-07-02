# 🌟 GitHub Stars & Follows Automation API

![GitHub Repo stars](https://img.shields.io/github/stars/Shineii86/GithubStars?color=%23ffcc00&style=flat-square)
![GitHub followers](https://img.shields.io/github/followers/Shineii86?label=Follow%20Me&style=social)
![Vercel](https://img.shields.io/badge/Deploy-Vercel-000?logo=vercel&style=flat-square)
![Made with Node.js](https://img.shields.io/badge/Made%20with-Node.js-green?style=flat-square)

> Automate GitHub starring, following, forking and more using multiple accounts via a secure, key-based Vercel API.

---

## 📘 Features

- 🔒 Secured with dynamic `API_KEY` access control
- ⭐ Star / Unstar public repos
- 👤 Follow / Unfollow users
- 🍴 Fork / Unfork repositories
- 📍 Check fork status per account
- 📦 List all starred repos & followed users
- 🧪 Temporary API Keys valid for 5 minutes
- ⚙️ Token-based multiple GitHub account support

---

## 🔐 Security - API Key

There are two types of keys:

### 🔑 Developer Key (Permanent, Manual)

Manually add in Vercel:
```
API_KEY1 = Quinx_KGxNfr7vdLyf857nU7Sv8c0WDk8_DEV
```

### 🕒 Temporary Key (Expires in 5 Minutes)

Generate using:
```
GET /api/generate?dev_key=Quinx_KGxNfr7vdLyf857nU7Sv8c0WDk8
```

Returns:
```json
{
  "message": "✅ Temporary API Key created",
  "api_key": "TEMP_xxxxx",
  "expires_in": "5 minutes"
}
```

Automatically added to Vercel Environment and removed after 5 minutes.

---

## 🔗 API Usage

### 1️⃣ `/api/star` — Star/Unstar Repos
```
GET /api/star?owner={username}&repo={reponame}&action=star|unstar&key=API_KEY
```

### 2️⃣ `/api/follow` — Follow/Unfollow Users
```
GET /api/follow?owner={username}&action=follow|unfollow&key=API_KEY
```

### 3️⃣ `/api/list` — List Stars & Follows
```
GET /api/list?key=API_KEY
```

### 4️⃣ `/api/fork` — Fork a Repo
```
GET /api/fork?owner={username}&repo={reponame}&key=API_KEY
```

### 5️⃣ `/api/unfork` — Delete Forked Repo
```
GET /api/unfork?owner={username}&repo={reponame}&key=API_KEY
```

### 6️⃣ `/api/fork-status` — Check Fork Status
```
GET /api/fork-status?owner={username}&repo={reponame}&key=API_KEY
```

### 7️⃣ `/api/generate` — Generate Temp API Key
```
GET /api/generate?dev_key=YOUR_DEV_KEY
```

---

## 🧪 Example

```json
{
  "action": "star",
  "target": "vercel/vercel",
  "total_tokens": 3,
  "results": [
    "✅ Star successful",
    "✅ Star successful",
    "❌ Failed (403): Bad credentials"
  ],
  "creator": {
    "github": "@Shineii86",
    "telegram": "@Shineii86"
  }
}
```

---

## 🧑‍💻 Creator Info

- GitHub: [@Shineii86](https://github.com/Shineii86)
- Telegram: [@Shineii86](https://t.me/Shineii86)

---

## 🛠 Deployment

Deploy using Vercel:

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/import/project)

> Add tokens like:
> 
> ```
> TOKEN1 = ghp_...
> TOKEN2 = ghp_...
> ```
> 
> Add your Vercel token + project ID:
> ```
> VERCEL_API_TOKEN = vercel_personal_token
> VERCEL_PROJECT_ID = project_id_from_vercel
> ```

---

## ⚠️ Disclaimer

This project is for **educational and personal use only**. Abusing GitHub APIs may lead to account limitations.
Use responsibly.
