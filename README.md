# Forensic Analysis of WhatsApp Web

This project showcases a forensic investigation of WhatsApp Web sessions using browser-based artifacts. The work focuses on identifying and analyzing persistent digital traces (e.g., UUID, SessionID, timestamps) and evaluates risks like session hijacking.

## Research Objective

The research answers these key questions:
- Do session tokens persist in the browser after logout?
- Can stored session data be reused to hijack a WhatsApp Web session?
- What artifacts remain even after cache clearing?
- How secure is the backup and synchronization system?

## Tools Used

- FTK Imager
- DB Browser for SQLite
- SQLite Spy
- MZCacheView
- Wireshark
- Firefox Storage Inspector

## Key Findings

| Artifact        | Persists After Logout | Cache Clear | Security Risk |
|----------------|-----------------------|-------------|----------------|
| UUID           | ✅                    | ❌          | Low           |
| Profile Picture| ✅                    | ❌          | Medium        |
| Timestamp      | ✅                    | ❌          | Low           |
| SessionID      | ❌                    | ❌          | High          |
| Backup Fragments | ✅                  | ✅          | High          |

## Screenshots

Included in `/screenshots/`:
- UUID trace from IndexedDB
- Profile picture cache file
- SessionID in local storage
- IP address from Wireshark capture

## Research Paper

The full paper: [`Research Paper.pdf`](./Research Paper.pdf)

## Author

**Prakriti Negi**  

---

> This repository is intended for academic and educational purposes only. No real user data was used in any part of this study.
