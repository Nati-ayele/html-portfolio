# Student Finance Tracker

A **web-based application** for students to track their expenses, manage budgets, and analyze spending trends. Built with HTML, CSS, and JavaScript, featuring modular architecture, validation, and accessibility-focused design.

---

## 🎯 Chosen Theme
**Student Finance Tracker** – Manage personal budgets, add transactions, track spending, and visualize trends.  

**Note:** This app focuses on financial tracking for students, including budget limits, category analysis, and currency conversions.

---

## ⚡ Features
- Add, edit, and delete transactions.
- Sort transactions by **Description, Amount, Category, or Date**.
- Regex-based search with **case toggle** and accessible highlighting.
- Track total transactions, total spent, top category, and weekly trends.
- Manage **budget caps** with alerts when exceeding limit.
- **Currency conversion** between USD, EUR, and RWF.
- Import and export transactions as JSON.
- Modular code structure (`validators.js`, `ui.js`, `state.js`, `storage.js`, `search.js`).
- Fully responsive and accessible design with keyboard navigation.

---

## 🧩 Regex Catalog

| Field       | Regex Rule | Regex Expression | Example (Valid) | Example (Invalid) |
|------------|--------------|----------------|-----------------|
| Description | No leading/trailing spaces, no duplicate words | /^\S(?:.*\S)?$/ |`"Morning coffee"` | `" Coffee"` or `"coffee coffee"` |
| Amount      | Number, max 2 decimals | |`"25"`, `"25.50"` | `"25.555"`, `"abc"` |
| Date        | `YYYY-MM-DD` format, not future | /^\d{4}-(0[1-9]|1[0-2])-(0[1-9]|[12]\d|3[01])$/ |`"2025-06-01"` | `"01-06-2025"`, `"2026-12-01"` |
| Category    | Letters, spaces, hyphens only | /^[A-Za-z]+(?:[ -][A-Za-z]+)*$/ |`"Food-Dining"` | `"Food123"` |
| Duplicate Words    | case sensitive duplicate checking| /\b(\w+)\b\s+\b\1\b/ |`"books books" matches` | `"Books books" passes` |


**Search:** Regex patterns can be entered in the search box. Use the checkbox to toggle **case-insensitive** searches. Matches are highlighted in the table.

---

## ⌨️ Keyboard Map
| Key / Shortcut | Action |
|----------------|--------|
| `Tab`          | Navigate through form inputs, buttons, and links |
| `Shift + Tab`  | Navigate backward |
| `Enter`        | Activate focused button, link, or sort arrow (sorts the table by that column) |
| Skip link (`Skip to main content`) | Focus jumps directly to the main content |
| Arrow keys| Navigate up and down in the web page using tab + Enter (sorting only) |
| `Space`| Activate buttons (e.g., Save Transaction, Export/Import)  |

---

## ♿ Accessibility Notes
- All interactive elements have proper `aria-labels` and roles.
- Error messages and status updates use `aria-live="polite"` for screen readers.
- Skip links enable bypassing navigation to reach main content directly.
- Focus styles on inputs, buttons, and links are clearly visible.
- Color contrast passes WCAG AA standards.
- Semantic HTML structure with proper headings hierarchy (`<h1>` → `<h2>` → `<h3>`).

---

## 🧪 Running Tests
Validation tests are included to ensure form inputs meet the required criteria.

1. Open `tests.html` in a browser.
2. Results will be displayed under the **Form validation Tests** heading.
3. Each test prints **PASSED** or **FAILED** for:
   - Description validation
   - Amount validation
   - Date validation
   - Category validation
   - Full transaction object validation

---

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/NatnaelAyele/student-finance-tracker.git
2. Open index.html in a browser.
3. Navigate through sections via navigation bar or skip link.
4. Add, edit, sort, search, and export/import transactions.
5. Monitor console for debugging (no errors expected).



📂 File Structure
/
├─ index.html
├─ styles/
│  └─ main.css
├─ scripts/
│  ├─ validators.js
│  ├─ ui.js
│  ├─ state.js
│  ├─ storage.js
│  ├─ search.js
│  └─ tests.js
├─ tests.html
├─ README.md
└─ seed.json

Author

Natnael Ayele – © 2026
GitHub: NatnaelAyele
email: n.eticha@alustudent.com

