# Atlassian Implementation & License Estimator

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![Tech](https://img.shields.io/badge/tech-HTML%20%7C%20CSS%20%7C%20JS-orange)
![Style](https://img.shields.io/badge/style-Atlassian%20Design%20System-0052CC)

A powerful, single-file estimation tool designed for **Atlassian Solution Partners** and **Certified Experts**. This calculator helps generate professional scope-of-work (SOW) estimations, plan license costs, and export client-ready PDF documents.

Built with the **Atlassian Design System** (ADS) visual style for a native look and feel.

## Features

- **Comprehensive Project Phases:** Structured estimation across four key phases:
  - **A.** Administrative & Contractual Onboarding
  - **B.** Technical Onboarding (Jira, JSM, Confluence, Assets, Integrations)
  - **C.** Operational Onboarding (UAT, Training, Go-Live)
  - **D.** Post-Onboarding Support
- **Dynamic Calculations:**
  - Toggle specific sections on/off to match the scope.
  - Adjust hours per task.
  - Define hourly rates.
  - **Service Cost Toggle:** Hide financial data for services (show only hours) if needed.
- **License Planning:**
  - Add specific products (Jira, JSM, JPD, Guard, etc.).
  - Calculate per-seat costs.
  - Auto-sum total license TCO (Seats & Cost).
- **Data Persistence:**
  - **Auto-save:** All inputs (including customer name, comments, and rates) are saved to `localStorage` instantly.
  - **JSON Import/Export:** Save your estimates as `.json` files to backup or share with colleagues.
- **Professional Output:**
  - **PDF Export:** Optimized print CSS removes UI elements (buttons, toggles, phase headers) and formats the estimation as a clean document.
  - **Dark/Light Mode:** Toggle between themes to match your preference.

## How to Run

This is a **client-side only** application contained in a single HTML file. No server, Node.js, or build process is required.

1. Download the `onboarding-estimation-form.html` file.
2. Open it in any modern web browser (Chrome, Firefox, Safari, Edge).
3. Start estimating!

## Usage Guide

### 1. Estimating Services

- Enter the **Customer Name** at the top.
- Scroll through the sections (Phases A-D). Use the **Toggle Switch** on the top right of each card to include or exclude a module.
- Uncheck specific tasks within a module if they are out of scope (they will appear crossed out).
- Adjust the **Estimated Hours** input at the bottom of each card.

### 2. License Planning

- Scroll to the **License Planning** section.
- Click **+ Add Team** to add a row.
- Select the product, enter the team name, quantity, and price per unit.
- The totals (Seats and Costs) will update automatically in the summary box.

### 3. Summary & Export

- The **Right Sidebar** stays sticky as you scroll.
- Set your **Hourly Rate**.
- Toggle **Include Services Cost** if you want to show/hide the monetary value of the service hours.
- **Export to PDF:** Click to open the system print dialog. Choose "Save as PDF".
- **Export JSON:** Downloads a backup of the current state.
- **Import JSON:** Loads a previously saved estimate.

## Data Privacy

- **No Data Collection:** This tool runs entirely in your browser.
- **Local Storage:** Data is stored in your browser's `localStorage`.
- **Security:** No data is sent to any external server or API. It is safe to use for sensitive client data as long as your local machine is secure.

## Customization

To modify the default values or product list, open `onboarding-estimation-form.html` in a code editor.

### Change Default Hourly Rate

Search for:

```html
<input type="number" id="hourly-rate" value="100" ... >
```

### Modify the Product Dropdown List

Search for the `const PRODUCTS` array in the `<script>` section:

```javascript
const PRODUCTS = [
  "Jira Software",
  "Jira Service Management",
  "Jira Product Discovery",
  "Confluence",
  "Bitbucket",
  "Compass",
  "Atlassian Guard"
];
```

## License

This project is open-source. Feel free to use it for your consultancy business.

Created by Oleksandr.
