# Vulnerability Assessment Lab

A walkthrough of how I run vulnerability scans, tell real findings apart from scanner noise, score and prioritize what's left, and turn that into a report someone can actually act on. Built as a single self-contained web page, no backend or build step required.

**[▶ Live demo](https://raheemmohd.github.io/vuln-assessment-portfolio-project/)**

![status](https://img.shields.io/badge/status-complete-brightgreen) ![type](https://img.shields.io/badge/type-portfolio%20project-blue) ![stack](https://img.shields.io/badge/stack-HTML%2FCSS%2FJS-informational)

---

## Why I built this

This is the fourth piece of the same practice environment — SOC, threat intel, red team, and now vulnerability management. A scanner's raw output is just a list of possibilities; the actual skill is validating which findings are real, scoring and prioritizing them properly, and knowing when the scanner is wrong. I wanted to show both sides of that with real evidence: a critical finding I traced all the way to a confirmed exploit path, and a scanner-flagged "critical" I manually disproved before it ever reached a report.

The critical case study here — an unpatched SMB vulnerability on a Windows host — is the same target I later exploited in my Red Team Lab project. Seeing it from the scanning side first, before the exploitation side, is really the point of running vulnerability management at all.

## What's inside

| Section | What it covers |
|---|---|
| Assessment workflow | Asset discovery → scanning → validation → CVSS scoring → prioritization → remediation → rescan |
| Tools & sample scans | Nessus vs. OpenVAS compared, real scan configs, an NVD API query |
| Reading CVSS scores | Decoding an actual CVSS vector string metric by metric |
| Risk prioritization model | A formula (CVSS × exposure × asset criticality) with a worked example |
| Case study 1 | MS17-010/EternalBlue — from a Nessus flag to a confirmed, prioritized, remediated finding |
| Case study 2 | A scanner-flagged "critical" Apache CVE I manually disproved before it reached the report |
| Reporting & remediation tracking | What actually goes in my report, and how I track a finding to verified closure |
| **Live demo — scan results queue** | 5 raw findings; view scan detail, then classify each one |
| Metrics that matter | Scan coverage, time to remediate, false positive rate, recurring vuln rate |
| Where vuln management is heading | Continuous exposure management, risk-based prioritization, attack path validation, AI-assisted patching |

## Skills demonstrated

`Nessus` · `OpenVAS` · `CVE/CVSS analysis` · `Vulnerability validation` · `Risk-based prioritization` · `Authenticated scanning` · `Remediation tracking` · `Security report writing`

## Tech stack & approach

Pure HTML, CSS, and vanilla JavaScript — no frameworks, no dependencies, no build tooling, same as my other projects. All diagrams are hand-built inline SVG, and the scan-results queue is a small state machine in plain JS.

## Running it locally

```bash
git clone https://github.com/raheemmohd/vuln-assessment-portfolio-project.git
cd vuln-assessment-portfolio-project
open index.html
```

## A note on the data

All scan results, hosts, and findings shown are from my own practice lab, not a real client engagement.

## License

MIT

## Author

Mohammed Abdul Raheem
