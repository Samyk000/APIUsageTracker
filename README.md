# 🎯 API Usage Tracker - Never Lose Track Again

**A sleek, single-file web app to monitor your OpenRouter & Cerebras AI API usage across multiple keys in real-time.**

<p align="center">
  <img src="https://img.shields.io/badge/Status-Production%20Ready-success?style=for-the-badge" alt="Status">
  <img src="https://img.shields.io/badge/Platform-Web-blue?style=for-the-badge" alt="Platform">
  <img src="https://img.shields.io/badge/Dependencies-ZERO-orange?style=for-the-badge" alt="Dependencies">
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="License">
</p>

***

## 🚨 The Problem

If you're like me, you're juggling **5-6 API keys** from OpenRouter and Cerebras to dodge those annoying daily limits. But here's the chaos:

❌ **A .txt file on desktop** with keys but no idea which one you already burned through today  
❌ **WhatsApp messages to yourself** with the same problem  
❌ **Can't keep 6 temp email accounts logged in** just to check usage dashboards  
❌ **No clue which key to use next** when coding at 2 AM  

**Result?** You waste time manually checking limits, hit rate limits unexpectedly, or forget which key you used where.

***

## ✨ The Solution

**API Usage Tracker** is your personal command center for monitoring multiple API keys across devices.

### Why This Exists

Free tier users on OpenRouter (50 req/day) and Cerebras (1M tokens/day) create multiple accounts to maximize their limits. This tool makes managing them **effortless**.

### What Makes It Special

✅ **Real-time tracking** - Updates usage stats the moment you add a key  
✅ **Cross-device sync** - Use the same key on mobile? Desktop? It tracks it all  
✅ **No backend needed** - Everything runs in your browser (localStorage only)  
✅ **Auto-refresh** - Set it to 3 hours (or any interval) to keep stats fresh  
✅ **Health indicators** - 🟢 Safe / 🟡 Getting high / 🔴 Nearly exhausted  
✅ **Mobile-friendly** - Works perfectly on phones, tablets, and desktops  

***

## 🎯 Features

### Core Functionality
- 📊 **Real-time Usage Stats** - See current usage, limits, and percentages
- 🔄 **Manual & Auto Refresh** - Refresh on-demand or set auto-refresh intervals
- 🏷️ **Custom Labels** - Name your keys ("Work", "Personal", "Backup #2")
- ⏱️ **Reset Timers** - Know exactly when your daily limit resets
- 🕐 **Last Checked** - Track when each key was last verified
- 🗑️ **Easy Management** - Add/remove keys with one click

### Provider Support
- **OpenRouter** - Track free tier (50 req/day) and paid accounts ($10+ = 1000 req/day)
- **Cerebras** - Monitor your 1M tokens/day (or 120M for Cerebras Code users)

### Security & Privacy
- 🔒 **100% Client-Side** - Your API keys never leave your browser
- 💾 **localStorage Only** - No database, no server, no tracking
- 🚫 **No Analytics** - Zero telemetry, zero data collection

***

## 🚀 Quick Start

### Option 1: Use Directly (Recommended)
1. Visit: **https://github.com/Samyk000/APIUsageTracker.git** *(deploy and add link here)*
2. Bookmark it on desktop and mobile
3. Add your API keys
4. Done! 🎉

### Option 2: Self-Host
```bash
# Clone the repo
git clone https://github.com/Samyk000/APIUsageTracker.git

# Open index.html in any browser
open index.html

# Or serve it locally
python -m http.server 8000
```

***

## 📱 Usage Guide

### Adding Your First Key
1. Select **Provider** (OpenRouter or Cerebras)
2. Paste your **API Key** 
3. Add a **Label** (e.g., "Main Account")
4. Click **"Add Key"**
5. Watch it fetch usage instantly ✨

### Understanding the Dashboard

```
╔══════════════════════════════════╗
║  OpenRouter - Work Account  🟢   ║
║  ████████░░░░░░░░░░ 45%         ║
║  23/50 requests                 ║
║  Resets in: 6h 15m              ║
║  Last checked: 2m ago           ║
╠══════════════════════════════════╣
║  Cerebras - Personal       🟡   ║
║  ████████████████░░ 82%         ║
║  820K/1M tokens                 ║
║  Resets in: 4h 30m              ║
╚══════════════════════════════════╝
```

**Color Indicators:**
- 🟢 **Green (0-50%)** - Safe to use
- 🟡 **Yellow (51-85%)** - Getting high
- 🔴 **Red (86-100%)** - Nearly exhausted

***

## 🛠️ Tech Stack

**Built with pure simplicity:**
- HTML5
- CSS3 (Vanilla, no frameworks)
- JavaScript (ES6+, no dependencies)
- localStorage API
- Fetch API

**Total Bundle Size:** ~50KB (one file!)

***

## 📊 How It Works

### Cross-Device Tracking Magic

The beauty? **OpenRouter and Cerebras track usage server-side by API key**, not by device.

**Example:**
1. 🖥️ Use Key #1 in Kilo Code (desktop) → 30 requests
2. 📱 Use Key #1 in mobile app → 15 requests
3. 🌐 Open API Tracker → Shows **45/50 requests** total

The app queries the provider's API to get the **current total usage** for each key. No logging needed!

### Auto-Refresh Strategy
- Default: **3 hours** (prevents API abuse)
- Adjustable: 30s / 1m / 5m / 10m / 3h
- Skips keys that returned errors (no spam)

***

## 🔐 Security & Privacy

### What Gets Stored
- API keys: **localStorage only** (your browser)
- Settings: Auto-refresh preferences, theme choice

### What Doesn't Get Stored
- ❌ Usage history (fetched fresh each time)
- ❌ Request logs
- ❌ Analytics or tracking data

### Recommendations
- ✅ Use on **personal devices only**
- ✅ Don't share your bookmarked link with API keys saved
- ✅ Clear localStorage if using a shared computer

***

## 🤝 Contributing

Found a bug? Have a feature idea? Contributions are welcome!

1. Fork the repo
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

***

## 📜 License

This project is licensed under the **MIT License** - see below for details.

### MIT License

```
MIT License

Copyright (c) 2026 [Sameer (Samyk000)]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

***

## 🙏 Acknowledgments
- **OpenRouter** - For providing affordable LLM access
- **Cerebras** - For the insanely fast and generous free tier
- **Everyone juggling multiple API keys** - This one's for you

***

## 📞 Support

Having issues? Open an issue on GitHub or reach out!

**Star ⭐ this repo** if it saved you time!

***

<p align="center">
  Made with ☕ by developers, for developers who refuse to pay for overpriced APIs
</p>

<p align="center">
  <a href="#-quick-start">Get Started</a> - 
  <a href="#-features">Features</a> - 
  <a href="#-usage-guide">Guide</a> - 
  <a href="#-license">License</a>
</p>
