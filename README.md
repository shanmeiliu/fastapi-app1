## How to set up local env using uv

| Task        | Command                          |
| ----------- | -------------------------------- |
| Create venv | `uv venv .venv`                  |
| Activate    | `source .venv/bin/activate`      |
| Install     | `uv pip install fastapi uvicorn` |
| Run app     | `uvicorn main:app --reload`      |


## How to run

Check that your shell is using the correct Python environment:

```
python -m uvicorn main:app --reload
```

This runs Uvicorn via the Python module interface — it bypasses PATH issues.

If that works, it confirms uvicorn is installed, but the binary directory (.venv/bin) isn’t on your PATH.