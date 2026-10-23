# Phishing URL Detector

## Project description
A beginner-friendly cybersecurity awareness project that checks a URL for common warning signs associated with phishing. It uses transparent rule-based checks and produces a warning score with explanations.

**Important:** This is an educational prototype, not a production security tool. “No obvious warning signs detected” does not mean a website is safe.

## Features
- Checks for IP-address hostnames
- Checks for an `@` symbol in the URL
- Flags unusually long URLs
- Checks whether HTTPS is absent
- Looks for common account-related lure words
- Flags hostnames with many dot-separated parts
- Recognizes a small list of URL shorteners
- Explains which rules were triggered

## Technologies used
- Python 3
- Jupyter Notebook
- Python standard library: `urllib.parse`, `ipaddress`

## Files
- `GayathriTS_PhishingURLDetector.ipynb` — complete project notebook
- `requirements.txt` — notebook environment dependencies
- `GayathriTS_ProjectReport.docx` — project report

## Dataset
This version does **not** use a dataset or machine learning. It is a rule-based prototype, so no dataset is required. This choice keeps the project simple, transparent, and runnable for beginners.

For future research, the UCI Machine Learning Repository has a Phishing Websites dataset page:
https://archive.ics.uci.edu/dataset/327/phishing+websites

The dataset is not used by the current code. Do not describe this prototype as a trained ML model.

## Setup and run
1. Install Python 3 from https://www.python.org/downloads/
2. Open Command Prompt / Terminal in the project folder.
3. Optional: create and activate a virtual environment.
4. Install the notebook tools:

   ```bash
   python -m pip install -r requirements.txt
   ```

5. Start Jupyter:

   ```bash
   jupyter notebook
   ```

6. Open `GayathriTS_PhishingURLDetector.ipynb` and run the cells from top to bottom.
7. In the final input cell, enter a URL to inspect. Do not open suspicious links.

## How the score works
Each triggered rule adds a small number of points. A score of 3 or more is labelled **Potentially Suspicious**. This threshold is only a simple demonstration rule and has not been validated on a real-world test set.

## Limitations and safety
- False positives and false negatives are possible.
- It does not contact the URL or verify a website in real time.
- It does not establish that a website is safe or malicious.
- Do not enter private, personal, or confidential URLs into tools you do not trust.
- Use the result as an awareness aid, not as the only basis for a security decision.

## Author
Gayathri TS

## Suggested GitHub repository name
`phishing-url-detector`
