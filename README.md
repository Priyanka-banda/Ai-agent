# 🤖 AI Agent – Browser Automation Project

🌤️ Want to skip the setup? Use cloud for faster, scalable, stealth-enabled browser automation!

---

## 🤖 LLM Quickstart

Direct your favorite coding agent (Cursor, Claude Code, etc.) to `Agents.md`  
Prompt away!

---

## 👋 Human Quickstart

### 1️⃣ Create environment and install Browser-Use (Python >= 3.11)

```bash
uv init && uv add browser-use && uv sync
# uvx browser-use install  # Run if you don't have Chromium installed
```

---

### 2️⃣ (Optional) Add API Keys

Create a `.env` file:

```env
BROWSER_USE_API_KEY=your-key
GOOGLE_API_KEY=your-key
ANTHROPIC_API_KEY=your-key
```

---

### 3️⃣ Run Your First Agent

```python
from browser_use import Agent, Browser, ChatBrowserUse
# from browser_use import ChatGoogle  # ChatGoogle(model='gemini-3-flash-preview')
# from browser_use import ChatAnthropic  # ChatAnthropic(model='claude-sonnet-4-6')
import asyncio

async def main():
    browser = Browser(
        # use_cloud=True,  # Use a stealth browser on Browser Use Cloud
    )

    agent = Agent(
        task="Find the number of stars of the browser-use repo",
        llm=ChatBrowserUse(),
        # llm=ChatGoogle(model='gemini-3-flash-preview'),
        # llm=ChatAnthropic(model='claude-sonnet-4-6'),
        browser=browser,
    )

    await agent.run()

if __name__ == "__main__":
    asyncio.run(main())
```

---

## 🚀 Live Demo

👉 Add your deployed link here  
Example:

```
https://your-app.onrender.com
```

---

## 📸 Preview

Add screenshot inside `images/preview.png`

```markdown
![Preview](images/preview.png)
```

---

## 💡 Quick Public Demo (Temporary)

```python
demo.queue().launch(share=True)
```

Run:

```bash
python webui.py
```

It will generate a temporary public link like:

```
https://xxxxx.gradio.live
```

---

## 🧠 Project Description

🤖 AI Browser Automation Agent  
Built using Browser-Use + LLM  
Automates real-world web tasks using AI  

---

⭐ If you like this project, give it a star!
