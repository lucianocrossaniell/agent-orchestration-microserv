# 🤖 Single Agent - Your Personal AI Assistant

A simple AI agent that you can chat with in your browser. It can do math, analyze text, and have conversations using OpenAI's GPT-4.

## What Can It Do?

- 💬 **Chat naturally** like talking to a human
- 🧮 **Calculate math** - Ask it "What's 25 * 4 + 10?"
- 📝 **Analyze text** - Give it text and it counts words/characters
- 🎯 **Smart tool usage** - Automatically picks the right tool for each task

## Quick Start (3 Steps)

### 1. Get an OpenAI API Key
1. Go to [OpenAI's website](https://platform.openai.com/api-keys)
2. Create an account if you don't have one
3. Create a new API key
4. Copy the key (it looks like: `sk-proj-...`)

### 2. Setup the Agent
```bash
# Run the setup script
./start.sh
```
The script will:
- Install Python packages
- Create a `.env` file
- Ask you to add your API key

### 3. Add Your API Key
1. Open the `.env` file in a text editor
2. Replace `your_openai_api_key_here` with your actual API key
3. Save the file
4. Run `./start.sh` again

## How to Use It

### Chat Interface (Easiest)
1. Run `./start.sh` to start the agent
2. Open `chat.html` in your web browser
3. Start chatting!

### Try These Example Messages:
- "Hello! What can you help me with?"
- "Calculate 15 * 23 + 7"
- "Analyze this text: 'The quick brown fox jumps over the lazy dog'"
- "What's the square root of 144?"
- "Can you help me with basic math?"

### API Documentation
Visit `http://localhost:8000/docs` to see all available API endpoints.

## File Structure (What Each File Does)

```
single-agent/
├── start.sh          # 🚀 Main startup script - run this to start everything
├── chat.html         # 💬 Web chat interface - open this in your browser
├── main.py           # 🌐 Web server that handles requests
├── agent.py          # 🤖 The AI agent with tools (calculator, text analyzer)
├── config.py         # ⚙️  Configuration settings from .env file
├── requirements.txt  # 📦 List of Python packages needed
├── .env.example      # 📋 Template for your settings
├── .env             # 🔐 Your actual settings (you create this)
└── Dockerfile       # 🐳 For running in Docker (optional)
```

## Customization

### Change the Agent's Name
Edit `.env` file:
```bash
AGENT_NAME=MyPersonalAssistant
AGENT_DESCRIPTION=My custom AI helper
```

### Use Different AI Model
Edit `.env` file:
```bash
OPENAI_MODEL=gpt-3.5-turbo  # Faster and cheaper
# or
OPENAI_MODEL=gpt-4          # Smarter but slower
```

### Change Server Port
Edit `.env` file:
```bash
PORT=3000  # Use port 3000 instead of 8000
```

## Troubleshooting

### "OpenAI API key not provided"
- Make sure you copied your API key correctly to the `.env` file
- The key should start with `sk-proj-` or `sk-`
- Don't include quotes around the key

### "Agent not ready"
- Check that your API key is valid
- Make sure you have internet connection
- Verify you have credits in your OpenAI account

### "Module not found"
- Run the setup script again: `./start.sh`
- Make sure Python 3.8+ is installed

### Can't access the chat interface
- Make sure the agent is running (you should see "Starting SingleAgent server...")
- Try visiting `http://localhost:8000` first to check if the server is working
- Check if another program is using port 8000

## What's Next?

This single agent is designed to be the foundation for more advanced features:

- 🔗 **Multi-agent systems** - Multiple specialized agents working together
- 🌐 **Web deployment** - Put your agent online for others to use
- 🔧 **Custom tools** - Add your own special abilities
- 📊 **Memory systems** - Let the agent remember past conversations

## Need Help?

- Check the troubleshooting section above
- Look at the example messages in the chat interface
- Visit `http://localhost:8000/docs` for technical API details
- The agent logs helpful information when running - check the terminal output

## Requirements

- **Python 3.8+** (check with `python3 --version`)
- **Internet connection** (to reach OpenAI's servers)
- **OpenAI API key** (free tier available)
- **Modern web browser** (Chrome, Firefox, Safari, Edge)