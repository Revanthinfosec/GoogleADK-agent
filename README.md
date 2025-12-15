# Google Search Agent

A simple agent that uses Google's Generative AI to answer questions by performing web searches.

## Features

- Performs web searches using Google Search
- Uses Google's Gemini 2.5 Flash model for generating responses
- Maintains conversation context using session management
- Built on Google's ADK (Agent Development Kit)

## Prerequisites

- Python 3.9+
- Google Cloud Project with Generative AI API enabled
- Google Cloud SDK installed and authenticated

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd Nagent
   ```

2. Create a virtual environment and activate it:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Set up your environment variables:
   - Copy `.env.example` to `.env`
   - Add your Google API key to the `.env` file

## Usage

Run the agent with a query:
```bash
python -m weather_agent.agent
```

Or import and use the agent in your Python code:
```python
from weather_agent.agent import call_agent_async
import asyncio

async def main():
    response = await call_agent_async("What's the latest AI news?")
    print(response)

if __name__ == "__main__":
    asyncio.run(main())
```

## Configuration

Create a `.env` file in the project root with the following variables:
```
GOOGLE_GENAI_USE_VERTEXAI=0
GOOGLE_API_KEY=your_api_key_here
```

## Project Structure

```
Nagent/
├── .gitignore
├── README.md
├── requirements.txt
└── weather_agent/
    ├── __init__.py
    ├── agent.py
    └── .env
```

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.