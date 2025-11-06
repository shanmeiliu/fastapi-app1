


## How to set up local env using uv

| Task        | Command                          |
| ----------- | -------------------------------- |
| Create venv | `uv venv .venv`                  |
| Activate    | `source .venv/bin/activate`      |
| Install     | `uv pip install fastapi uvicorn` |
| Run app     | `uvicorn main:app --reload`      |
 
### Basic usage of uv

```uv venv```: Creates a virtual environment in a directory named ```.venv```. 

```uv venv my-env```: Creates a virtual environment in a directory named ```my-env```. 

```uv venv --python 3.11```: Creates a virtual environment using Python 3.11 (requires the version to be installed on your system or will be downloaded by uv). 

### Using uv run
uv run allows you to execute commands within the project's virtual environment without manually activating it.
It automatically detects and creates the environment if it doesn't exist, installs dependencies from pyproject.toml and uv.lock, and then runs your command.
Example: ```uv run main.py``` to run a script, or ```uv run flask run``` to start a flask server. 

## How to run

Check that your shell is using the correct Python environment:

```
python -m uvicorn main:app --reload
```

This runs Uvicorn via the Python module interface — it bypasses PATH issues.

If that works, it confirms uvicorn is installed, but the binary directory (.venv/bin) isn’t on your PATH.