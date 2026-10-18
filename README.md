# My First Google Map

A simple web page that embeds an interactive Google Map using the **Google Maps JavaScript API**. The map loads centered on London and can be zoomed and dragged like any Google Map.

## Features

- Interactive Google Map embedded in a plain HTML page
- Map centered on London (51.508742, -0.120850) at zoom level 5
- Lightweight: a single HTML file, no frameworks or build tools

## Tech Stack

- HTML5
- JavaScript
- [Google Maps JavaScript API](https://developers.google.com/maps/documentation/javascript)

## Getting Started

### Prerequisites

- A modern web browser
- A Google Maps API key ([how to get one](https://developers.google.com/maps/documentation/javascript/get-api-key))

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   cd <your-repo-name>
   ```
2. Open `map.html` in a text editor and replace `YOUR_API_KEY` in the script tag with your own key:
   ```html
   <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=myMap"></script>
   ```
3. Open `map.html` in your browser. The map should appear below the heading.

## How It Works

The `myMap()` function runs as the API's callback once the library has loaded. It sets the map's center and zoom, then creates a `google.maps.Map` inside the `#googleMap` div.

```js
function myMap() {
  var mapProp = {
    center: new google.maps.LatLng(51.508742, -0.120850),
    zoom: 5,
  };
  var map = new google.maps.Map(document.getElementById("googleMap"), mapProp);
}
```

To show a different place, change the latitude and longitude in `LatLng(...)`. A higher `zoom` value zooms in closer.

## Project Structure

```
.
├── map.html    # Page, styles, and map script
└── README.md
```

## Security Note

Never commit a real API key to a public repository. In the Google Cloud Console, restrict your key to specific HTTP referrers (for example, your GitHub Pages URL) and to the Maps JavaScript API only.

## Future Improvements

- Add markers and info windows
- Let users search for places
- Use the browser's geolocation to center the map on the user

## Author

**Kajal Baraiya**
Aspiring software developer from Surat, Gujarat, India, working with HTML, CSS, JavaScript, React, Node.js, Python, and Java.

- GitHub: [@kajalbaraiya](https://github.com/kajalbaraiya)
- LinkedIn: [kajal-baraiya-761862419](https://www.linkedin.com/in/kajal-baraiya-761862419)
- Email: kajalbaraiya2052007@gmail.com

## License

This project is open source and available under the [MIT License](LICENSE).
