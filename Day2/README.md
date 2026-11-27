# CampusConnect – Day 2

CampusConnect is an AI-powered college helpdesk assistant built as the Day-2 use case for the Agentic AI learning task. It answers student queries using supplied college information and keeps a short conversation history.

## Features

- **System prompting:** Defines the assistant's role, behaviour, and safety rules.
- **Few-shot prompting:** Classifies student messages as `question`, `complaint`, or `request`.
- **Python dictionaries and JSON:** Demonstrates dictionary-to-JSON conversion and JSON-to-dictionary conversion.
- **Support-ticket extraction:** Converts a student's message into a structured JSON ticket.
- **Conversation memory:** Remembers recent messages during the current program session.
- **Memory trimming:** Keeps the system prompt and the latest five conversation turns.
- **Decorators:** Logs when the chatbot function starts and finishes.
- **Exception handling:** Handles API rate limits, connection errors, and unexpected errors.
- **Continuous chat loop:** Keeps accepting messages until the student types `exit`, `bye`, or `quit`.
- **Conversation history:** Displays messages stored during the current session.

## Technology

- Python
- Groq API (OpenAI-compatible client)
- `openai` Python package
- JSON

## Project structure

```text
Day-2/
├── task.py
└── README.md
```

## Setup

### 1. Install the dependency

```bash
pip install openai
```

### 2. Set your Groq API key

Create a Groq API key and store it as an environment variable named `GROQ_API_KEY`.

**Windows PowerShell (current terminal session):**

```powershell
$env:GROQ_API_KEY="your_groq_api_key"
```

**Google Colab:**

Store the key in Colab Secrets with the name `GROQ_API_KEY`. Do not paste the key into the notebook or upload it to GitHub.

### 3. Run the program

```bash
python task.py
```

## Example interaction

```text
🎓 Welcome to CampusConnect!
Ask me anything about your college.
Type 'exit' to end the conversation.

Student: Hi, my name is Ravi and I am from Data Science.
CampusConnect: Hello Ravi! How can I assist you today?

Student: Which department am I from?
CampusConnect: You are from the Data Science department, Ravi.

Student: exit
CampusConnect: Thank you for using CampusConnect. Goodbye!
```

The exact wording of AI responses may vary.

## Important configuration

Before using the assistant with real students, update `COLLEGE_INFO` in `task.py` with verified information from your college. The current college name and FAQ entries are safe demonstration placeholders. The assistant is instructed not to invent exam dates, fee amounts, attendance rules, or other official policies.

## Security

- Never commit API keys, passwords, or other secrets.
- Keep `GROQ_API_KEY` in environment variables or Colab Secrets.
- Do not ask students to share passwords or sensitive personal information.

## Notes

- Conversation memory is stored in Python memory and lasts only while the program session is running.
- Restarting the Python runtime clears the conversation history.
- The support-ticket function returns a dictionary parsed from the model's JSON response. Review tickets before using them as official records.

