# Website Analyzer MCP

## Features

- Extracts visible text and metadata from webpages using Playwright
- Analyzes website content using Gemini and Claude APIs
- Identifies business information such as:
  - Target audience (aka target buyers/consumers)
  - Main features/products
  - Unique value proposition
  - Industries served
  - Company size
- Provides structured output for integration with other systems

## Requirements

- Python 3.8+
- Playwright
- httpx
- dotenv

## Usage

```python
import asyncio
from website_analyzer import analyze_website_with_browser

async def main():
    url = "https://example.com"
    result = await analyze_website_with_browser(url)
    print(result)

asyncio.run(main())
```

## Output Format

The analyzer returns a dictionary with the following structure:

```json
{
  "title": "Website Title",
  "description": "Website Description",
  "headings": ["Heading 1", "Heading 2", ...],
  "target_audience": "Description of target audience",
  "main_features": ["Feature 1", "Feature 2", ...],
  "unique_value": "Description of unique value proposition",
  "industries": ["Industry 1", "Industry 2", ...],
  "company_size": "Description of company size",
  "raw_text": "Sample of raw text from the website"
}
```

This tool is part of the Network AI system for business profile analysis and event recommendations.
