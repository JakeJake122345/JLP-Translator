# Jake Language+++ Translator

A web application that translates English text into Jake Language+++ and vice versa using binary, hexadecimal, trinary, and custom symbols.

## Features

- Translate English text to Jake Language+++ (binary, hexadecimal, and custom symbols)
- Translate Jake Language+++ back to English
- PostgreSQL database integration to save translation history
- Clean, responsive Bootstrap UI

## How It Works

Jake Language+++ uses different encoding methods for different characters:
- Letters → Binary (ASCII): A = 01000001
- Numbers → Hexadecimal: 9 = 39
- Space → 201 (custom code)
- Punctuation → Special codes (e.g., comma = 2C)

## Tech Stack

- **Backend**: Python with Flask
- **Database**: PostgreSQL
- **Frontend**: HTML, CSS, JavaScript
- **Styling**: Bootstrap (Dark Theme)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/jake-language-translator.git
cd jake-language-translator
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Set up environment variables:
```bash
export DATABASE_URL=your_database_url
export SESSION_SECRET=your_session_secret
```

4. Run the application:
```bash
gunicorn --bind 0.0.0.0:5000 main:app
```

## Project Structure

- `main.py` - Main application file with Flask routes and translation logic
- `models.py` - Database models definition
- `templates/` - HTML templates directory
- `static/` - Static files (CSS, JavaScript)

## API Endpoints

- `POST /translate` - Translate text (accepts JSON with 'text' and 'direction')
- `GET /api/history` - Get translation history as JSON

## Screenshots

![Jake Language+++ Translator](https://via.placeholder.com/800x450.png?text=Jake+Language+++Translator)

## License

MIT