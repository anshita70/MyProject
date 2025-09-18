# Financial Document Analyzer - Debug Assignment

## Project Overview
A comprehensive financial document analysis system that processes corporate reports, financial statements, and investment documents using AI-powered analysis agents.

## Getting Started

### Install Required Libraries
```sh
pip install -r requirement.txt
```

### Sample Document
The system analyzes financial documents like Tesla's Q2 2025 financial update.

**To add Tesla's financial document:**
1. Download the Tesla Q2 2025 update from: https://www.tesla.com/sites/default/files/downloads/TSLA-Q2-2025-Update.pdf
2. Save it as `data/sample.pdf` in the project directory
3. Or upload any financial PDF through the API endpoint

**Note:** Current `data/sample.pdf` is a placeholder - replace with actual Tesla financial document for proper testing.

# You're All Not Set!
🐛 **Debug Mode Activated!** The project has bugs waiting to be squashed - your mission is to fix them and bring it to life.

## Debugging Instructions

1. **Identify the Bug**: Carefully read the code in each file and understand the expected behavior. There is a bug in each line of code. So be careful.
2. **Fix the Bug**: Implement the necessary changes to fix the bug.
3. **Test the Fix**: Run the project and verify that the bug is resolved.
4. **Repeat**: Continue this process until all bugs are fixed.

## Expected Features
- Upload financial documents (PDF format)
- AI-powered financial analysis
- Investment recommendations
- Risk assessment
- Market insights
## Bugs Found & Fixes
Bugs Found & Fixes

| Bug # | Type       | Error Message / Location                                  | Fix Applied |
|-------|------------|-----------------------------------------------------------|-------------|
| 1     | Dependency | `ModuleNotFoundError: No module named 'fastapi'` (main.py, line 1) | Installed FastAPI using `pip install fastapi` and added it to `requirements.txt` |

 2 | Dependency | `ModuleNotFoundError: No module named 'crewai'` (task.py, line 2) | Installed CrewAI using `pip install crewai` and added it to `requirements.txt` |

 3 | Encoding / File Reading | UnicodeDecodeError: 'utf-8' codec can't decode byte 0xff in position 0: invalid start byte | with open("filename.txt", "r", encoding="utf-8", errors="ignore") as f:
    data = f.read() |
    Bug #	Type	Error Message	Fix Applied
4|	Dependency| (corrupted package)	UnicodeDecodeError: 'utf-8' codec can't decode byte 0xff in position 0 (main.py, line 6)	| Reinstalled crewai using pip install --upgrade --force-reinstall crewai. Updated requirements.txt.


5|	Dependency |Missing	ModuleNotFoundError: No module named 'fastapi' (main.py, line 1)	| Installed fastapi, uvicorn, and python-multipart. Updated requirements.txt.


6	Config / Encoding	| UnicodeDecodeError: 'utf-8' codec can't decode byte 0xff in position 0 |  (agents.py, line 4)	.env file was not UTF-8. Recreated .env with correct UTF-8 encoding and proper variables.


7 |	Dependency |	ModuleNotFoundError: No module named 'fastapi' |	Installed FastAPI & uvicorn