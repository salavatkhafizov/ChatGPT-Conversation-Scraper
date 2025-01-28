# ChatGPT Conversation Scraper

A Python utility for extracting conversations from ChatGPT interface with support for text and JSON exports. To use it you need first to share ChatGPT chat and get a weblink for it.

## Features
- Clean extraction of ChatGPT conversations
- Support for TXT and JSON output formats
- Automatic role detection (User/ChatGPT)
- Conversation validation and cleaning
- Detailed logging system

## Requirements

### System Requirements
- Python 3.8+
- Google Chrome (latest version)
- 4GB+ RAM
- Stable internet connection

### Dependencies
```bash
pip install selenium
```

## Installation

### 1. Set Up Environment
```bash
# Create virtual environment
python -m venv venv

# Activate on Windows
venv\Scripts\activate
# OR on macOS/Linux
source venv/bin/activate

# Install dependencies
pip install selenium
```

### 2. ChromeDriver Setup
1. Download [ChromeDriver](https://chromedriver.chromium.org/downloads) matching your Chrome version
2. Add to system PATH:
   - Windows: Extract to PATH directory
   - macOS/Linux: `sudo mv chromedriver /usr/local/bin`
3. Verify installation:
```bash
chromedriver --version
```

## Usage

### Basic Operation
```bash
python gptscraper.py
```

Follow the prompts to:
1. Enter conversation URL
2. Select output format (txt/json)
3. Specify output filename

### Output Formats

#### Text Format (TXT)
```text
User:
Your message here

ChatGPT:
Response here
```

#### JSON Format
```json
{
  "timestamp": "2024-01-20T12:00:00",
  "conversation": [
    {
      "role": "User",
      "content": "Your message"
    },
    {
      "role": "ChatGPT",
      "content": "Response"
    }
  ]
}
```

## Troubleshooting

### Common Issues

1. **ChromeDriver Version Mismatch**
   ```bash
   # Check Chrome version in browser
   chrome://version
   # Download matching ChromeDriver version
   ```

2. **Permission Issues (Unix)**
   ```bash
   chmod +x /path/to/chromedriver
   ```

3. **Timeouts**
   - Increase wait time in configuration
   - Check internet connection

### Logging

The script creates a detailed log file `scraper.log` containing:
- Operation timestamps
- Error messages
- Processing status

## Contributing

1. Fork the repository
2. Create feature branch
3. Submit pull request with:
   - Clear description
   - Test cases
   - Documentation updates

## License

MIT License - see LICENSE file for details

## Support

For issues and suggestions, please use GitHub issues tracker.
