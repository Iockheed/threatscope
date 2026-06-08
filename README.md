# ThreatScope
Internal Threat Intelligence Triage Tool

ThreatScope is a self contained SOC triage application for analyzing URLs IPs file hashes and uploaded files

It runs as a standalone Windows executable with optional Python source for development

No external API keys are required for base functionality  
No data leaves the system unless you enable integrations

---

# Quick Start Windows

- Download the release zip
- Extract it
- Run ThreatScope.exe

That is it

Open the app
Paste an artifact
Click scan

Supported inputs
- URL or domain
- IP address
- File hash
- File upload optional

---

# What it does

ThreatScope performs local threat intelligence style analysis and returns a structured result

## URL and domain analysis
- WHOIS age checks
- Pattern detection
- Reputation signals

## IP analysis
- GeoIP lookup
- ASN data
- Abuse reputation checks
- Optional threat intel enrichment

## File analysis
- MD5 SHA256 hashing
- PE structure inspection
- String extraction
- YARA style matching if enabled

## Hash lookup
- Local and external intelligence correlation

---

# Output

Each scan produces a structured JSON report designed for SIEM or SOAR pipelines

```json
{
  "artifact": "",
  "verdict": "MALICIOUS | SUSPICIOUS | BENIGN | WHITELISTED",
  "risk_score": 0,
  "action_item": "ISOLATE_HOST | BLOCK_IP | MANUAL_REVIEW | NO_ACTION",
  "summary": {
    "static_analysis": {},
    "dynamic_analysis": {},
    "threat_intel": {},
    "network": {}
  }
}
