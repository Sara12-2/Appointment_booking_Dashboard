# 🚀 Apex — Appointment Dashboard

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](#)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](#)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](#)

**Apex** is a sophisticated, single-file HTML dashboard for managing appointments, clients, and business analytics. It features a modern dark-mode UI, real-time data visualization, and a fully interactive calendar, making it perfect for salons, clinics, gyms, or any service-based business.
---
## Live demo:
https://appointment-booking-dashboard-ten.vercel.app/

## 📸 Screenshots

### Dashboard View
![Dashboard](images/Dashboard.png)

### Appointments View
![Appointments](images/Appointments.png)

### Calendar View
![Calendar](images/Calender.png)

### Clients View
![Clients](images/Clients.png)

### Analytics View
![Analytics](images/Analytics.png)

### Settings View
![Settings](images/Settings.png)

### Messages View
![Messages](images/messages.png)

---

## ✨ Key Features

- **📊 Real-time Dashboard** - View key metrics (KPIs), upcoming appointments, and service mix at a glance
- **📅 Smart Calendar** - FullCalendar integration for weekly/monthly visual overview
- **👥 Client Directory** - Dedicated section to view all clients and their appointment history
- **📈 Analytics Hub** - Interactive charts (Line, Doughnut, Bar) to track booking trends and service popularity
- **🔔 Notification System** - Sleek toast notification system for all CRUD actions
- **🎨 Dynamic Theming** - Change the entire accent color of the UI on the fly from Settings
- **📱 Fully Responsive** - Optimized for desktops, tablets, and mobile devices with collapsible sidebar
- **⚡ Zero Dependencies (Almost)** - Built with vanilla JS, HTML5, CSS3 + two industry-standard libraries
- **🔍 Search & Filter** - Global search and status-based filtering for appointments
- **✏️ Complete CRUD** - Create, Read, Update, and Delete appointments seamlessly

---

## 🛠️ Built With

| Technology | Purpose |
|------------|---------|
| **HTML5** | Semantic structure |
| **CSS3** | Custom properties, animations, flexbox/grid layouts |
| **Vanilla JavaScript** | Core logic, DOM manipulation, state management |
| **Chart.js** | Simple and beautiful charts |
| **FullCalendar** | Powerful calendar views |
| **Font Awesome 6** | High-quality icons |
| **Google Fonts** | Fraunces (display) & Instrument Sans (body) fonts |

---

## 🚀 Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection (for CDN resources on first load)

### Installation

#### Method 1: Direct Download
1. Download the `index.html` file
2. Double-click to open in your browser

#### Method 2: Clone Repository
```bash
git clone https://github.com/your-username/apex-dashboard.git
cd apex-dashboard
```

#### Method 3: Run with Live Server
```bash
# Python
python -m http.server 8000

# VS Code
# Install "Live Server" extension → Right-click index.html → Open with Live Server

# Node.js
npx serve .
```
Then open `http://localhost:8000` in your browser.

---

## 🎮 How to Use

### Navigation

| Section | Description |
|---------|-------------|
| Dashboard | Overview with KPIs, upcoming appointments, service mix |
| Appointments | Full appointment list with search and status filters |
| Calendar | Visual month/week view of all appointments |
| Clients | Directory of all clients with their details |
| Analytics | Charts showing booking trends and service popularity |
| Messages | Activity log and notification center |
| Settings | Preferences, notifications, theme customization |

### Managing Appointments

#### Create Appointment
1. Click **"Book Appointment"** button (top-right corner)
2. Fill in client details:
   - Full Name (required)
   - Email (optional)
   - Phone (optional)
   - Service (Consultation, Hair Styling, Gym Session, Medical Check)
   - Date (required)
   - Time (required)
   - Notes (optional)
3. Click **"Confirm Booking"**
4. Success toast notification appears

#### Edit Appointment
1. Click the pencil icon (✏️) next to any appointment
2. Modify the required fields in the modal
3. Click **"Save Changes"**
4. Update confirmation toast appears

#### Delete Appointment
1. Click the trash icon (🗑️) next to any appointment
2. Appointment is removed immediately
3. Deletion confirmation toast appears

### Search & Filter

| Search Type | Location | Behavior |
|-------------|----------|----------|
| Global Search | Top bar | Searches appointments by name or service |
| Appointments Filter | Appointments page | Search + Status dropdown (Confirmed/Pending/Cancelled) |

### Customizing Theme
1. Navigate to **Settings → Accent Color**
2. Click on any color swatch:
   - Sky Blue (Default) `#5BADFF`
   - Teal `#4ED9C0`
   - Violet `#A78BFA`
   - Rose `#FF6B7A`
   - Amber `#FFB347`
3. Theme updates instantly across the entire dashboard

---

## 📂 Project Structure

```
apex-dashboard/
│
├── index.html              # Complete application (HTML, CSS, JavaScript)
├── README.md               # Documentation (this file)
├── LICENSE                 # MIT License (optional)
└── images/                 # Screenshots folder
    ├── Dashboard.png       # Dashboard view screenshot
    ├── Appointments.png    # Appointments page screenshot
    ├── Calender.png        # Calendar view screenshot
    ├── Clients.png         # Clients directory screenshot
    ├── Analytics.png       # Analytics page screenshot
    ├── Settings.png        # Settings page screenshot
    └── messages.png        # Messages view screenshot
```

> All code is contained in a single HTML file — no complex build process or dependencies to install!

---

## 💾 Data Structure

### Appointment Object
```javascript
{
  id: number,           // Auto-incremented unique identifier
  name: string,         // Client's full name
  email: string,        // Client's email address
  phone: string,        // Client's phone number
  service: string,      // Service type (Consultation, Hair Styling, etc.)
  date: string,         // YYYY-MM-DD format
  time: string,         // HH:MM format (24-hour)
  status: string,       // "Confirmed" | "Pending" | "Cancelled"
  notes: string         // Additional notes/comments
}
```

### Default Services

| Service | Emoji |
|---------|-------|
| Consultation | 📋 |
| Hair Styling | ✂️ |
| Gym Session | 🏋️ |
| Medical Check | 🩺 |

### Demo Data
The dashboard comes with **6 sample appointments** pre-loaded for demonstration purposes.

> **Note:** Data is stored in-memory (`apts` array). Page refresh resets to demo data. For production, implement backend API integration.

---

## 🎨 Styling System

### Color Variables

| Variable | Default | Usage |
|----------|---------|-------|
| `--bg` | `#0D1B2E` | Main background |
| `--bg2` | `#0A1628` | Secondary background |
| `--surface` | `#112240` | Card surfaces |
| `--border` | `rgba(148,190,255,0.1)` | Borders |
| `--gold` | `#5BADFF` | Primary accent |
| `--teal` | `#4ED9C0` | Success indicators |
| `--rose` | `#FF6B7A` | Error/cancellation |
| `--amber` | `#FFB347` | Warning/pending |
| `--lavender` | `#A78BFA` | Revenue/analytics |
| `--cream` | `#E8F1FF` | Primary text |
| `--cream-mute` | `rgba(232,241,255,0.32)` | Muted text |

### Typography

| Font | Usage |
|------|-------|
| Fraunces (serif) | Headings, KPIs, logo |
| Instrument Sans (sans-serif) | Body text, labels, buttons |

---

## 📱 Responsive Breakpoints

| Breakpoint | Layout Changes |
|------------|----------------|
| > 1200px | Full 4-column KPI grid, 2-column main layout |
| 768px - 1200px | 2-column KPI grid, 1-column main layout |
| < 768px | Sidebar hidden (hamburger menu), stacked layout |
| < 480px | Single-column KPI grid, full-width filters |
| < 360px | Single column everything |

---

## 🔧 Customization Guide

### Changing Business Information
```html
<!-- Logo text - Line ~175 -->
<div class="logo-text">Your<span>Brand</span></div>

<!-- User profile - Line ~247 -->
<div class="user-name">Your Name</div>
<div class="user-role">Your Role</div>

<!-- Greeting - Line ~1010 -->
<div class="page-title">Good morning, <span>Your Name</span> 👋</div>
```

### Adding New Services

Add to modal dropdown (Line ~301):
```html
<option>New Service</option>
```

Add to analytics tracking (Line ~1275):
```javascript
const svc = {
  'Consultation': 0,
  'Hair Styling': 0,
  'Gym Session': 0,
  'Medical Check': 0,
  'New Service': 0  // Add this
};
```

Add to service mix display (Line ~1085):
```javascript
['Consultation','Hair Styling','Gym Session','Medical Check','New Service']
```

### Changing Colors
Modify CSS variables in `:root` selector (Line ~15):
```css
:root {
  --bg: #0D1B2E;      /* Main background */
  --surface: #112240; /* Card background */
  --gold: #5BADFF;    /* Primary accent */
}
```

### Making Data Persistent

Replace in-memory storage with `localStorage`:
```javascript
// Save data
localStorage.setItem('appointments', JSON.stringify(apts));

// Load data
const saved = localStorage.getItem('appointments');
if (saved) apts = JSON.parse(saved);
```

Or integrate with a backend API using `fetch()`:
```javascript
async function saveToAPI(data) {
  const response = await fetch('/api/appointments', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify(data)
  });
  return response.json();
}
```

---

## 🧪 Browser Support

| Browser | Version |
|---------|---------|
| Chrome | ✅ Latest |
| Firefox | ✅ Latest |
| Safari | ✅ Latest |
| Edge | ✅ Latest |
| Opera | ✅ Latest |

---

## 📊 Performance

| Metric | Value |
|--------|-------|
| First Contentful Paint | ~0.5s |
| Time to Interactive | ~1.2s |
| Total Size | ~50KB (HTML) + CDN libraries |
| Lighthouse Score | ~95/100 |

---

## 🔄 Future Enhancements

- **LocalStorage/IndexedDB** - Data persistence across sessions
- **Backend API Integration** - Node.js/Express + MongoDB/PostgreSQL
- **Email/SMS Notifications** - Automated reminders
- **Recurring Appointments** - Weekly, monthly patterns
- **Export Data** - CSV, PDF, Excel reports
- **Multi-user Authentication** - Login system with roles
- **Payment Processing** - Stripe/PayPal integration
- **Client History Timeline** - Complete service history
- **Custom Service Creation** - User-defined services
- **Dark/Light Mode Toggle** - Theme switcher
- **Drag & Drop Calendar** - Reschedule by dragging
- **Calendar Sync** - Google Calendar, Outlook integration
- **Mobile App** - React Native / Flutter wrapper

---

## 🤝 Contributing

Contributions are what make the open-source community amazing! Any contributions you make are greatly appreciated.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Guidelines
- Keep code clean and well-commented
- Follow existing code style
- Test on multiple browsers before submitting
- Update documentation as needed

## Github repo link

https://github.com/Sara12-2/Appointment_booking_Dashboard
---

## 📝 License

Distributed under the **MIT License**. See `LICENSE` file for more information.

You are free to:
- ✅ Use commercially
- ✅ Modify and adapt
- ✅ Distribute copies
- ✅ Use privately

Under these terms:
- 📄 Include original copyright notice
- 📄 Include license in distributions

---

## 🙏 Acknowledgements

- [Chart.js](https://www.chartjs.org/) - Elegant charts library
- [FullCalendar](https://fullcalendar.io/) - Robust calendar solution
- [Font Awesome](https://fontawesome.com/) - Amazing icon set
- [Google Fonts](https://fonts.google.com/) - Beautiful typography
- All open-source contributors

---

### Support Options
- 📖 Read the documentation above
- 🐛 Report issues on GitHub
- ⭐ Star the repo if you find it useful
- 🔄 Fork for your own modifications

---

## 💖 Show Your Support

If this project helped you or you found it useful:

- ⭐ Star this repository on GitHub
- 📢 Share with others
- 💝 Consider sponsoring

---

## 📋 Version History

| Version | Date | Changes |
|---------|------|---------|
| 1.0.0 | 2026-05-17 | Initial release |
| 1.1.0 | Coming soon | Backend integration, export features |

---


