NetGrowth 2026
A lightweight, single-page SMART Networking Goal Tracker for managing a 14-day professional networking sprint. Track meaningful connections, monitor daily outreach velocity, view progress charts, and copy outreach-message templates—all in the browser.

Features
SMART goal dashboard

Goal: 70 professional connections

Duration: 14 days

Daily target: 5 connections

Displays total progress, completion percentage, daily average, elapsed days, and remaining connections

Visual analytics

Doughnut chart for overall completion progress

Bar-and-line chart for daily connection velocity versus the target

Connection activity log

Add new connections through a modal form

Track platform and relationship quality on a 1–5 scale

View contact date, name, company/role details, platform, quality, and status

Includes sample connection data for demonstration

Outreach template vault

Six ready-to-use networking scripts:

Cold outreach to peers

Cold outreach to leaders

Warm introductions

No-reply follow-ups

Post-meeting thank-yous

Value-add nurture messages

One-click copy-to-clipboard functionality

Responsive interface

Built with Tailwind CSS

Optimized for desktop and mobile layouts

Tab-based navigation for Dashboard, Daily Log, and Templates

Tech Stack
Technology	Purpose
HTML5	Application structure
Tailwind CSS	Responsive styling and layout
Vanilla JavaScript	Application state, rendering, tabs, modal, and interactions
Chart.js	Progress doughnut and daily-velocity charts
Google Fonts	Inter typeface
Getting Started
This project does not require a build process, package manager, or backend.

Download or clone this repository:

bash
git clone https://github.com/your-username/netgrowth-2026.git
Navigate into the project directory:

bash
cd netgrowth-2026
Open index.html in a modern browser.

Alternatively, launch it with a simple local server:

bash
python -m http.server 8000
Then visit http://localhost:8000 in your browser.

Project Structure
text
netgrowth-2026/
├── index.html      # Entire application: markup, styles, and JavaScript
└── README.md       # Project documentation
How It Works
Dashboard
The Dashboard calculates progress using these default values:

javascript
const GOAL = 70;
const TARGET_DAILY = 5;
const START_DATE = new Date('2026-08-08');
const END_DATE = new Date('2026-08-21');
It updates the following metrics whenever a connection is added:

Total logged connections

Percentage of the 70-connection goal completed

Average connections per elapsed day

Days elapsed in the 14-day sprint

Connections remaining to reach the milestone

Adding a Connection
Open the Daily Log tab.

Select Log New Connection.

Enter the contact name.

Choose the outreach platform.

Set a quality score from 1 to 5.

Select Save to Log.

New entries are automatically added with:

Today’s date

Self-Added Entry as the company/role detail

Awaiting Reply as the status

Templates
Open the Templates tab and select Copy to Clipboard on any outreach script. Replace placeholders such as [Name], [Company], and [Topic] before sending your message.

Customization
Change the goal or timeframe
Edit the constants in the <script> section of index.html:

javascript
const GOAL = 70;
const TARGET_DAILY = 5;
const START_DATE = new Date('2026-08-08');
const END_DATE = new Date('2026-08-21');
For example, to run a 30-day sprint with a goal of 120 connections:

javascript
const GOAL = 120;
const TARGET_DAILY = 4;
const START_DATE = new Date('2026-09-01');
const END_DATE = new Date('2026-09-30');
If you change the duration, also update the hard-coded 14 values used in the dashboard labels and chart-data arrays.

Update initial sample data
Modify the connections array:

javascript
let connections = [
  {
    id: 1,
    date: '2026-08-08',
    name: 'Jane Doe',
    details: 'TechCorp, Sr. PM',
    platform: 'LinkedIn',
    quality: 4,
    status: 'Awaiting Reply'
  }
];
Add or edit outreach templates
Modify the templates array:

javascript
const templates = [
  {
    title: "Cold Outreach (Peer)",
    text: "Hi [Name], I've been following your work at [Company]..."
  }
];
Current Limitations
Connection data is stored only in JavaScript memory.

Refreshing or closing the browser resets newly added entries.

There is no authentication, database, cloud sync, export, edit, or delete capability.

The add-connection form does not currently collect company/role details or a custom follow-up status.

Tailwind CSS and Chart.js load from CDNs, so an internet connection is needed for their hosted resources.

Future Improvements
Persist connections with localStorage, Firebase, Supabase, or a REST API

Add edit and delete actions for logged contacts

Add custom fields for company, role, notes, and follow-up date

Export the activity log as CSV

Add filters by platform, quality, or status

Add streak tracking and daily reminder notifications

Support configurable goals and sprint lengths through the UI

Add dark mode and accessibility enhancements

License
This project is available under the MIT License. Add a LICENSE file to the repository if you plan to distribute or open-source it.
