# 🎓 English Tutor Bot - AI-Powered Telegram Chatbot

An intelligent English learning assistant for Telegram that helps users practice conversational English through natural chat, voice messages, and image analysis.

![n8n](https://img.shields.io/badge/n8n-workflow-orange)
![Telegram](https://img.shields.io/badge/Telegram-Bot-blue)
![AI](https://img.shields.io/badge/AI-Powered-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

## ✨ Features

- 💬 **Natural Conversation** - Chat like a real friend, not a robot
- 🎤 **Voice Messages** - Send voice, get text response (Speech-to-Text)
- 🔊 **Text-to-Speech** - Receive audio responses to improve listening
- 📸 **Photo Analysis** - Send images and discuss them in English
- 🧠 **Conversation Memory** - Remembers context for natural flow
- 📝 **Grammar Correction** - Gentle corrections without embarrassment
- 📚 **Vocabulary Building** - Highlights new words for learning

## 🏗️ Architecture

```
┌─────────────────┐     ┌──────────────┐     ┌─────────────────┐
│  Telegram User  │────▶│   n8n Bot    │────▶│   AI Models     │
│  (Text/Voice/   │◀────│  (Workflow)  │◀────│ (Gemini/Groq)   │
│   Photo)        │     └──────────────┘     └─────────────────┘
└─────────────────┘            │
                               ▼
                    ┌──────────────────┐
                    │  ElevenLabs TTS  │
                    │  (Voice Output)  │
                    └──────────────────┘
```

## 📋 Required Credentials

| Service | Purpose | Get it from |
|---------|---------|-------------|
| **Telegram Bot API** | Bot communication | [@BotFather](https://t.me/BotFather) |
| **Google Gemini API** | Main AI model | [Google AI Studio](https://aistudio.google.com/) |
| **Groq API** | Fast inference + Whisper STT | [console.groq.com](https://console.groq.com/) |
| **ElevenLabs API** | Text-to-Speech (optional) | [elevenlabs.io](https://elevenlabs.io/) |

## 🚀 Installation

### 1. Import Workflow
1. Open your n8n instance
2. Go to **Workflows** → **Import from File**
3. Upload `English_Tutor_Bot_Template_v2.json`

### 2. Configure Credentials
After import, click on each red-highlighted node and add credentials:

1. **Telegram Trigger** → Add Telegram API credential
2. **Google Gemini Chat Model** → Add Google PaLM API credential
3. **Groq Chat Model** → Add Groq API credential
4. **Convert text to speech** → Add ElevenLabs API credential (optional)

### 3. Activate
Toggle the workflow to **Active** and start chatting with your bot!

## 📁 Files

| File | Description |
|------|-------------|
| `English_Tutor_Bot_Template_v2.json` | Main n8n workflow |
| `README.md` | This documentation |

## 🎯 How It Works

1. **User sends message** (text, voice, or photo)
2. **Switch node** routes to appropriate handler
3. **Voice** → Groq Whisper transcribes to text
4. **Photo** → Gemini Vision analyzes image
5. **AI Agent** generates friendly response
6. **Response sent** as text + optional audio

## 💡 Customization

### Change AI Personality
Edit the `Code in JavaScript` node to modify the system prompt:
- Adjust conversation style
- Add/remove daily phrases
- Change vocabulary preferences

### Add Custom Words
Edit the `words` node to add vocabulary you want to practice.

## 🤝 Contributing

Feel free to fork, improve, and submit pull requests!

## 📄 License

MIT License - Feel free to use for personal or commercial projects.

## 👤 Author

**adembtr** - [GitHub](https://github.com/adembtr)

---

⭐ If this helped you, please star the repo!

---

Built by [Adem Batur](https://github.com/adembtr) · License: [MIT](LICENSE)
