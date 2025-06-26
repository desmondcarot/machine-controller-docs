# Welcome To Machine Controller
Machine Controller is a backend system designed to control and manage multiple machines asynchronously using image recognition. It leverages OpenCV's template matching to execute task flows, and provides a web interface for real-time interaction and control.

---

## Tech Stack

- **Backend:** FastAPI (REST API + frontend server)
- **Image Recognition:** OpenCV (template matching)
- **Frontend:** HTML/CSS/JS served via FastAPI
- **Concurrency:** Python `asyncio`

---

## Features

- Add or remove machines
- List all registered machines
- Start/stop asynchronous task loops
- Perform manual control operations
- Visual feedback via camera and image processing

---

## Control Interface

Available via **Web UI** or **REST API**:

| Function            | Description                                         |
|---------------------|-----------------------------------------------------|
| *Add Machine*       | Register a new machine with its configuration       |
| *List Machine*      | View all machines in the system                     |
| *Start Task Loop*   | Begin automated task execution                      |
| *Stop Task Loop*    | Stop the current task execution loop                |
| *Manual Control*    | Direct control over machine movement/actions        |

---

## Directory Overview
```text
project-root/
├── logs/                          # Logging output folder (runtime)
├── MachineController/             # Core logic
│   ├── __init__.py                # Module initialization
│   ├── camera_repo/               # Camera device connection & logic
│   ├── classes.py                 # Supplementary classes
│   ├── device_action/             # Device-specific action handlers
│   ├── globals.py                 # Global variables and constants
│   ├── logger_config.py           # Logging setup and formatting
│   ├── machine_controller.py      # Controls multiple machines, exposes methods to FastAPI
│   ├── machine.py                 # Task loop logic for each machine
│   ├── serial_connection.py       # Serial communication and camera handling
│   └── utils.py                   # Helper functions
├── web/                           # Frontend assets (HTML/CSS/JS)
├── config.json                    # Global configuration file
├── main.py                        # FastAPI app entry point
└── requirements.txt               # Python dependencies

```

---
# Thanks!

<div style="padding: 1em; background: #f9f9f9; border: 1px solid #ddd; margin-top:40px">
  <h2 style="color: teal;">🚀 Custom HTML Section</h2>
  <p>You can embed <strong>HTML</strong> directly into your Markdown files in MkDocs.</p>
  <a href="getting-started/" style="color: blue;">Start Here →</a>
</div>