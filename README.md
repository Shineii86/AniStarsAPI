# 🌟 GitHub Stars & Follows API

![GitHub Repo stars](https://img.shields.io/github/stars/Shineii86/AniStarsAPI?style=social)
![Vercel](https://img.shields.io/badge/Deployed%20on-Vercel-000?logo=vercel&style=flat-square)
![Made with Node.js](https://img.shields.io/badge/Made%20with-Node.js-green?style=flat-square)

> A secure, token-based API to automatically star, unstar, follow, unfollow, and list starred/followed GitHub data using multiple accounts — privately hosted on Vercel.

---

## 📦 Features
- ✅ Star or Unstar Repositories
- ✅ Follow or Unfollow Users
- ✅ List Starred Repos and Followed Users
- ✅ API Key Protection
- ✅ Unlimited GitHub Tokens

---

## 🚀 API Endpoints

### ⭐ `/api/star`
**Star or Unstar a repository**
```
GET /api/star?owner=OWNER&repo=REPO&action=star|unstar&key=YOUR_KEY
```

### 👤 `/api/follow`
**Follow or Unfollow a GitHub user**
```
GET /api/follow?owner=USERNAME&action=follow|unfollow&key=YOUR_KEY
```

### 📃 `/api/list`
**List starred repos & followed users per token**
```
GET /api/list?key=YOUR_KEY
```

---

## 🔐 API Key Security

In `.env` or Vercel Settings, add multiple keys:
```
API_KEY1 = yourkey1
API_KEY2 = yourkey2
API_KEY3 = yourkey3
```
Use them in `?key=yourkey1` for access.

---

## ⚙️ Setup (Vercel)

1. Upload all files to GitHub
2. Connect to [Vercel](https://vercel.com)
3. Set Environment Variables:
```
TOKEN1 = ghp_XXXXXXXXXXXXXXXXXXX
TOKEN2 = ghp_YYYYYYYYYYYYYYYYYYY
...
API_KEY1 = shine123
API_KEY2 = friend456
```
4. Deploy!

---

## 🖥 UI Preview (Frontend)

Visit the homepage to use the follow/unfollow form:
- Input GitHub username
- Choose action
- Enter your API key
- View live results from all tokens

---

## 👨‍💻 Created By
- GitHub: [@Shineii86](https://github.com/Shineii86)
- Telegram: [@Shineii86](https://t.me/Shineii86)

---

## ⚠️ Disclaimer
> This tool is for educational and private automation use only.
> Violating GitHub’s Terms of Service may result in penalties.
