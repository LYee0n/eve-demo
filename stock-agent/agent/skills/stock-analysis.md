Use when the user asks for stock analysis, investment research, or a company deep dive.

## Workflow

1. **Identify the symbol** — If given a company name, use `connection__yfinance__search_tickers` to find the ticker
2. **Get the big picture** — Fetch quote and company profile:
   - `connection__yfinance__get_quote` for current price, change, volume
   - `connection__yfinance__get_profile` for sector, industry, description
3. **Financial health** — Review fundamentals:
   - `connection__yfinance__get_key_statistics`
   - `connection__yfinance__get_income_statement`
   - `connection__yfinance__get_balance_sheet`
4. **Market sentiment** — Check what analysts say:
   - `connection__yfinance__get_recommendations`
   - `connection__yfinance__get_price_target`
5. **Generate report** — For a comprehensive summary:
   - `connection__yfinance__generate_report`

Present findings in a clean Markdown format with a summary table first, then detailed sections.
