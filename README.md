## How to run

Check that your shell is using the correct Python environment:

```
python -m uvicorn main:app --reload
```

This runs Uvicorn via the Python module interface — it bypasses PATH issues.

If that works, it confirms uvicorn is installed, but the binary directory (.venv/bin) isn’t on your PATH.