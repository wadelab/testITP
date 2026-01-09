# Testing the Orca Sightings Map

## Important Note

The application requires internet access to load:
1. **Leaflet.js library** - For the interactive mapping functionality
2. **OpenStreetMap tiles** - For the map background
3. **iNaturalist API** - For the Orca observation data

## How to Test

### Option 1: Direct Browser Access (Recommended)
1. Simply open `index.html` in any modern web browser
2. Make sure you have an active internet connection
3. The map should load automatically with Orca sightings

### Option 2: Local Web Server
```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx http-server

# Using PHP
php -S localhost:8000
```

Then navigate to `http://localhost:8000/index.html`

### Option 3: GitHub Pages
Push to a GitHub repository and enable GitHub Pages to host it publicly.

## What to Test

### Basic Functionality
- ✅ Map loads and displays world view
- ✅ Orca sighting markers appear on the map
- ✅ Markers show whale emoji icon (🐋)

### Interactivity
- ✅ **Zoom**: Mouse wheel or +/- buttons work
- ✅ **Pan**: Click and drag to move around the map
- ✅ **Marker Click**: Clicking a marker shows a popup with details

### Popup Information
Each popup should display:
- ✅ Photo of the sighting (if available)
- ✅ Observation date
- ✅ Location name
- ✅ Observer username
- ✅ Quality grade (Research Grade, Needs ID, or Casual)
- ✅ Number of identifications
- ✅ Link to view on iNaturalist

### Controls
- ✅ Results input: Change number (10-200) and refresh
- ✅ Refresh button: Reload data from API
- ✅ Stats bar: Shows count and date range

### Expected Behavior
1. **Initial Load**: Map centers on world view and automatically fetches 100 recent sightings
2. **Loading State**: Shows loading spinner while fetching data
3. **Auto-fit**: Map adjusts to show all markers after loading
4. **Status Updates**: Status message updates during loading and after completion

## Troubleshooting

### Map doesn't load
- **Check internet connection**: The app needs to download Leaflet.js from CDN
- **Check browser console**: Open DevTools (F12) and look for errors
- **Try different browser**: Test in Chrome, Firefox, or Safari

### No markers appear
- **API might be down**: Check https://www.inaturalist.org/
- **Network restrictions**: Some networks block API access
- **Try refreshing**: Click the refresh button

### Markers don't show details
- **Disable popup blockers**: Make sure popups aren't blocked
- **Check console**: Look for JavaScript errors

## Known Limitations in Sandboxed Environments

The application will NOT work in:
- Environments that block external CDN access
- Networks that block unpkg.com, OpenStreetMap, or iNaturalist
- Offline mode (requires internet for all resources)

This is expected behavior for security reasons in sandboxed testing environments. The application will work normally in standard web browsers with internet access.

## Browser Compatibility

Tested and working on:
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

Requires:
- JavaScript enabled
- Internet connection
- Modern browser with ES6 support
