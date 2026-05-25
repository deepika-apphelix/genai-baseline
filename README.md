# genai-baseline

A small FastAPI application with a `/health` endpoint and a pytest test case.

## Prerequisites

- Python 3.12 or newer
- PowerShell

## Set Up the Project

From the project root:

```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install fastapi uvicorn pytest httpx
```

## Run the Application

Start the FastAPI server with Uvicorn:

```powershell
uvicorn main:app --reload
```

The app will run at:

```text
http://127.0.0.1:8000
```

## Check the Health Endpoint

Open this URL in a browser:

```text
http://127.0.0.1:8000/health
```

Or call it from PowerShell:

```powershell
Invoke-RestMethod http://127.0.0.1:8000/health
```

Expected response:

```json
{
  "status": "ok"
}
```

## Run the Test Case

With the virtual environment activated, run:

```powershell
pytest
```

The test in `test_main.py` verifies that `/health` returns HTTP `200` and:

```json
{
  "status": "ok"
}
```
