# ThreatScope — Python Dependencies
# Install: pip install -r requirements.txt

# ── Core (all built into Python stdlib — no pip install needed for base app) ──
# tkinter   — built-in GUI (comes with Python on Windows/Mac)
# hashlib   — built-in hashing
# json      — built-in JSON
# re        — built-in regex
# ipaddress — built-in IP validation
# threading — built-in concurrency
# struct    — built-in binary parsing

# ── Optional: upgrade to real integrations ────────────────────────────────────
# Uncomment as you hook up real APIs:

# python-whois          # Real WHOIS lookups:     pip install python-whois
# dnspython             # Real DNS queries:        pip install dnspython
# requests              # HTTP API calls:          pip install requests
# yara-python           # Real YARA scanning:      pip install yara-python
# oletools              # Office macro analysis:   pip install oletools
# pefile                # Deep PE analysis:        pip install pefile

# ── To build a .exe ───────────────────────────────────────────────────────────
# pip install pyinstaller
# pyinstaller --onefile --windowed --name ThreatScope app.py
