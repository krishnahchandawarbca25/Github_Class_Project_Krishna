

# **INFOSPHERE - INTEGRATED SEARCH & NEWS HUB**
## **Complete Project Documentation**

---

## **TABLE OF CONTENTS**

1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Technology Stack](#technology-stack)
4. [Installation & Setup](#installation--setup)
5. [Usage Guide](#usage-guide)
6. [Code Structure](#code-structure)
7. [API Integration](#api-integration)
8. [Design & UI](#design--ui)
9. [Component Details](#component-details)
10. [Future Enhancements](#future-enhancements)
11. [Troubleshooting](#troubleshooting)
12. [Author Information](#author-information)

---

## **PROJECT OVERVIEW**

**Infosphere** is a unified web application that consolidates multiple internet utilities into a single, elegant platform. It combines web search, real-time news feeds, and weather intelligence into one accessible interface with a modern dark-mode design.

### **Purpose**

Rather than jumping between multiple tabs and applications to access different services, users can access everything they need from Infosphere:
- Search the web seamlessly
- Browse global news by category
- Check weather forecasts for any location
- All within a beautiful, cohesive interface

### **Target Audience**

- Information researchers
- News enthusiasts
- Students and professionals
- Anyone who wants centralized access to web utilities

### **Project Repository**

```
GitHub: krishnahchandawarbca25/web-semister-exam
File: testing.html
Commit: bb07c43bd33e243b80eaba53402e6a9f1eabe757
```

---

## **FEATURES**

### **1. Global News Feed**

- **Real-time Headlines** - Powered by NewsAPI.org
- **Category Filtering** - Browse by:
  - General
  - Business
  - Technology
  - Health
  - Science
  - Sports
  - Entertainment
- **Rich Card Display** - Each article shows:
  - Thumbnail image (with fallback icon)
  - Headline (clickable link to source)
  - Description
  - Source attribution
  - Publication time
- **Fallback System** - Mock data displays if API fails

### **2. Weather Intelligence Hub**

- **City Autocomplete** - Real-time suggestions as you type
- **Current Weather Display**:
  - Temperature and condition
  - Humidity percentage
  - Wind speed
  - "Feels like" temperature
  - Visibility/pressure
- **7-Day Forecast** - Shows max/min temperatures and weather icons
- **Geolocation Support** - One-click weather for current location
- **WMO Code Mapping** - Weather codes converted to readable descriptions

### **3. Web Search Gateway**

- **Multi-Tab Browser** - Create and manage multiple search tabs
- **Bing Integration** - Powered by Bing search engine
- **Quick Access Panel** - Speed dial to:
  - Gmail
  - GitHub
  - YouTube
  - ChatGPT
- **Tab Management** - Open, close, and minimize tabs
- **URL Bar** - Shows current tab's address

### **4. Theme Customization**

- **Dark/Light Mode Toggle** - Smooth theme switching
- **Jewel-Tone Palette** - Custom color scheme:
  - Deep Navy background
  - Teal accents
  - Coral highlights
  - Golden yellow elements
- **Persistent Storage** - Theme preference saved in localStorage
- **Animated Transitions** - 0.5s smooth color transitions

### **5. Visual Enhancements**

- **Three.js Starfield** - Animated background with rotating stars
- **Video Background Option** - High-quality Mixkit video
- **Animated Gradient Overlay** - Subtle depth effect
- **Custom Scrollbars** - Themed to match app design
- **Fade-in Animations** - Smooth section transitions
- **Responsive Design** - Works on desktop, tablet, and mobile

---

## **TECHNOLOGY STACK**

### **Frontend**

| Component | Technology | Purpose |
|-----------|-----------|---------|
| **Structure** | HTML5 | Semantic markup |
| **Styling** | Tailwind CSS + Custom CSS | Responsive design, themes |
| **Icons** | Lucide Element | Clean, modern icons |
| **3D Graphics** | Three.js | Starfield background |
| **Weather Icons** | Weather Icons 2.0.10 | Weather condition icons |
| **Markdown** | Marked.js | Parse markdown content |
| **Runtime** | Vanilla JavaScript (ES6+) | No frameworks |

### **External APIs**

| API | Provider | Purpose | Authentication |
|-----|----------|---------|-----------------|
| News API | newsapi.org | Live news headlines | API Key |
| Geocoding API | open-meteo.com | City location search | None (Free) |
| Weather API | open-meteo.com | Weather data & forecast | None (Free) |
| Bing Search | bing.com | Web search integration | Browser-based |

### **CDN Resources**

```html
<script src="https://cdn.tailwindcss.com"></script>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/weather-icons/2.0.10/css/weather-icons.min.css" />
<script src="https://unpkg.com/lucide-element@latest/dist/lucide-element.js"></script>
<script src="https://cdn.jsdelivr.net/npm/marked@12.0.2/lib/marked.umd.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
```

---

## **INSTALLATION & SETUP**

### **Prerequisites**

- Modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection (for API calls)
- No installation required

### **Quick Start**

1. **Download the file**
   ```bash
   git clone https://github.com/krishnahchandawarbca25/web-semister-exam.git
   cd web-semister-exam
   ```

2. **Open in browser**
   ```bash
   # Simply open the file:
   open testing.html
   # Or drag-and-drop into browser
   ```

3. **Grant permissions** (when prompted)
   - Allow geolocation for weather feature
   - Allow clipboard access for quick links

### **Configuration**

#### **NewsAPI Key Setup**

To use live news, add your API key:

1. Visit [newsapi.org](https://newsapi.org)
2. Sign up for free tier account
3. Copy your API key
4. In `testing.html`, find line 826:
   ```javascript
   const NEWS_API_KEY = '59266ddc0e244208b727e03111ec1213';
   ```
5. Replace with your own key:
   ```javascript
   const NEWS_API_KEY = 'your_api_key_here';
   ```

**Note:** The app includes fallback mock data if API key is invalid.

---

## **USAGE GUIDE**

### **Navigating the App**

#### **Sidebar Navigation**
- **Web Search** - Access web search and quick links
- **Global News Feed** - Browse news by category
- **Weather Hub** - Check weather forecasts

#### **Theme Toggle**
- Click moon icon → switches to light mode
- Click sun icon → switches to dark mode
- Preference auto-saved

#### **Sidebar Collapse**
- Click chevron icon to collapse/expand sidebar
- Content area expands to fill space
- Useful on smaller screens

#### **Background Selection**
- Dropdown menu lets you choose:
  - **Stars** - Three.js animated starfield
  - **Video** - Mixkit video background

### **Using News Feed**

1. Navigate to "Global News Feed" tab
2. Select category from dropdown (default: General)
3. Browse article cards
4. Click on title to read full article on source website
5. View source name and publication time

### **Using Weather Hub**

#### **Search by City Name**
1. Navigate to "Weather Hub" tab
2. Start typing city name in search box
3. Select from autocomplete suggestions (shows country & coordinates)
4. View current weather and 7-day forecast

#### **Use Current Location**
1. Click map-pin icon
2. Allow browser to access location
3. Weather for your location loads automatically

#### **Weather Information Displayed**
- Current temperature
- Weather condition (e.g., "Partly Cloudy")
- Humidity percentage
- Wind speed
- "Feels like" temperature
- Atmospheric pressure/visibility
- 7-day forecast with daily high/low temps

### **Using Web Search**

1. Navigate to "Web Search Gateway" tab
2. Enter search query in search box
3. Click search button or press Enter
4. Modal browser window opens
5. Browse results in embedded browser
6. Use tab management:
   - Click "+" to open new tab
   - Click "X" on tab to close it
   - Click minimize to hide browser (keep tabs open)
   - Click close (X-circle) to close all tabs

#### **Quick Access Links**
Click any quick link to open in new tab:
- **Gmail** - gmail.com
- **GitHub** - github.com
- **YouTube** - youtube.com
- **ChatGPT** - chatgpt.com

---

## **CODE STRUCTURE**

### **File Organization**

```
testing.html (1,480 lines total)
├── HTML Structure (500 lines)
│   ├── Head metadata and CDN imports
│   ├── Sidebar navigation
│   ├── News feed section
│   ├── Weather hub section
│   ├── Web search section
│   └── Browser modal
├── CSS Styling (500 lines)
│   ├── Theme variables (dark & light mode)
│   ├── Component styles
│   ├── Animations & transitions
│   ├── Responsive media queries
│   └── Custom scrollbar
└── JavaScript (480 lines)
    ├── Global configuration & API keys
    ├── Utility functions
    ├── News feed functions
    ├── Weather hub functions
    └── Event listeners & initialization
```

### **Key Directories & Sections**

#### **HTML Structure**
- `<aside id="sidebar">` - Navigation sidebar
- `<main id="content-area">` - Main content area with three tabs
- `<section id="news-tab">` - News feed UI
- `<section id="weather-tab">` - Weather hub UI
- `<section id="web-tab">` - Web search UI

#### **CSS Sections**
- `:root` - Dark mode variables
- `:root.light` - Light mode variables
- `.card` - Card component styling
- `.weather-*` - Weather component styles
- `.forecast-*` - Forecast component styles
- `.speed-dial-*` - Quick access link styles
- `.chat-*` - (Reserved for future chat feature)
- `.modal-*` - Modal overlay styles

#### **JavaScript Functions**

**Utility Functions**
- `formatTime(isoString)` - Format timestamps
- `getWeatherIcon(code, isDay)` - Map weather codes to icons
- `debounce(func, delay)` - Debounce function calls

**News Functions**
- `renderNewsCards(articles)` - Create news article cards
- `loadNewsFeed(topic)` - Fetch news from API

**Weather Functions**
- `fetchCitySuggestions(query)` - Get city autocomplete
- `fetchWeatherData(lat, lon, cityName)` - Get weather data
- `renderWeatherUI(data, cityName)` - Display weather UI

**Event Handlers**
- Sidebar toggle
- Theme toggle
- Tab switching
- Form submissions
- Modal management

---

## **API INTEGRATION**

### **NewsAPI Integration**

#### **Endpoint**
```
https://newsapi.org/v2/top-headlines
```

#### **Request Parameters**
```javascript
{
  country: 'us',           // Country code
  category: 'general',     // News category
  pageSize: 10,           // Articles per request
  apiKey: YOUR_API_KEY    // Authentication
}
```

#### **Response Handling**
```javascript
if (data.status === "ok" && data.articles.length > 0) {
    newsContainer.innerHTML = renderNewsCards(data.articles);
} else {
    newsContainer.innerHTML = renderNewsCards(MOCK_NEWS_DATA.articles);
}
```

### **Open-Meteo API Integration**

#### **Geocoding Endpoint**
```
https://geocoding-api.open-meteo.com/v1/search
```

**Parameters:**
- `name` - City name query
- `count` - Max results (5)
- `language` - Result language (en)
- `format` - Response format (json)

#### **Weather Endpoint**
```
https://api.open-meteo.com/v1/forecast
```

**Parameters:**
- `latitude` / `longitude` - Location coordinates
- `current` - Current weather fields
- `daily` - Daily forecast fields
- `timezone` - Timezone selection (auto)

#### **Current Weather Fields**
```javascript
current=temperature_2m,
        relative_humidity_2m,
        apparent_temperature,
        precipitation,
        weather_code,
        wind_speed_10m,
        surface_pressure
```

#### **Daily Forecast Fields**
```javascript
daily=weather_code,
      temperature_2m_max,
      temperature_2m_min,
      sunrise,
      sunset
```

### **WMO Weather Code Mapping**

```javascript
const wmoMap = {
    0: 'Clear Sky',
    1: 'Mainly Clear',
    2: 'Partly Cloudy',
    3: 'Overcast',
    45: 'Fog',
    48: 'Depositing Rime Fog',
    51: 'Light Drizzle',
    61: 'Slight Rain',
    65: 'Heavy Rain',
    71: 'Slight Snow',
    80: 'Slight Showers',
    95: 'Thunderstorm'
};
```

---

## **DESIGN & UI**

### **Color Palette**

#### **Dark Mode (Default)**
```css
--bg: #071428              /* Deep Navy */
--card: #0f2a3a            /* Dark Teal Card */
--text: #ffffff            /* White Text */
--accent1: #0fb5a6         /* Vivid Teal */
--accent2: #ff7a59         /* Warm Coral */
--accent3: #ffd166         /* Golden Yellow */
--border: #1f3f50          /* Dark Border */
--warning: #ef4444         /* Red */
--success: #10b981         /* Green */
```

#### **Light Mode**
```css
--bg: #f8fafc              /* Light Gray */
--card: #ffffff            /* White */
--text: #1e293b            /* Dark Blue-Gray */
--accent1: #0ea5e9         /* Sky Blue */
--accent2: #f59e0b         /* Amber */
--accent3: #10b981         /* Emerald */
--border: #e2e8f0          /* Light Border */
```

### **Layout Architecture**

```
┌─────────────────────────────────────────────────────┐
│  Sidebar (280px)  │  Content Area (Flexible)        │
├─────────────────────────────────────────────────────┤
│ • Infosphere Logo │  Selected Tab Content           │
│ • Navigation      │  (News / Weather / Search)      │
│ • Theme Toggle    │                                 │
│ • BG Selector     │                                 │
│ • Collapse Btn    │                                 │
└─────────────────────────────────────────────────────┘
```

### **Responsive Breakpoints**

- **Mobile** - Single column, collapsed sidebar
- **Tablet** - Adjustable layout, sidebar collapsible
- **Desktop** - Full sidebar + content area (280px + flexible)

### **Animation & Transitions**

| Animation | Duration | Use Case |
|-----------|----------|----------|
| Fade in | 0.6s | Section entrance |
| Smooth scroll | 0.3s | Sidebar collapse |
| Color transition | 0.5s | Theme switching |
| Pulse effect | 1.5s | Live indicator |
| Hover scale | 0.3s | Interactive elements |
| Box shadow | 0.3s | Hover effects |

---

## **COMPONENT DETAILS**

### **Sidebar Component**

**HTML Structure**
```html
<aside id="sidebar" class="fixed top-0 left-0 h-screen z-20">
    <div class="flex items-center justify-between">
        <h1>Infosphere</h1>
        <div class="flex items-center space-x-2">
            <button id="theme-toggle">☀️/🌙</button>
            <select id="bg-selector">
                <option value="threejs">Stars</option>
                <option value="video">Video</option>
            </select>
            <button id="toggle-sidebar">◀◀</button>
        </div>
    </div>
    <nav class="space-y-3">
        <!-- Navigation links -->
    </nav>
</aside>
```

**CSS Classes**
- `.sidebar.collapsed` - Slides out of view
- `.nav-link` - Navigation items
- `.active-tab` - Current tab indicator

---

### **News Feed Component**

**Article Card Structure**
```html
<div class="card p-4 rounded-xl shadow-md flex">
    <img src="thumbnail" class="w-24 h-24 object-cover rounded-lg mr-4">
    <div>
        <a href="article-url" class="text-lg font-semibold text-accent1">
            Article Title
        </a>
        <p class="text-muted text-sm mt-1">Description text...</p>
        <p class="text-xs text-muted mt-2">
            Source Name • Publication Time
        </p>
    </div>
</div>
```

**Features**
- Image fallback (shows icon if no image available)
- Click-through to original article
- Responsive layout

---

### **Weather Component**

**Search Box**
```html
<input id="weather-search-input" 
       type="text" 
       placeholder="Search City..."
       autocomplete="off">
<div id="city-suggestions" class="suggestion-list"></div>
```

**Current Weather Card**
```html
<div class="weather-current-card">
    <h3 id="weather-city-name">City Name</h3>
    <p id="weather-date">Monday, 12 Oct</p>
    <div class="flex items-center">
        <i id="current-weather-icon" class="wi wi-day-sunny"></i>
        <span id="current-temp">28°C</span>
        <p id="current-condition">Partly Cloudy</p>
    </div>
</div>
```

**Detail Grid**
```
┌──────────────┬──────────────┐
│   Humidity   │  Wind Speed  │
│     65%      │   15 km/h    │
├──────────────┼──────────────┤
│ Feels Like   │ Visibility   │
│     26°C     │   10 km      │
└──────────────┴──────────────┘
```

---

### **Browser Modal Component**

**Structure**
```html
<div id="browser-modal" class="fixed inset-0 hidden">
    <div class="bg-card rounded-2xl flex flex-col">
        <!-- Tab Bar -->
        <div id="browser-tabs" class="flex items-center gap-1">
            <!-- Tabs dynamically added -->
            <button id="new-tab-btn">+</button>
        </div>
        
        <!-- URL Bar & Controls -->
        <div class="flex items-center gap-4">
            <button id="close-browser-btn">✕</button>
            <button id="minimize-browser-btn">−</button>
            <input id="browser-url-bar" type="text" readonly>
        </div>
        
        <!-- Content Area -->
        <div id="browser-content-area">
            <!-- Iframes loaded here -->
        </div>
    </div>
</div>
```

**Tab Management**
- Each tab has unique ID: `_abc123def`
- Stores URL and iframe reference
- Tab button shows URL domain
- Active tab highlighted with different background color

---

## **FUTURE ENHANCEMENTS**

### **Phase 2: User Features**
- [ ] Save favorite articles and cities
- [ ] Search history with quick access
- [ ] Bookmarks for frequently visited sites
- [ ] Custom news sources

### **Phase 3: Advanced Features**
- [ ] User authentication system
- [ ] Cloud synchronization
- [ ] Offline mode with caching
- [ ] PWA (Progressive Web App) support
- [ ] Mobile app wrapper

### **Phase 4: AI & Automation**
- [ ] ChatGPT integration for news summaries
- [ ] Voice search functionality
- [ ] Personalized news recommendations
- [ ] Weather alerts and notifications

### **Phase 5: Additional Integrations**
- [ ] Stock market ticker
- [ ] Cryptocurrency prices
- [ ] Social media feeds
- [ ] Email client integration
- [ ] Calendar integration

### **Phase 6: Internationalization**
- [ ] Multi-language support
- [ ] Article translation
- [ ] Regional weather units (Celsius/Fahrenheit)
- [ ] Localized news sources

---

## **TROUBLESHOOTING**

### **Issue: News not loading**

**Symptoms:** News tab shows error message

**Solutions:**
1. Check internet connection
2. Verify NewsAPI key is valid (32 characters)
3. Check API rate limit hasn't been exceeded
4. Fallback mock data should display if API fails

**Code to check:**
```javascript
if (NEWS_API_KEY.length !== 32) {
    console.log("API key invalid");
    // Falls back to mock data
}
```

---

### **Issue: Weather data not appearing**

**Symptoms:** Weather section stays loading

**Solutions:**
1. Verify city name is correctly spelled
2. Check internet connection
3. Try clicking autocomplete suggestion instead of typing manually
4. Try using geolocation button for current location

**Debug:**
```javascript
// Check browser console (F12) for error messages
console.error("Weather data error:", error);
```

---

### **Issue: Geolocation not working**

**Symptoms:** Map-pin button doesn't trigger location detection

**Solutions:**
1. Ensure browser permission is granted
2. Refresh page and try again
3. Check browser settings allow geolocation
4. Use Firefox or Chrome (best compatibility)

**Permission check:**
```javascript
if (!navigator.geolocation) {
    console.log("Geolocation not supported");
}
```

---

### **Issue: Theme not persisting**

**Symptoms:** Theme resets to dark mode on page refresh

**Solutions:**
1. Clear browser cache (Ctrl+Shift+Delete)
2. Check localStorage is enabled in browser
3. Try alternative browser
4. Check browser isn't in private/incognito mode

**Storage check:**
```javascript
localStorage.setItem('theme', 'light');
const savedTheme = localStorage.getItem('theme');
console.log(savedTheme); // Should show 'light'
```

---

### **Issue: Sidebar not collapsing**

**Symptoms:** Chevron button doesn't collapse sidebar

**Solutions:**
1. Refresh browser (F5)
2. Check browser console for JavaScript errors
3. Try clicking chevron again (double-click if needed)
4. Clear browser cache

---

## **PERFORMANCE OPTIMIZATION**

### **Current Optimizations**

1. **Debounced API calls** - City suggestions throttled to 300ms intervals
2. **Lazy loading** - Sections hidden by default, shown on demand
3. **CSS variables** - Efficient theme switching without reflows
4. **Event delegation** - Single listeners for dynamic elements
5. **Image optimization** - Thumbnail images cached by browser

### **Potential Improvements**

- Implement service workers for offline functionality
- Add image lazy-loading for news thumbnails
- Minify CSS and JavaScript in production
- Implement pagination for news feed
- Cache API responses

---

## **BROWSER COMPATIBILITY**

| Browser | Version | Status |
|---------|---------|--------|
| Chrome | 90+ | ✅ Fully supported |
| Firefox | 88+ | ✅ Fully supported |
| Safari | 14+ | ✅ Fully supported |
| Edge | 90+ | ✅ Fully supported |
| Mobile Safari | 14+ | ⚠️ Limited (smaller screens) |
| Chrome Mobile | Latest | ⚠️ Limited (smaller screens) |

---

## **SECURITY CONSIDERATIONS**

### **API Keys**
- NewsAPI key is visible in code (consider server-side proxying for production)
- Open-Meteo API has no authentication, requires no secrets
- Browser-based search doesn't transmit sensitive data

### **iframe Sandboxing**
- Browser modal iframes use sandbox attributes for security
- Restrictions: `allow-same-origin allow-scripts allow-forms allow-popups`
- Prevents XSS attacks and unauthorized access

### **Data Privacy**
- No user data is stored on external servers
- localStorage only stores theme preference locally
- Geolocation data is used locally, not transmitted to our servers

---

## **MAINTENANCE & UPDATES**

### **Regular Maintenance Tasks**

1. **Monthly:** Check API status pages for downtime notifications
2. **Quarterly:** Update CDN library versions
3. **Quarterly:** Review and update mock data
4. **Semi-annually:** Check for browser compatibility issues

### **Dependency Updates**

- Tailwind CSS - Monitor for security patches
- Three.js - Update for new features
- Lucide Icons - Keep current for new icons
- Weather Icons - Monitor for new icon support

---

## **DEPLOYMENT OPTIONS**

### **Option 1: GitHub Pages (Recommended)**

```bash
# Push to GitHub Pages branch
git push origin main --force
# Enable Pages in repository settings
# Site available at: https://krishnahchandawarbca25.github.io/web-semister-exam
```

### **Option 2: Netlify**

```bash
# Upload testing.html to Netlify
# Drag and drop into Netlify dashboard
# Instant deployment, automatic HTTPS
```

### **Option 3: Self-hosted**

```bash
# Copy testing.html to web server
# Serve via Apache, Nginx, or similar
# Ensure server allows CORS for API calls
```

### **Option 4: Static Server**

```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx http-server

# Using PHP
php -S localhost:8000
```

---

## **AUTHOR INFORMATION**

**Student Name:** Krishna Chandawar  
**GitHub:** @krishnahchandawarbca25  
**Repository:** [web-semister-exam](https://github.com/krishnahchandawarbca25/web-semister-exam)  
**Project Date:** March 2026  
**Course:** Web Semester Exam Project  

### **Contact & Support**

For issues or questions:
- Open an issue on GitHub
- Check documentation above
- Review code comments in HTML file

---

## **LICENSE**

This project is open-source and available for educational use.

---

## **CHANGELOG**

### **Version 1.0** (March 11, 2026)
- ✅ Initial release
- ✅ News feed functionality
- ✅ Weather hub with 7-day forecast
- ✅ Web search with multi-tab browser
- ✅ Dark/Light theme toggle
- ✅ Three.js starfield background
- ✅ Responsive design

---

## **QUICK REFERENCE**

### **Keyboard Shortcuts**
- `M` - Toggle theme (future implementation)
- `CTRL+N` - New search tab (via quick search)
- `ESC` - Close browser modal

### **Common API Responses**

**Successful News Response:**
```json
{
  "status": "ok",
  "articles": [
    {
      "title": "Article Title",
      "description": "Article description",
      "url": "https://source.com/article",
      "urlToImage": "https://source.com/image.jpg",
      "publishedAt": "2026-03-11T10:30:00Z",
      "source": { "name": "Source Name" }
    }
  ]
}
```

**Weather Response:**
```json
{
  "current": {
    "temperature_2m": 28,
    "weather_code": 2,
    "humidity": 65,
    "wind_speed_10m": 15
  },
  "daily": {
    "time": ["2026-03-11", "2026-03-12"],
    "temperature_2m_max": [28, 26],
    "temperature_2m_min": [18, 16],
    "weather_code": [2, 3]
  }
}
```

---

****
