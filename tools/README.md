# Tools

Deterministic functions and scripts that the agent can execute.

## Purpose

Store reusable scripts and utilities that perform specific operations:
- Data processing scripts
- Automation utilities
- Integration helpers
- Custom commands

## Structure

```
tools/
├── scripts/          # Executable scripts
│   ├── analyze.py
│   └── process.sh
├── templates/        # Code templates
└── utils/            # Utility functions
```

## Creating Tools

### Python Scripts

```python
#!/usr/bin/env python3
"""Tool description.

Usage: python tools/scripts/my-tool.py [args]
"""

import sys

def main():
    # Tool logic here
    pass

if __name__ == "__main__":
    main()
```

### Shell Scripts

```bash
#!/bin/bash
# Tool description
# Usage: bash tools/scripts/my-tool.sh [args]

set -e
# Script logic here
```

## Using Tools

The agent executes tools via the `bash` command:

```
bash("python tools/scripts/analyze.py data.csv", "Analyzing data")
```

## Tips

- Include usage instructions in script headers
- Handle errors gracefully with clear messages
- Use environment variables for configuration
- Keep scripts focused on one task
