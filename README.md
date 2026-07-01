# PI Capacity Calculator

A lightweight, browser-based **Program Increment (PI) Capacity Planning Calculator** designed for SAFe Scrum teams.

# Live Demo -> https://dhruvmts-wq.github.io/pi-capacity-planner/

The calculator helps Agile teams estimate realistic delivery capacity by considering:

- Team composition
- Meeting overhead
- Individual availability
- Public holidays
- Personal time off (PTO)
- IP Iteration focus
- Story Point capacity
- Work Type allocation

Everything runs entirely in the browser—no backend, no database, and no data leaves your machine.

---

## Features

### Team Management

- Add or remove team members
- Rename members inline
- Support for:
  - Developers (Dev)
  - DIT members
- Experience presets
  - Junior
  - Mid
  - Senior
- Adjustable availability percentage for each member
- Automatic meeting overhead calculation

---

### PI & Iteration Planning

Configure:

- 5 delivery iterations
- 1 Innovation & Planning (IP) iteration

For every iteration you can configure:

- Start date
- End date
- Automatic working day calculation
- IP focus percentage (for IP iteration)

Working days automatically exclude:

- Weekends
- Organization holidays

---

### Holiday & PTO Management

Supports two levels of leave management.

#### Organization Holidays

Applies to the entire team.

Examples:

- National holidays
- Company shutdowns
- Festival holidays

#### Individual PTO

Track vacation days for every team member in every iteration.

---

### Capacity Calculation

Capacity is calculated automatically using:

```
Available Days
      ↓
Available Hours
      ↓
Story Points
```

Formula:

```
Available Days
    = Working Days
    - Organization Holidays
    - PTO

Effective Hours
    = Available Days
      × 8 hours
      × Availability %

Story Points
    = Effective Hours ÷ 8
```

---

### Work Type Allocation

Allocate PI capacity across multiple work types.

Examples:

- Features
- RTR
- Technical Debt
- TCoO
- Defects
- Production Support
- Innovation

Features include:

- Unlimited work types
- Editable names
- Editable percentages
- Manual Story Point override
- Validation ensuring total allocation equals 100%

---

### Summary Dashboard

Automatically generates:

- Total PI Story Points
- Capacity excluding IP iteration
- Effective delivery hours
- Team composition
- Per-iteration capacity
- Per-member capacity
- PI totals

---

### Export & Import

#### Export JSON

Save the complete planning configuration.

Includes:

- Team members
- PTO
- Holidays
- Iteration dates
- Work type allocation

#### Import JSON

Reload previously saved planning sessions.

---

### PDF Report

Generate a professional PDF containing:

- PI Summary
- Capacity metrics
- Work type allocation
- Iteration breakdown
- Team member capacity table

Ideal for:

- PI Planning
- Sprint Planning
- Leadership reviews
- Capacity discussions

---

## Technology Stack

- HTML5
- CSS3
- Vanilla JavaScript

Libraries:

- jsPDF
- jsPDF AutoTable

No frameworks are required.

---

## Getting Started

Clone the repository.

```bash
git clone https://github.com/<your-username>/pi-capacity-calculator.git
```

Navigate into the project.

```bash
cd pi-capacity-calculator
```

Open the application.

```text
index.html
```

Or simply double-click `index.html` in your browser.

No installation or build process is required.

---

## Recommended Workflow

1. Configure your team.
2. Set PI iteration dates.
3. Add organization holidays.
4. Enter individual PTO.
5. Review the calculated capacity.
6. Allocate Story Points across work types.
7. Export the PDF for PI Planning.

---

## Assumptions

The calculator currently assumes:

- 8-hour workday
- 1 Story Point = 8 hours
- Monday–Friday working week
- Availability percentage represents delivery time after meetings and ceremonies

---

## Data Privacy

This application is completely client-side.

- No server
- No database
- No tracking
- No analytics
- No internet connection required after opening the page

All calculations happen locally in your browser.

---

## Future Enhancements

Potential improvements include:

- Multiple team support
- Velocity history
- Burnup projections
- Capacity trend charts
- Dark/light theme toggle
- Custom work calendars
- Localization
- Azure DevOps / Jira integration
- CSV export
- Multi-PI planning

---

## License
This project is provided as-is for educational and planning purposes.

Feel free to fork, modify, and adapt it for your team's needs.
