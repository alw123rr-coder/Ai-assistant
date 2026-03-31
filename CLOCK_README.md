# 🕐 Digital Clock - Multiple Timezones

A beautiful, real-time digital clock displaying the current time across multiple timezones.

## Features

✨ **Real-time Updates** - Automatically updates every second
🌍 **Multiple Timezones** - Displays 8 different timezones:
  - UTC (Coordinated Universal Time)
  - EST (US Eastern Standard Time)
  - CST (US Central Standard Time)
  - PST (US Pacific Standard Time)
  - IST (Indian Standard Time)
  - GMT (Greenwich Mean Time)
  - JST (Japan Standard Time)
  - AEST (Australian Eastern Standard Time)

📱 **Responsive Design** - Works on desktop, tablet, and mobile
🎨 **Modern UI** - Beautiful gradient background with smooth animations

## Installation

### Step 1: Install Dependencies
```bash
pip install Flask pytz
```

### Step 2: Run the Application
```bash
python clock.py
```

### Step 3: Open in Browser
Navigate to: **http://localhost:5001**

## File Structure
```
Ai-assistant/
├── clock.py                    # Main Flask application
├── templates/
│   └── clock.html             # HTML template
└── static/
    ├── clock.css              # Styling
    └── clock.js               # JavaScript for updates
```

## How It Works

1. **Backend (clock.py)**:
   - Uses Flask to serve the application
   - Provides `/api/time` endpoint that returns current time in all timezones
   - Uses `pytz` library for timezone handling

2. **Frontend (clock.html, clock.js, clock.css)**:
   - Fetches time data every second from the API
   - Displays time in beautiful cards
   - Responsive grid layout
   - Smooth animations and hover effects

## API Endpoint

**GET /api/time**

Returns JSON with current time for all timezones:
```json
{
  "UTC": {
    "time": "14:30:45",
    "date": "Tuesday, March 31, 2026",
    "timezone": "UTC"
  },
  "EST": {
    "time": "10:30:45",
    "date": "Tuesday, March 31, 2026",
    "timezone": "EST"
  }
  ...
}
```

## Customization

To add more timezones, edit the `TIMEZONES` dictionary in `clock.py`:

```python
TIMEZONES = {
    'UTC': 'UTC',
    'EST': 'US/Eastern',
    'YOUR_TZ': 'Your/Timezone',  # Add your timezone
    ...
}
```

List of valid timezone strings: https://en.wikipedia.org/wiki/List_of_tz_database_time_zones

## Technologies Used

- **Backend**: Python, Flask
- **Frontend**: HTML5, CSS3, JavaScript (Vanilla)
- **Timezone Handling**: pytz library

## Browser Support

✅ Chrome
✅ Firefox
✅ Safari
✅ Edge
✅ Mobile browsers

## License

MIT License - Feel free to use and modify!