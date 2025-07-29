Earth911 LLM-Based Scraper

This project is a technical task for scraping recycling center data from Earth911 using Playwright and OpenAI's GPT-4 for material classification.

---

What It Does

- Scrapes recycling centers for **Electronics** near ZIP code `10001` from [Earth911](https://search.earth911.com/)
- Extracts:
  - Business name
  - Last updated date
  - Street address
  - Material category
  - Materials accepted
- Uses **OpenAI's GPT-4** to classify materials into predefined recycling categories

---

 Files

| File | Description |
|------|-------------|
| `scraper.py` or `scraper.ipynb` | Main scraping + LLM logic |
| `output.json` | Final JSON output with 3 sample entries |
| `requirements.txt` | Python dependencies |
| `README.md` | You are here |

---

 Prompting Strategy

We pass raw "accepted materials" text to GPT-4 with this format:
- Predefined categories and subtypes
- Forced JSON output structure
- GPT classifies into `materials_category` and `materials_accepted`

---

 Tech Stack

- Python
- Playwright (Chromium browser automation)
- OpenAI API (GPT-4)
- nest_asyncio (for notebooks)
- JSON parsing

---

 Edge Cases Handled

- Dynamic iframe-based search interface
- Hidden or missing material fields
- Unknown last-updated dates
- Headless browser issues with full rendering

---

 Setup

```bash
pip install -r requirements.txt
playwright install
