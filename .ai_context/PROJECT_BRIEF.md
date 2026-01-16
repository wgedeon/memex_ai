# PROJECT_BRIEF: [Project Name]

## 1. Mission
**[What is the core purpose of this project in one sentence?]**
> Example: *Build a personal dashboard for visualizing and analyzing daily habit completion, focusing on private, long-term trend analysis.*

## 2. Core Principles (Non-Negotiables)
- **Must:** [Key technical or philosophical requirement]
- **Must:** [Another critical constraint]
- **Must Not:** [A deal-breaking behavior or technology to avoid]
> Example:
> - **Must:** Store all data locally in a single file; no backend server or user accounts.
> - **Must:** Use only static charts (SVG/Canvas); no heavy visualization libraries.
> - **Must Not:** Send any data to external services; all processing must happen client-side.

## 3. Scope & Boundaries
**In Scope for V1:**
- [User Story 1: e.g., "Manually log a habit as 'done' for a specific date."]
- [User Story 2: e.g., "View a calendar heatmap of my consistency for one habit over the last 90 days."]
- [User Story 3: e.g., "Export my entire dataset as a JSON file for backup."]

**Explicitly Out of Scope (Save for Later):**
- [e.g., Mobile apps, push notifications, or social features]
- [e.g., Automated habit tracking via phone sensors or integrations]

## 4. High-Level Architecture
**Components:**
- `[./data/]`: JSON file - Central data store for all habit entries.
- `[./src/]`: Vanilla JS + HTML - Core application logic and static UI.
- `[./lib/]`: Lightweight charting library (e.g., Frappe Charts) - For generating visualizations.

**Key Technical Decisions:**
- Decision: Use a browser's LocalStorage as a cache, with a primary JSON file for full data.
- Reason: Enables offline use and simple, user-controlled data portability.