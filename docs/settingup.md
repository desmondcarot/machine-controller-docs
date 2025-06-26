# Setting up the project

## Prerequisites

Before you begin, ensure the following tools are installed:

- **Python 3.10+** — Main development language  
- **Visual Studio Code (VSCode)** — Recommended IDE  
- **Virtual Environment** — Optional but recommended for dependency isolation

---

## Installation & Running the Project

### Standard Setup

1. Navigate to the root of the project:
    ```bash title="bash"
    cd path/to/project
    ```

2. Install dependencies using `pip`:
    ```bash title="bash"
    pip install -r requirements.txt
    ```

3. Run the application:
    ```bash title="bash"
    python main.py
    ```

### Optional: Using `uv` and Virtual Environment

This is a cleaner way to manage dependencies using [`uv`](https://github.com/astral-sh/uv), a fast Python package manager.

1. Navigate to the project folder:
    ```bash title="bash"
    cd path/to/project
    ```

2. Install `uv`:
    ```bash title="bash"
    pip install uv
    ```

3. Create a virtual environment:
    ```bash title="bash"
    uv venv
    ```

4. Activate the virtual environment:

    - **Windows**:
      ```bash title="bash"
      .venv\Scripts\activate
      ```

    - **macOS/Linux**:
      ```bash title="bash"
      source .venv/bin/activate
      ```

    > ⚠️ If the `uv` or `pip` command is not found, make sure the Python `Scripts/` folder is added to your system PATH environment variable.

5. Install dependencies:
    ```bash title="bash"
    uv pip install -r requirements.txt
    ```

6. Run the app:
    ```bash title="bash"
    python main.py
    ```

7. You should see FastAPI running on `http://localhost:8000`

