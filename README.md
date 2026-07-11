<div align="center">

# 🎬 Hoshiyomi API

### Unified REST API for Short Drama Streaming

Access **16+ short drama platforms** with a single API key.

[![API Docs](https://img.shields.io/badge/API_Docs-docs-green?style=for-the-badge)](https://api.hoshiyomi.my.id/docs)
[![Telegram](https://img.shields.io/badge/Telegram-Bot-26A5E4?style=for-the-badge&logo=telegram)](https://t.me/dramaboxplusbot)

---

**[📚 API Documentation](https://api.hoshiyomi.my.id/docs)** • **[🤖 Telegram Bot](https://t.me/dramaboxplusbot)**

</div>

---

## 📖 About

Hoshiyomi API is a unified REST API that aggregates content from 16+ short drama streaming platforms into a single, easy-to-use interface.

### Why Hoshiyomi API?

- **One API, 16+ Platforms** — No need to integrate multiple platforms separately
- **16 Languages** — Indonesian, English, Korean, Japanese, Chinese, Arabic, and more
- **50,000+ Content** — Thousands of dramas across all platforms
- **Real-time Documentation** — Interactive API explorer with live testing
- **WebSocket Monitoring** — Real-time rate limit tracking

---

## 🚀 Quick Start

### 1. Get Your API Key

**Free Trial (Shared):**
```
HOSHIYOMI-TRIAL
```
- 60 requests per minute
- No expiry
- Shared among all users

**Personal Key (Free):**
Get via Telegram Bot: **[@dramaboxplusbot](https://t.me/dramaboxplusbot)**
- 30 requests per minute
- 1,000 requests per day
- Expires in 3 days
- Private key (1 per user)

### 2. Make Your First Request

**cURL:**
```bash
curl -s "https://api.hoshiyomi.my.id/api/dramabox/trending?lang=id" \
  -H "X-API-Key: HOSHIYOMI-TRIAL" \
  -H "User-Agent: Mozilla/5.0"
```

**Python:**
```python
import requests

resp = requests.get(
    "https://api.hoshiyomi.my.id/api/dramabox/trending",
    params={"lang": "id"},
    headers={
        "X-API-Key": "HOSHIYOMI-TRIAL",
        "User-Agent": "Mozilla/5.0"
    }
)
data = resp.json()
for drama in data["items"]:
    print(f"{drama['title']} - {drama['episodes']} episodes")
```

**JavaScript:**
```javascript
const res = await fetch(
  "https://api.hoshiyomi.my.id/api/dramabox/trending?lang=id",
  {
    headers: {
      "X-API-Key": "HOSHIYOMI-TRIAL",
      "User-Agent": "Mozilla/5.0"
    }
  }
);
const data = await res.json();
console.log(data);
```

---

## 📡 API Endpoints

All endpoints: `https://api.hoshiyomi.my.id/api/{platform}/{endpoint}`

| Endpoint | Method | Description | Parameters |
|----------|--------|-------------|------------|
| `/languages` | GET | List supported languages | - |
| `/trending` | GET | Get trending dramas | `lang` (opt), `page` (opt) |
| `/search` | GET | Search dramas | `q` (req), `lang` (opt), `page` (opt) |
| `/detail` | GET | Get drama details | `id` (req), `lang` (opt) |
| `/allepisode` | GET | Get all episodes with video | `id` (req), `lang` (opt) |
| `/foryou` | GET | Personalized recommendations | `lang` (opt), `page` (opt) |
| `/recommended` | GET | Similar dramas | `lang` (opt) |
| `/hotrank` | GET | Hot rankings | `lang` (opt) |
| `/latest` | GET | Latest dramas | `lang` (opt), `page` (opt) |

**Note:** Each platform supports different endpoints. See [platform documentation](https://api.hoshiyomi.my.id/docs/#platforms) for details.

---

## 📱 Supported Platforms

| Platform | Endpoints | Status |
|----------|-----------|--------|
| DramaBox | 9 | ✅ Active |
| Melolo | 4 | ✅ Active |
| PineDrama | 4 | ✅ Active |
| NetShort | 4 | ✅ Active |
| ShortMax | 4 | ✅ Active |
| FlickReels | 0 | 🟡 Maintenance |
| ReelShort | 5 | ✅ Active |
| GoodShort | 4 | ✅ Active |
| DramaBite | 7 | ✅ Active |
| iDrama | 4 | ✅ Active |
| StarShort | 6 | ✅ Active |
| FlareFlow | 4 | ✅ Active |
| MoboReels | 4 | ✅ Active |
| DramaNova | 0 | 🟡 Maintenance |
| DramaWave | 4 | ✅ Active |
| Playlet | 4 | ✅ Active |

---

## 💰 Pricing & Rate Limits

| Plan | Price | RPM | Daily Limit | Duration |
|------|-------|-----|-------------|----------|
| Trial (Shared) | Free | 60 | Unlimited | Forever |
| Free (Personal) | Free | 30 | 1,000 | 3 days |
| **Starter** | **$3/mo** | 500 | 15,000 | 30 days |
| Starter 3M | $8 | 500 | 15,000 | 90 days |
| **Growth** | **$8/mo** | 2,000 | 50,000 | 30 days |
| Growth 3M ★ | $20 | 2,000 | 50,000 | 90 days |
| **Pro** | **$15/mo** | 10,000 | 200,000 | 30 days |
| Pro 3M | $38 | 10,000 | 200,000 | 90 days |
| **Business** | **$25/mo** | 30,000 | 500,000 | 30 days |
| Business 3M | $63 | 30,000 | 500,000 | 90 days |
| Enterprise | Custom | Custom | Custom | Contact Us |

**Payment Methods (via Telegram Bot):**
- 💲 **USDT (OKX Direct)** — no fee, 3 networks (TRC20/ERC20/Solana)
- 💳 **Card / Other Crypto** — +$1 fee via NOWPayments

---

## 🤖 Telegram Bot

Get API keys via **[@dramaboxplusbot](https://t.me/dramaboxplusbot)**

**Features:**
- 🆓 Free personal keys (30 RPM, 1K/day, 3 days)
- 💳 Paid plans with crypto payments (USDT via OKX)
- 🔄 Auto-delivery after payment confirmation
- 📊 Real-time rate limit monitoring
- 🌐 Multi-language support (EN/ID)

---

## 🔑 Key Formats

| Format | Example | Description |
|--------|---------|-------------|
| Trial | `HOSHIYOMI-TRIAL` | Shared public key, 60 RPM |
| Personal | `HOSHIYOMI-FREE-xxxxxxxx` | Free key, 30 RPM, 3 days |
| Paid | `HOSHIYOMI-PRE-xxxxxxxx` | Paid key, 500-30K RPM |

---

## ❌ Error Codes

| Code | Description |
|------|-------------|
| 400 | Bad Request — Invalid parameters |
| 401 | Unauthorized — Invalid or missing API key |
| 403 | Forbidden — API key expired or suspended |
| 404 | Not Found — Endpoint or resource not found |
| 429 | Too Many Requests — Rate limit exceeded |
| 500 | Internal Server Error |

---

## 🌍 Language Support

| Code | Language | Code | Language |
|------|----------|------|----------|
| `id` | Indonesian | `ko` | Korean |
| `en` | English | `ja` | Japanese |
| `ms` | Malay | `zh` | Chinese |
| `th` | Thai | `ar` | Arabic |
| `vi` | Vietnamese | `fr` | French |
| `de` | German | `es` | Spanish |
| `pt` | Portuguese | `tr` | Turkish |
| `hi` | Hindi | `fil` | Filipino |

---

## 📚 Documentation

**[https://api.hoshiyomi.my.id/docs](https://api.hoshiyomi.my.id/docs)**

---

## 📞 Support

- **Telegram:** [@dramaboxplusbot](https://t.me/dramaboxplusbot)
- **Admin:** [@Widiharu](https://t.me/Widiharu)
- **GitHub Issues:** [Create an issue](https://github.com/beranalpa/dramabox-asia-api/issues)

---

<div align="center">

**Built with ❤️ for drama lovers worldwide**

[![Docs](https://img.shields.io/badge/API_Docs-api.hoshiyomi.my.id-green?style=for-the-badge)](https://api.hoshiyomi.my.id/docs)

</div>
