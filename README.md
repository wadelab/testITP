# Orca Sightings Map 🐋

An interactive web-based interface that displays recent Orca (killer whale) sightings on a world map using data from the iNaturalist database.

## Features

- **Interactive Map**: Pan and zoom to explore Orca sightings around the world
- **Real-time Data**: Fetches recent observations from iNaturalist API
- **Detailed Information**: Click on any marker to view:
  - Observation date
  - Location details
  - Observer information
  - Photos (when available)
  - Quality grade and identifications count
  - Direct link to the observation on iNaturalist
- **Customizable Results**: Adjust the number of sightings to display (10-200)
- **Responsive Design**: Works on desktop and mobile devices

## How to Use

1. **Open the Application**:
   - Simply open `index.html` in a web browser
   - Or serve it using a local web server

2. **View Sightings**:
   - The map loads automatically with recent Orca sightings
   - Each marker (🐋) represents an observation

3. **Interact with Markers**:
   - Click on any marker to see detailed information
   - Click the "View on iNaturalist" link to see the full observation

4. **Navigate the Map**:
   - **Zoom**: Use mouse wheel or +/- buttons
   - **Pan**: Click and drag the map
   - **Reset**: Click the refresh button to reload data

5. **Adjust Settings**:
   - Change the "Results" number to load more or fewer sightings
   - Click "🔄 Refresh Data" to reload with new settings

## Technical Details

### Technologies Used
- **Leaflet.js**: Interactive mapping library
- **iNaturalist API**: Source of Orca observation data
- **OpenStreetMap**: Map tile provider
- **HTML/CSS/JavaScript**: Pure vanilla implementation (no frameworks)

### API Information
- **Data Source**: iNaturalist API v1
- **Species**: Orcinus orca (Taxon ID: 47664)
- **Data Quality**: Research grade and needs ID observations
- **Geolocation**: Only observations with GPS coordinates

### Browser Compatibility
- Chrome, Firefox, Safari, Edge (modern versions)
- Requires JavaScript enabled
- Internet connection required to load map tiles and data

## Local Development

To run locally:

```bash
# Option 1: Python
python -m http.server 8000

# Option 2: Node.js
npx http-server

# Then open http://localhost:8000
```

Or simply open `index.html` directly in your browser.

## License

This project uses data from iNaturalist under their terms of service.