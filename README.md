# securechain

A blockchain-based chain of custody system for digital evidence. Files are fingerprinted using SHA-256 and logged to a tamper-proof chain — any modification to a logged file, or to the chain itself, is immediately detectable.

Built as a lightweight simulation of forensic evidence authentication workflows used in legal and investigative environments.

---

## How It Works

- Each file is hashed using SHA-256
- The hash is stored in a block alongside a submitter name and timestamp
- Each block links to the previous block's hash, forming a chain
- Any tampering — to a file or to the chain — breaks the link and gets flagged

---

## Usage

```bash
python main.py add       # Log a new file
python main.py verify    # Verify a file's integrity
python main.py view      # View the full evidence log
```

---

## Project Structure

```
securechain/
├── main.py           # Entry point and CLI
├── ledger.py         # Block and Chain logic
├── fingerprint.py    # SHA-256 file hashing
└── README.md
```

---

## Tech Stack

Python — `hashlib`, `json`, `datetime`, `os` (all built-in, no installs required)
