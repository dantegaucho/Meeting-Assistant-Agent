🧠 **Multilingual Meeting Assistant Bot** 


An intelligent Telegram bot that transcribes, translates, and summarizes multilingual meeting audio using the OpenAI API. Ideal for professionals and teams who want automate meeting notes from voice messages or uploaded audio files.

✨ **Features**

🎙️ **Transcribes** voice notes and audio files (e.g., .mp3, .ogg, .wav)

🌍 **Detects and translates** multiple languages automatically

🧾 **Generates** clear, concise meeting summaries

💬 **Built using** python-telegram-bot + OpenAI Whisper + GPT

⚡ **Fast, accurate, and easy to extend**

🧩 **Requirements**

- Python 3.9 or later
- An OpenAI API key
- A Telegram bot token (from @BotFather)

📁 **Project Structure**
```
Meeting-Assistant-Agent/
├── app.py
├── requirements.txt
├── .env
└── README.md
```

⚙️ **Installation**

1. **Clone the repository**
    ```bash
    git clone https://github.com/yourusername/Meeting-Assistant-Agent.git
    cd Meeting-Assistant-Agent
    ```

2. **Create and activate a virtual environment**
    ```bash
    python -m venv venv
    source venv/bin/activate        # on macOS/Linux
    venv\Scripts\activate           # on Windows
    ```

3. **Install dependencies**
    ```bash
    pip install -r requirements.txt
    ```

4. **Set up your environment variables**

    Create a .env file in the root directory and add:
    ```
    TELEGRAM_BOT_TOKEN=your_telegram_token_here
    OPENAI_API_KEY=your_openai_api_key_here
    ```

🚀 **Running the Bot**

Start the bot with:
```bash
python app.py
```

You should see output like:
🤖 **Multilingual Meeting Assistant Bot is running...**

Then open your Telegram app and send a voice note or audio file to your bot. The bot will:

- **Transcribe** your audio
- **Translate** if needed
- **Generate** a summarized meeting report

🧠 **Example Interaction**

User: (sends a 2-minute voice note)  
Bot:

📝 **Meeting Summary:**  
The team discussed the progress of the logistics app, agreed on a new delivery schedule, and decided to assign Daniel to coordinate supplier communication next week.

⚠️ **Common Errors & Fixes**
| Error | Cause | Solution |
|-------|-------|----------|
| telegram.error.InvalidToken | Wrong or expired Telegram token | Regenerate token via @BotFather |
| telegram.error.Conflict: terminated by other getUpdates request | Bot already running elsewhere | Stop all other sessions or remove existing webhooks |
| openai.error.RateLimitError: You exceeded your current quota | OpenAI API quota exceeded | Upgrade your OpenAI plan or add billing info |
| ValueError: No audio found | Unsupported audio format | Convert to .ogg, .mp3, or .wav before sending |

🔄 **Audio Conversion Tips**  
If Telegram saves files as .oga, convert them to .ogg:

Using FFmpeg (recommended):
```bash
ffmpeg -i input.oga output.ogg
```

Or for Windows users:
```bash
ffmpeg.exe -i input.oga output.ogg
```

## 🧰 **Tech Stack**

- **Language:** Python 3
- **Framework:** python-telegram-bot
- **AI Models:**
  - OpenAI Whisper → for speech-to-text
  - GPT (via OpenAI API) → for summarization and translation

📜 **License**

This project is released under the MIT License. Feel free to use, modify, and distribute it for educational or commercial purposes.

💬 **Author**

Daniel Mutiso  
📧 **Contact:** danmutiso17@gmail.com

🧠 Passionate about AI, data science, and automation tools.
