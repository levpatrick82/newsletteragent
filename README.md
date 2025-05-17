Plugilo Newsletter Agent
This project automates the process of checking websites for newsletter signups, extracting company information, and logging results for analysis. It leverages Google Gemini (free tier) and the browser-use agent to interact with websites, fill out newsletter forms, and scrape legal/company details.
Features
Newsletter Signup Automation:
Visits each provided website, searches for a newsletter signup form, fills it with a specified name and email, and submits the form.
Company Info Extraction:
Scrapes the website (including “impressum”/“imprint” pages) for company name, tax ID, CEO/person in charge, and other legal details.
Metadata Collection:
Extracts the website’s title, logo image URL, and tags/keywords.
Result Logging:
agent_newsletter_results.csv: Main results for each URL (title, logo, tags, impressum info, and newsletter signup result).
company_info.csv: Detailed company information for each site.

failed.csv: URLs where extraction or signup failed, with reasons.
Duplicate Handling:
Skips URLs already processed and present in the results CSV.
Batch Processing:
Supports single URL, multiple URLs, or a CSV file of URLs.
Gemini Free Tier Compliance:
Keeps LLM responses within the free tier token limit.
Requirements
Python 3.10+
browser-use
langchain-google-genai
python-dotenv
Google Gemini API key (set in .env as GOOGLE_API_KEY)
Install dependencies (example):
pip install browser-use langchain-google-genai python-dotenv
Run
Setup
Clone the repository and navigate to the project directory.
Set up your environment:
Setup
Clone the repository and navigate to the project directory.
Set up your environment:
Create a .env file with your Google Gemini API key:
Prepare a CSV file with URLs to process (one per line, header optional).
Usage
Run the agent script:
Apply to python run_gemini_agent.py(Optional) 
You will be prompted to choose an input mode:
1: Enter a single URL
2: Enter multiple URLs (comma or newline separated)
3: Provide a CSV file with URLs
The agent will process each URL, attempt newsletter signup, extract company info, and log results.

