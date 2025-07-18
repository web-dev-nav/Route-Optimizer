# Route Optimizer

A web-based route optimization tool designed for service professionals, delivery personnel, and field technicians to efficiently plan their daily routes across Canada.

## 🎯 Purpose

The Route Optimizer helps service professionals and delivery personnel minimize travel time and distance when visiting multiple locations across Canada. By calculating the most efficient route between stops, users can:

- **Save Time**: Reduce total travel time between locations
- **Save Fuel**: Minimize driving distance with optimized routing
- **Increase Productivity**: Complete more deliveries or service calls per day
- **Improve Service**: Provide more accurate arrival time estimates

## 🚀 Features

### 📍 Location Services
- **Current Location Detection**: Automatically detect and use your current GPS location as starting point
- **Canadian Address Validation**: Restricts addresses to Canadian locations only
- **Google Places Autocomplete**: Smart address suggestions as you type
- **Multiple Travel Modes**: Support for driving, walking, and bicycling routes

### 🗺️ Route Optimization
- **Intelligent Routing**: Uses Google's Distance Matrix API to calculate optimal visit order
- **Visual Map Display**: Interactive Google Maps showing your optimized route
- **Real-time Directions**: Turn-by-turn directions for each leg of your journey
- **Distance & Duration**: Shows travel time and distance between each stop

### 🎥 User Support
- **Tutorial Video**: Built-in video tutorial explaining how to use the application
- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Clean Interface**: Simple, intuitive design focused on ease of use

## 🛠️ Technical Specifications

### Technologies Used
- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Styling**: TailwindCSS framework
- **Maps**: Google Maps JavaScript API
- **Services**: Google Places API, Distance Matrix API, Directions API
- **Responsive**: Mobile-first responsive design

### Browser Requirements
- Modern web browser with JavaScript enabled
- Internet connection for map services
- Location services permission (optional, for current location feature)

## 📋 How It Works

### Step 1: Set Your Starting Location
- Enter your starting address manually, or
- Click "Use Current Location" to automatically detect your position
- Only Canadian addresses are accepted

### Step 2: Add Destination Addresses
- Enter destination addresses using the autocomplete-enabled input fields
- Add multiple destinations using the "Add Customer" button
- Remove destinations by clicking the ✖ button next to their address
- All addresses are validated to ensure they're in Canada

### Step 3: Choose Travel Mode
- **Driving**: For vehicle-based service calls (default)
- **Walking**: For dense urban areas or short distances
- **Bicycling**: For eco-friendly or traffic-heavy areas

### Step 4: Optimize Your Route
- Click "Optimize Route" to calculate the most efficient path
- The system analyzes distances between all locations
- Uses nearest-neighbor algorithm for optimal stop ordering

### Step 5: Follow Your Route
- View the optimized route on the interactive map
- See detailed stop-by-stop directions
- Note travel time and distance for each leg
- Follow turn-by-turn directions to each destination

## 🔧 Setup Instructions

### Prerequisites
- Web server (Apache, Nginx, or simple HTTP server)
- Google Maps API key with the following APIs enabled:
  - Maps JavaScript API
  - Places API
  - Distance Matrix API
  - Directions API

### Installation

1. **Download the files**
   ```bash
   # Download or clone the project files
   # Ensure index.html is in your web server directory
   ```

2. **Configure Google Maps API**
   - Get a Google Maps API key from [Google Cloud Console](https://console.cloud.google.com/)
   - Enable required APIs (Maps JavaScript, Places, Distance Matrix, Directions)
   - Replace the API key in index.html:
   ```html
   <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&libraries=places"></script>
   ```

3. **Deploy to Web Server**
   ```bash
   # Copy files to your web server document root
   cp index.html /var/www/html/
   # Or serve locally for development
   python -m http.server 8000
   ```

4. **Access the Application**
   - Open your web browser
   - Navigate to your server URL or `http://localhost:8000`
   - Grant location permissions when prompted (optional)

### Configuration Options

**API Key Security**: For production use, implement server-side API key management and domain restrictions in Google Cloud Console.

**Geographic Restrictions**: The application is pre-configured for Canada. To modify for other countries, update the `componentRestrictions` in the code:
```javascript
componentRestrictions: { country: "ca" } // Change "ca" to your country code
```

## 🎯 Target Users

- **Delivery Personnel**: Package and parcel delivery drivers
- **Service Technicians**: Computer repair, appliance repair, HVAC technicians
- **Field Sales Representatives**: Multi-location sales visits
- **Healthcare Workers**: Home care nurses, mobile medical services
- **Small Business Owners**: Any business requiring multi-stop routing
- **Independent Contractors**: Freelance service providers

## 🌍 Regional Focus

This application is specifically designed for Canadian markets:
- Address validation restricted to Canadian postal codes
- Map centered on Canada by default
- Optimized for Canadian geography and address formats
- All distance calculations in metric system

## 📞 Support & Contact

For suggestions, improvements, or technical support:
- **Developer**: Navjot
- **Email**: web.dev.nav@gmail.com
- **Year**: 2024

## 📄 License

© 2024 Route Optimizer. All Rights Reserved.

## 🚨 Important Notes

1. **API Costs**: Google Maps API usage may incur charges based on usage volume
2. **Internet Required**: Application requires internet connection for map services
3. **Privacy**: Location data is processed by Google Maps services
4. **Accuracy**: Route optimization is based on road distances, not aerial distances
5. **Canada Only**: Currently restricted to Canadian addresses only

## 🔄 Future Enhancements

Potential improvements for future versions:
- Offline map caching
- Route export to GPS devices
- Customer appointment scheduling integration
- Multi-day route planning
- Service time estimation per stop
- Route sharing with team members
- Integration with delivery management systems
- Package tracking and delivery confirmation
