# SMART Networking Goal Tracker (NetGrowth)

A lightweight, single-page web application designed to help professionals track and execute a high-velocity networking sprint. By default, it tracks a 14-day sprint to make 70 meaningful professional connections (5 per day), but it can be easily customized for any networking goal.

## 🚀 Features

* **Visual Dashboard:** Real-time metrics tracking your total progress, daily average, and remaining connections. Includes interactive doughnut and bar charts powered by Chart.js to visualize goal completion and daily velocity.
* **Connection Activity Log:** A detailed, tabular record of your professional outreach. Track the date, contact name, platform (LinkedIn, Email, X, etc.), connection quality (1-5 scale), and current status.
* **Outreach Message Vault:** A built-in library of proven networking scripts (e.g., Cold Outreach, Warm Introductions, Follow-ups). Includes a one-click "Copy to Clipboard" feature to speed up your workflow.
* **Quick-Log Modal:** A frictionless popup form to instantly log new connections without leaving the page.
* **Fully Responsive:** Styled with Tailwind CSS to work flawlessly on desktop, tablet, and mobile devices.

## 🛠️ Built With

* **HTML5 & CSS3**
* **Vanilla JavaScript** (No complex frameworks required)
* **Tailwind CSS** (via CDN for rapid, modern styling)
* **Chart.js** (via CDN for data visualization)
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

## ⚙️ Customization

You can easily adjust the sprint parameters to fit your specific goals. Open `index.html`, scroll down to the `<script>` section, and modify the core constants:

```javascript
// --- DATA & STATE ---
const GOAL = 70; // Total number of connections desired
const TARGET_DAILY = 5; // Daily connection target
const START_DATE = new Date('2026-08-08'); // Sprint start date
const END_DATE = new Date('2026-08-21'); // Sprint end date

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

## 📝 Note on Data Storage

Currently, this application runs entirely client-side. The initial data is populated via a mock array, and any new connections added during your session are stored in local memory. **If you refresh the page, newly added connections will be lost.**

*For future development:* To make the data persistent, you can integrate browser `localStorage` or connect the frontend to a backend database (like Firebase, Supabase, or a Node.js/Express server).

## 📄 License

This project is open-source and available under the [MIT License](https://www.google.com/search?q=LICENSE). Feel free to fork, modify, and use it for your own personal or professional growth!
