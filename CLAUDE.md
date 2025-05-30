# my-schedule Development Guidelines

## Commands
- Run script: `python main.py` (default shows next 2 weeks of events, excluding holidays)
- Show available slots: `python main.py --available-slots` or `python main.py -a`
- Show available slots with minimum duration: `python main.py -a 2` (for 2+ hour slots)
- Show available slots with total hours: `python main.py --available-slots --show-total-hours` or `python main.py -a -t`
- Combine minimum hours with total: `python main.py -a 2 -t` (for 2+ hour slots with total)
- JSON output: `python main.py --format json` or `python main.py -f json`
- Set weekday language: `python main.py --weekday-lang en` or `python main.py -w en`
- Include holidays: `python main.py --include-holidays` (holidays are excluded by default)
- Run tests: `python -m pytest test_main.py -v`
- Run tests with coverage: `python -m pytest --cov=main test_main.py`
- Generate HTML coverage report: `python -m pytest --cov=main --cov-report=html test_main.py`
- Lint code: `python -m flake8 main.py` (recommended to install)
- Type check: `python -m mypy main.py` (recommended to install)

## Setup
- Install dependencies: `pip install -r requirements.txt`
- Create client_secret.json (from Google Calendar API Console)

## Code Style
- Imports: Group standard library, third-party, and local imports with blank lines between groups
- Docstrings: Use Google-style docstrings with Args/Returns sections
- Formatting: 4-space indentation, max line length 100
- Error handling: Use try/except for potential errors, provide clear error messages
- Timezone: All dates should be properly converted to JST for display
- Variable naming: snake_case for variables/functions, UPPER_CASE for constants
- Comments: Add comments for complex logic blocks or timezone conversions