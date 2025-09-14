# 6obcy TUI Chat Bot

A terminal client for [6obcy.org](https://6obcy.org) featuring:
- Anonymous conversations with random people
- AI-powered automatic responses (OpenAI fine-tuned model)
- Captcha solving via 2captcha
- Simple TUI (Text User Interface) based on `neo-blessed`

## ✨ Features

- ✅ WebSocket connection to 6obcy server
- ✅ Terminal interface (`neo-blessed`)
- ✅ Message history and scrolling
- ✅ Captcha handling:
  - Manual code entry
  - Or automatic solving via 2captcha API
- ✅ Auto-response mode (AI responds for you)
- ✅ Online users counter
- ✅ Commands: `/topic`, `/dis`, `/start`, `/stop`, `/auto`

---

## 🚀 Installation

1. Clone the repository and install dependencies:

```bash
git clone https://github.com/emkacztoja/6obcy-jebator.git
cd 6obcy-jebator
npm install
```

2. Create a `.env` file with required API keys:

```env
OPENAI_API_KEY=your_openai_api_key_here
CAPTCHA2_API=your_2captcha_api_key_here   # optional
WELCOME=hey there 👋                      # optional welcome message
```

---

## ▶️ Running

```bash
npm start
```

After startup:
- The app connects to the 6obcy server
- If captcha appears, a page opens at `http://localhost:<port>/captcha`
- You can type messages in the bottom terminal field

---

## 💻 Controls

- `/topic` → Get random question from server
- `/dis` → Disconnect
- `/start` → Start conversation
- `/stop` → End conversation and disable auto-reconnect
- `/auto` → Toggle AI auto-responses
- `Esc` or `Ctrl+C` → Exit program

---

## ⚠️ Warning

- Using bots on 6obcy.org may violate their terms of service. This project is for educational and testing purposes only.
- Never share your API keys publicly.

---

## 🛠️ Tech Stack

- [Node.js](https://nodejs.org/)
- [WebSocket](https://www.npmjs.com/package/ws)
- [neo-blessed](https://github.com/chjj/blessed)
- [ora](https://www.npmjs.com/package/ora)
- [colors](https://www.npmjs.com/package/colors)
- [express](https://expressjs.com/)
- [OpenAI API](https://platform.openai.com/)
- [2captcha API](https://2captcha.com/)

---

## 🤖 AI Configuration

The bot uses a fine-tuned OpenAI GPT-3.5-turbo model specifically trained for natural Polish conversations. The AI is configured to respond as "Kasia", a 17-year-old girl from Warsaw, using natural teenage language patterns.

### Model Details:
- **Model**: `ft:gpt-3.5-turbo-0125:personal:6obcy-chatbot:CFmOQ1Kb`
- **Temperature**: 0.8 (0.9 on retries)
- **Max Tokens**: 120
- **Personality**: Natural Polish teenager responses

---

## 📝 License

This project is for educational purposes only. Use at your own risk.
