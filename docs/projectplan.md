# Project Plan: Wrenchlog – Maintenance App for Motocross

## Project Name

**Wrenchlog** – short, technical, and easy to extend

## Objective

Development of a mobile and offline-capable app for structured documentation of motocross bike maintenance tasks. The app will include PDF exports, JSON backups, and later optional analysis tools. Development begins on a Linux notebook using Flutter & Dart, with eventual porting to Android. Python will be used in parallel for side tasks (e.g., JSON analysis).

---

## Tech Stack

| Component            | Tool/Technology       | Reason                                         |
| -------------------- | --------------------- | ---------------------------------------------- |
| Programming Language | Dart                  | Required for Flutter                           |
| Framework            | Flutter               | Cross-platform, stable, strong UI capabilities |
| IDE                  | VS Code               | Lightweight, extendable                        |
| Version Control      | Git + GitHub          | Open source, collaborative                     |
| Local Database       | Isar DB               | Fast, modern, Flutter-compatible               |
| PDF Export           | `pdf` Flutter package | For maintenance documentation                  |
| Backup/Import        | JSON                  | Readable, easy to process                      |
| Side Tools           | Python                | Analysis scripts and utilities                 |

---

## Project Structure (GitHub)

```plaintext
wrenchlog/
├── lib/
│   ├── models/
│   ├── screens/
│   └── services/
├── assets/
│   └── mx_maintenance.json
├── python/
│   └── analyze_json.py
├── docs/
│   └── projectplan.md
├── README.md
├── LICENSE
└── pubspec.yaml
```

---

## Agile Workflow (Scrum, 1-week sprints)

### Sprint 0 – Setup

**Goal:** Local and online project structure ready

* Create GitHub repo: `wrenchlog`
* Generate local Flutter project structure
* Write README.md with objectives
* Add `.gitignore`
* Install Flutter SDK & VS Code (with plugin)

**Deliverables:**

* GitHub repo with basic structure
* Local Flutter project folder
* README with project overview

---

### Sprint 1 – Import & Display Maintenance Data

**Goal:** Maintenance list visible and interactive in the app

* Convert Excel to JSON
* Load JSON data into app and display as a list
* Add checkboxes + input fields (e.g. current values)
* Tooltips for maintenance hints
* “Complete Maintenance” button with confirmation dialog

**Deliverables:**

* App displays checklist with interaction
* JSON file embedded in project assets

---

### Sprint 2 – Data Persistence & PDF Export

**Goal:** Save user inputs and export them as PDF

* Store inputs locally (Isar or SharedPreferences)
* Generate PDF with `pdf` package
* Include: date, entries, status
* Export PDF to local folder

**Deliverables:**

* Persistent data storage
* Maintenance PDF export

---

### Sprint 3 – Backup/Restore & Python Interface

**Goal:** Backup data as JSON and analyze with Python

* Button to create JSON backup file
* Button to import/restore previous backup
* Python script to analyze JSON data (e.g. statistics, frequency)

**Deliverables:**

* Backup JSON file
* CLI-based analysis tool in Python

---

## MVP (Minimal Viable Product)

| Feature              | Status     |
| -------------------- | ---------- |
| Display maintenance  | 🟡 Planned |
| Input persistence    | 🟡 Planned |
| PDF export           | 🟡 Planned |
| JSON backup/restore  | 🟡 Planned |
| Python analysis tool | 🟡 Planned |

---

## Next Steps (Sprint 0)

1. Create GitHub repo `wrenchlog`
2. Start local Flutter project
3. Create structure as shown above
4. Install Flutter SDK and run `flutter doctor`
5. First commit message: `Initial project setup`

---

## Conclusion

This app solves a real-world problem (maintenance tracking, proof of service, report exports). It is technically feasible, modular, and offers a practical learning platform for the developer and useful tool for the motocross community.

> Goal: Structure over chaos. Small steps. Visible progress.
