# Etonuge - Herbal Quality Assessment

A modern, responsive website for Etonuge, an AI-powered electronic tongue system for herbal quality testing. This is a static website built with HTML, CSS, and vanilla JavaScript.

## Features

- **Responsive Design**: Works on all device sizes
- **Interactive Demo**: Simulated AI analysis of herbal samples
- **Dashboard**: Overview of test results and statistics
- **Modern UI**: Clean, professional interface with smooth animations
- **No Dependencies**: Built with vanilla JavaScript (no frameworks)

## Project Structure

```
etonuge_website/
├── css/
│   └── styles.css         # All CSS styles
├── js/
│   └── script.js          # JavaScript functionality
├── images/               # Image assets
├── index.html            # Landing page
├── dashboard.html        # Dashboard page
└── README.md             # This file
```

## Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, or Edge)
- No server required - runs directly in the browser

### Installation

1. Clone or download this repository
2. Open `index.html` in your web browser

## How to Use

### Home Page
- The home page provides an overview of the Etonuge project
- Use the navigation menu to explore different sections
- Try the interactive demo to see how the analysis works

### Demo
1. Click on the upload area or drag and drop a file
2. Supported formats: CSV, XLSX, XLS
3. Click "Run Analysis" to see the simulated results

### Dashboard
- View test statistics and results
- Navigate through different sections using the sidebar
- The dashboard is fully responsive and works on mobile devices

## Customization

### Colors

You can customize the color scheme by modifying the CSS variables in `css/styles.css`:

```css
:root {
    --primary-color: #2e7d32;    /* Main brand color */
    --primary-light: #60ad5e;   /* Lighter shade */
    --primary-dark: #005005;    /* Darker shade */
    --secondary-color: #ff8f00; /* Accent color */
    /* ... other variables ... */
}
```

### Fonts

The website uses Google Fonts (Inter) by default. You can change this in the `<head>` section of the HTML files:

```html
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
```

## Future Integration

To connect this frontend to a real backend API, you'll need to:

1. Set up an API endpoint for file uploads and analysis
2. Update the `analyzeBtn` click handler in `script.js` to make a real API call:

```javascript
// Example API call (replace with your actual endpoint)
async function analyzeSample(file) {
    const formData = new FormData();
    formData.append('sample', file);
    
    try {
        const response = await fetch('https://your-api-endpoint.com/analyze', {
            method: 'POST',
            body: formData
        });
        
        const data = await response.json();
        return data;
    } catch (error) {
        console.error('Error analyzing sample:', error);
        throw error;
    }
}
```

## Browser Support

The website is compatible with all modern browsers including:
- Google Chrome (latest)
- Mozilla Firefox (latest)
- Safari (latest)
- Microsoft Edge (latest)

## License

This project is open source and available under the [MIT License](LICENSE).

## Contact

For any questions or feedback, please contact [Your Email].

---

*This is a static website template. Backend integration is required for full functionality.*
