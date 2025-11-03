# FinGPT - AI-Powered Financial Assistant

FinGPT is an intelligent financial assistant chatbot built with Streamlit that helps users with finance-related queries, including stock market information, investment advice, insurance, retirement planning, and personal finance management.

## Features

### 💬 AI-Powered Chat Interface
- Intelligent conversational AI trained on financial topics
- Real-time responses using Mixtral-8x7B-Instruct model from Hugging Face
- Context-aware responses with sentiment analysis

### 📈 Stock Market Integration
- Real-time stock price fetching using Yahoo Finance (yfinance)
- Interactive stock price charts with Plotly
- Automatic ticker detection from user queries

### 🎤 Voice Interaction
- Speech-to-text input for hands-free querying
- Text-to-speech output for audio responses
- Built-in microphone support

### 🧠 Advanced NLP Features
- Sentiment analysis of user messages
- Keyword extraction to identify main topics
- Tailored responses based on detected sentiment and keywords

### 📊 Custom Data Integration
- Upload and integrate custom fine-tuning data (TXT files)
- Import CSV data for personalized responses
- Pre-loaded financial Q&A knowledge base

### 💾 Conversation Management
- Persistent chat history within sessions
- Clear chat history functionality
- Conversation summarization feature

## Prerequisites

- Python 3.8 or higher
- Hugging Face API token (for AI model access)
- Microphone (optional, for voice input)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/Reeva28/FinGPT.git
cd FinGPT
```

2. Install required dependencies:
```bash
pip install streamlit huggingface-hub python-dotenv pandas yfinance gtts speechrecognition plotly pyaudio
```

Note: `pyaudio` is required for microphone support. On some systems, you may need to install additional system dependencies first.

3. Create a `.env` file in the project root and add your Hugging Face API token:
```
HUGGING_FACE_TOKEN=your_hugging_face_token_here
```

## Usage

1. Start the Streamlit application:
```bash
streamlit run basic_ai_template.py
```

2. Open your web browser and navigate to the URL shown in the terminal (typically `http://localhost:8501`)

3. Start chatting with the AI assistant about:
   - Stock market queries
   - Investment strategies
   - Insurance questions
   - Retirement planning
   - Personal finance management
   - Financial products and services

### Voice Interaction

- Click the 🎤 button to use voice input
- Click the 🔊 button next to any message to hear it read aloud

### Custom Data Upload

Use the sidebar to:
- Upload custom fine-tuning data (TXT format)
- Import CSV files with additional financial information
- View conversation summaries

## Project Structure

```
FinGPT/
├── basic_ai_template.py      # Main Streamlit application
├── tune_data.txt              # Pre-loaded fine-tuning data (loaded at startup)
├── fine_tuning_data.txt       # User-uploaded training data (created from UI uploads)
├── bot_score.csv              # Sample CSV data (fitness scores and discounts)
├── data.csv                   # User-uploaded CSV data storage
├── .env                       # Environment variables (not in repo)
└── .gitignore                 # Git ignore file
```

## Features Breakdown

### Stock Query Examples
- "What's the current price of AAPL?"
- "Show me Tesla stock performance"
- "Tell me about $MSFT"

### Financial Topics Covered
- Stock market analysis
- Mutual funds
- Investment banking
- Retirement planning (401k, annuities)
- Personal finance (budgeting, savings)
- Insurance (health, disability, umbrella, renters)
- Credit and loans (HELOC, mortgages)
- Financial products and services

## Configuration

### Environment Variables
- `HUGGING_FACE_TOKEN`: Your Hugging Face API token for accessing the AI model

### Customizable Parameters
- Stock history period (default: 1 month)
- AI response max tokens (default: 150)
- Model: Mixtral-8x7B-Instruct-v0.1

## Dependencies

- **streamlit**: Web application framework
- **huggingface-hub**: AI model integration
- **python-dotenv**: Environment variable management
- **pandas**: Data manipulation and CSV handling
- **yfinance**: Real-time stock data fetching
- **gtts**: Text-to-speech conversion
- **speech_recognition**: Speech-to-text conversion
- **plotly**: Interactive chart visualization

## Limitations

- The AI assistant only responds to finance-related queries
- Stock data requires active internet connection
- Voice input requires microphone access
- API rate limits may apply based on your Hugging Face tier

## Privacy & Security

- API tokens should be stored in `.env` file (not committed to version control)
- User conversations are stored only in session state
- No personal data is transmitted beyond the AI model API

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available for educational and personal use.

## Support

For issues, questions, or suggestions, please open an issue on the GitHub repository.

## Acknowledgments

- Powered by Hugging Face's Mixtral-8x7B-Instruct model
- Stock data provided by Yahoo Finance
- Built with Streamlit framework
