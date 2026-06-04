# HVAC Expansion Project — Command Dashboard

A self-contained, zero-dependency project tracking dashboard for a multi-year HVAC expansion project. Single HTML file — no build tools, no npm, no server required.

---

## 🚀 Quick Start

### Option A — Open locally
```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/hvac-dashboard.git
cd hvac-dashboard

# Open directly in any browser — no server needed
open index.html          # macOS
start index.html         # Windows
xdg-open index.html      # Linux
```

### Option B — GitHub Pages (recommended)
1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set **Source** to `Deploy from a branch` → `main` → `/ (root)`
4. Click **Save** — your dashboard will be live at:
   `https://YOUR_USERNAME.github.io/hvac-dashboard/`

---

## 📁 File Structure

```
hvac-dashboard/
└── index.html      ← entire dashboard (HTML + CSS + JS, self-contained)
└── README.md       ← this file
```

No external files, CDNs, or dependencies. Everything is embedded.

---

## 🗂 Dashboard Sections

| Section | Description |
|---|---|
| **Phase Banner** | Current phase, start/end dates, duration |
| **Stat Cards** | Live countdown, progress %, risks, budget at a glance |
| **Master Timeline** | Phase bars with progress + circular completion rings |
| **Key Milestones** | 18 milestones with status badges |
| **Scope Areas** | 8 work packages with individual progress bars |
| **Risk Register** | Colour-coded risk ratings (High / Med / Low) |
| **Budget Tracker** | Allocated vs spent per category |
| **Project Team** | 7 roles with organisation labels |
| **Activity Log** | Scrollable chronological log entries |

---

## ✏️ How to Update the Dashboard

All data is plain HTML — no database, no CMS. Open `index.html` in any text editor (VS Code, Notepad++, etc.) and edit the relevant section.

### Update overall progress %
Search for `stat-value blue` and change the number.

### Change a milestone status
Find the milestone row and change the CSS class on `ms-status`:
```html
<!-- Options: completed | in-progress | upcoming | at-risk -->
<span class="ms-status completed">Completed</span>
```

### Update a scope area %
Find the scope item by name and update both the percentage text and bar width:
```html
<span class="scope-pct" style="color:var(--accent)">45%</span>
...
<div class="scope-bar-fill" style="width:45%;background:var(--accent)"></div>
```

### Add a risk
Copy an existing `.risk-row` block and paste it inside `.risk-list`. Set the dot colour and badge class (`high` / `medium` / `low`).

### Add a log entry
Copy an existing `.log-entry` and paste it at the top of `.log-body`. Update the date, tag class (`design` / `admin` / `scope` / `risk`), and message.
> 💡 **Tip:** Double-clicking the log panel creates a live editable entry.

### Update budget numbers
Find the `.budget-row` for the category and update both the dollar amounts and `width` of `.budget-spark-fill` (as a % of allocated).

### Change the Phase 2 countdown target date
Find this line in the `<script>` block:
```js
const target = new Date('2026-04-01');
```
Change the date string to your target.

---

## 🎨 Customisation

All colours are CSS variables at the top of the `<style>` block:
```css
:root {
  --accent:  #00c2ff;   /* Primary blue */
  --amber:   #f5a623;   /* Warnings / budget */
  --green:   #22d98f;   /* Completed / low risk */
  --red:     #ff4d6d;   /* High risk / overdue */
}
```
Change any value to rebrand the dashboard.

---

## ✅ Browser Compatibility

Works in all modern browsers — Chrome, Firefox, Safari, Edge. No polyfills needed.

---

## 📄 Licence

Internal use only. Not for public distribution.
