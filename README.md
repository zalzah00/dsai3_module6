# Local Setup Guide: GenAI Workshop (Module 6: Lessons 6.2 - 6.6)

---

### 1. Create the Environment
Save the `environment.yml` file in your project folder, open your terminal (or Anaconda Prompt), and run:

```bash
conda env create -f environment.yml
```

### 2. Configure Your Keys
Create a file named `.env` in your project folder and paste the following, replacing the placeholders with your actual keys. (You likely already have this from Module 5, just ensure your Hugging Face and Telegram keys are included!)

```bash
GROQ_API_KEY=your_key_here
GEMINI_API_KEY=your_key_here
HF_TOKEN=your_key_here
TELEGRAM_BOT_TOKEN=your_key_here
```

### 3. Initialization Code
Paste this into the **first cell** of your Jupyter Notebooks to load your keys automatically.

```python
import os
from dotenv import load_dotenv

# Load keys from .env
load_dotenv()

# Required keys for the lessons
os.environ["GROQ_API_KEY"] = os.getenv("GROQ_API_KEY", "")
os.environ["GEMINI_API_KEY"] = os.getenv("GEMINI_API_KEY", "")
os.environ["HF_TOKEN"] = os.getenv("HF_TOKEN", "")
os.environ["TELEGRAM_BOT_TOKEN"] = os.getenv("TELEGRAM_BOT_TOKEN", "")
```

---
### 4. Running the Notebook
1. Start Jupyter: `jupyter notebook`
2. Open your lesson file.
3. Click **Kernel** -> **Change Kernel**.
4. Select **"mod6envt"**.