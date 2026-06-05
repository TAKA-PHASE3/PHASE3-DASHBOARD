# HVAC Expansion Project — Command Dashboard v2.0

Self-contained, zero-dependency project dashboard. One HTML file. No build tools, no npm, no server.  
All edits are saved automatically to your browser's local storage — they survive page refreshes.

---

## 🚀 Deploy to GitHub Pages

```bash
git clone https://github.com/YOUR_USERNAME/hvac-dashboard.git
cd hvac-dashboard
# replace index.html with the one you downloaded
git add index.html README.md
git commit -m "Add HVAC dashboard"
git push origin main
```

Then go to **Settings → Pages → Source: main / root → Save**.  
Your live URL: `https://YOUR_USERNAME.github.io/hvac-dashboard/`

---

## ✏️ How to Edit the Dashboard (No Code Needed)

### Step 1 — Enable Edit Mode
Click the **EDIT MODE** button in the top-right corner.  
A blue toolbar appears. The button glows blue.

### Step 2 — Edit any field
- **Click any text** → it becomes editable. Type your change and press **Enter** or click away. Saved instantly.
- **Progress bars** → use the **−** and **+** buttons that appear beside each bar.
- **Status badges** (Upcoming / In Progress / At Risk / Completed) → **click the badge** to cycle to the next status.
- **Risk levels** (LOW / MED / HIGH) → **click the level badge** to cycle.
- **Log tags** (DESIGN / ADMIN / SCOPE / RISK) → **click the tag** to cycle.

### Step 3 — Add new rows
Use the **+ buttons** in the toolbar, or the **+ Add …** buttons that appear at the bottom of each panel.  
A form pops up — fill it in and click **Add**.

### Step 4 — Delete rows
In Edit Mode, a **×** button appears on every row. Click it to delete (with confirmation).

### Step 5 — Exit Edit Mode
Click **EDIT MODE** again to return to clean view mode.

---

## 💾 Backup & Restore

| Action | How |
|---|---|
| **Export** | Edit Mode → toolbar → **⬇ Export JSON** — downloads `hvac-dashboard-backup.json` |
| **Import** | Edit Mode → toolbar → **⬆ Import JSON** — restores from a backup file |
| **Reset** | Edit Mode → toolbar → **↺ Reset to Default** — clears all changes |

> **Important:** Data is stored in *your browser* on *your device*. If you clear browser data or open on a different device, use Export/Import to transfer your data.

---

## 📋 What's in the Dashboard

| Panel | Editable |
|---|---|
| Phase Banner — title, description, dates | ✓ All text fields |
| 6 Stat Cards — progress, actions, budget | ✓ All values |
| Master Timeline — 4 phase bars | ✓ Progress % via +/− |
| Completion Rings (4 metrics) | ✓ Progress % via +/− |
| Key Milestones | ✓ Name, date, status badge; add/delete rows |
| Scope Areas (work packages) | ✓ Name, progress bar, notes; add/delete |
| Risk Register | ✓ Description, impact, level badge; add/delete |
| Budget Tracker | ✓ Category, allocated, spent, usage %; add/delete |
| Project Team | ✓ Name, role, organisation; add/delete |
| Activity Log | ✓ Date, tag, message; add/delete |

---

## 🌐 Browser Support

All modern browsers — Chrome, Firefox, Safari, Edge. No extensions needed.

---

## 📄 Licence

Internal use only. Not for public distribution.
