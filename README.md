# RuleBot 🤖

A Python-based rule-based chatbot that engages users in interactive conversations using pattern matching and predefined responses.

## Features

- **Intent Recognition**: Uses regex patterns to identify user intents (greetings, questions, personal queries)
- **Dynamic Responses**: Multiple response variations to avoid repetitive conversations
- **Conversation Memory**: Caches responses and prevents consecutive identical replies
- **Sci-Fi Personality**: Engaging backstory with references to fictional worlds like "Nexus Prime"
- **Graceful Exit**: Multiple exit commands supported (quit, bye, exit, goodbye)
- **Fallback Handling**: Smart responses for unrecognized input patterns

## How It Works

RuleBot operates on a rule-based system that:
1. Analyzes user input using compiled regex patterns
2. Matches input to predefined intent categories
3. Selects appropriate responses from curated response pools
4. Maintains conversation flow with fallback mechanisms

## Intent Categories

- **Planet/Origin Questions**: Responds with creative sci-fi world descriptions
- **Why Questions**: Provides philosophical answers about purpose and connection
- **Greetings**: Acknowledges users by name with friendly responses
- **Personal Questions**: Shares information about AI capabilities and interests
- **Mood Inquiries**: Expresses optimal functioning and reciprocal interest

## Installation

No external dependencies required! Just ensure you have Python 3.x installed.

```bash
git clone https://github.com/yourusername/rulebot.git
cd rulebot
python rulebot.py
```

## Usage

1. Run the script: `python rulebot.py`
2. Enter your name when prompted
3. Start chatting with the bot
4. Use commands like `quit`, `exit`, or `goodbye` to end the conversation

## Example Interactions

```
RuleBot: Hi, I'm RuleBot! What's your name?
You: Alice

RuleBot: Nice to meet you Alice! I am a rule-based chatbot...
You: yes

RuleBot: why are you here?
You: Hi there!
RuleBot: Hello again, Alice! What's on your mind?

You: Where are you from?
RuleBot: I come from Nexus Prime, a crystalline world where technology 
         and nature exist in perfect harmony. The cities float among 
         iridescent clouds, and knowledge flows freely through the 
         quantum network. Would you like to know more? 🌌

You: Why are you here?
RuleBot: To bridge the gap between different forms of intelligence. 
         Shall we explore together? 🌉

You: quit
```

## Technical Details

- **Language**: Python 3.x
- **Dependencies**: Standard library only (`re`, `random`, `datetime`)
- **Architecture**: Object-oriented design with modular intent handling
- **Performance**: Response caching for improved efficiency

## Code Structure

```
RuleBot/
├── rulebot.py          # Main chatbot implementation
└── README.md           # This file
```

### Key Classes and Methods

- `RuleBot`: Main chatbot class
  - `greet()`: Initial user interaction and setup
  - `chat()`: Main conversation loop
  - `match_reply()`: Intent matching and response selection
  - `*_intent()`: Individual intent handlers

## Customization

### Adding New Intents

1. Add a regex pattern to `intent_patterns` dictionary
2. Create a corresponding `*_intent()` method
3. Add response variations to keep conversations dynamic

```python
# Example: Adding a joke intent
self.intent_patterns['joke_intent'] = re.compile(r'.*(joke|funny|humor).*?', re.IGNORECASE)

def joke_intent(self):
    jokes = [
        "Why don't robots ever panic? They have nerves of steel! 🤖",
        "What do you call a robot who takes the long way? R2-Detour! 🛣️"
    ]
    return random.choice(jokes)
```

### Modifying Personality

Edit the response arrays in each `*_intent()` method to change the bot's personality, tone, or backstory.

## Use Cases

- **Educational**: Learn chatbot fundamentals and NLP pattern matching
- **Demonstration**: Showcase rule-based conversational AI techniques
- **Foundation**: Starting point for more complex chatbot systems
- **Entertainment**: Interactive conversation partner with unique personality

## Contributing

Contributions are welcome! Here are some ways to help:

- 🆕 Add new intent patterns and responses
- 🎭 Expand personality traits and backstory elements
- 🔧 Improve conversation flow and context handling
- 📚 Enhance documentation and examples
- 🐛 Fix bugs and optimize performance

### Development Setup

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Make your changes and test thoroughly
4. Submit a pull request with a clear description

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgments

- Built with Python's standard library
- Inspired by classic rule-based chatbot architectures
- Designed for educational and demonstration purposes

---
