# SMART Networking Goal Tracker (NetGrowth)

A lightweight, single-page web application designed to help professionals track and execute a high-velocity networking sprint. By default, it tracks a 14-day sprint to make 70 meaningful professional connections (5 per day), but it can be easily customized for any networking goal.

## 🚀 Features

* **Visual Dashboard:** Real-time metrics tracking your total progress, daily average, and remaining connections. Includes interactive doughnut and bar charts powered by Chart.js to visualize goal completion and daily velocity.
* **Connection Activity Log:** A detailed, tabular record of your professional outreach. Track the date, contact name, platform, connection quality, and current status. **Click on any logged connection to edit its details.**
* **Cloud Sync & Data Vault (NEW):** Automatically syncs your progress to the cloud via Firebase. Includes a dedicated Data Vault where you can export a local `.json` backup of your data or permanently wipe your slate clean.
* **Outreach Message Vault:** A built-in library of proven networking scripts (e.g., Cold Outreach, Warm Introductions, Follow-ups) with a one-click "Copy to Clipboard" feature.
* **Quick-Log Modal:** A frictionless popup form to instantly log or edit connections without leaving the page.
* **Fully Responsive:** Styled with Tailwind CSS to work flawlessly on desktop, tablet, and mobile devices.

## 🛠️ Built With

* **HTML5 & CSS3**
* **Vanilla JavaScript** (No complex frameworks required)
* **Tailwind CSS** (via CDN for rapid, modern styling)
* **Chart.js** (via CDN for data visualization)
* **Firebase SDK** (v11.6.1 via CDN for Cloud Firestore and Anonymous Authentication)
* **Google Fonts** (Inter font family)

## 🏁 Getting Started

Since this project relies on CDNs and Vanilla JavaScript, there are no build steps, package managers, or dependencies to install.

1. **Clone the repository:**

```bash
git clone https://github.com/yourusername/netgrowth-tracker.git

```

2. **Navigate to the project directory:**

```bash
cd netgrowth-tracker

```

3. **Run the application:**
Simply double-click the `index.html` file to open it in your default web browser, or serve it using a local development server (like VS Code's Live Server extension).

*Note: Without a Firebase configuration injected, the app will gracefully fall back to **Offline Mode**, loading demo data. In offline mode, you can still use the tracker and export your data as a JSON file via the Data Vault before closing the tab.*

## ⚙️ Customization

You can easily adjust the sprint parameters to fit your specific goals. Open `index.html`, scroll down to the `<script>` section, and modify the core constants:

```javascript
// --- DATA & STATE ---
const GOAL = 70;
const TARGET_DAILY = 5;
const START_DATE = new Date('2026-08-08T00:00:00');

```

### Adding New Templates

To add your own custom outreach scripts to the "Templates" tab, simply add a new object to the `templates` array in the JavaScript section:

```javascript
const templates = [
    // ... existing templates ...
    { 
      title: "Your Custom Title", 
      text: "Hi [Name], your custom message goes here!" 
    }
];

```

## 📝 Data Storage & Sync

This application now features robust data handling:

* **Cloud Persistence:** If connected to a Firebase instance (by supplying standard Firebase config variables to the script), the app signs the user in anonymously (or via custom token) and syncs all connections to Cloud Firestore in real-time.
* **Live Status Indicator:** The top navigation bar includes a dynamic sync indicator letting you know when data is syncing, successfully saved, or operating in offline mode.
* **Local Backups:** Regardless of cloud connection status, you can visit the **Data Vault** tab to instantly download your entire connection log as a JSON file—perfect for importing into Excel, Notion, or keeping a hard offline copy.

## 📄 License

This project is open-source and available under the [MIT License](https://opensource.org/licenses/MIT). Feel free to fork, modify, and use it for your own personal or professional growth!
