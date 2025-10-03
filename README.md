# Attendance Analytics Dashboard

A responsive web application that helps students track and analyze their academic attendance data from ERP systems. Calculate your attendance percentage, get insights on eligibility, and receive recommendations for maintaining the required 80% threshold.

## Features

- **Real-time Analysis**: Paste attendance data directly from your ERP portal for instant insights
- **Smart Calculations**: Accurate attendance percentage calculations with eligibility status
- **Laboratory Support**: Special handling for lab sessions with multi-point attendance systems
- **Actionable Recommendations**: Get specific guidance on how many classes you need to attend or can miss
- **Visual Analytics**: Interactive charts and progress indicators for easy understanding
- **Subject-wise Breakdown**: Detailed analysis for each subject component (Theory, Practical, Tutorial)
- **Dark Mode**: Toggle between light and dark themes for comfortable viewing
- **Export Reports**: Download your attendance analysis as a text report
- **Fully Responsive**: Works seamlessly on desktop, tablet, and mobile devices

## Technologies Used

- HTML5
- CSS3 (Custom properties, Grid, Flexbox)
- JavaScript (ES6+)
- Chart.js for data visualization

## Getting Started

### Prerequisites

No installation required. Just a modern web browser.

### Usage

1. Clone or download this repository
2. Open `index.html` in your web browser
3. Click "How to Use This Tool" for detailed instructions
4. Copy your attendance table from your ERP portal
5. Paste it into the text area
6. Click "Analyze Attendance" to view your results

### File Structure

```
attendance-analytics-dashboard/
├── index.html          # Main HTML structure
├── styles.css          # Styling and responsive design
├── script.js           # Application logic and calculations
└── README.md          # Documentation
```

## How It Works

The application parses attendance data in the standard ERP format:

```
SrNo    Subject    Subject Type    Present    Total Period    Percentage (%)
1       Subject Name    TH         20         25              80.00
```

It then:
1. Calculates overall and category-wise attendance percentages
2. Identifies subjects below the 80% threshold
3. Provides specific recommendations for each subject
4. Displays visual analytics through charts and progress indicators
5. Handles laboratory sessions with point-based attendance systems

## Laboratory Attendance

The system supports special calculations for laboratory subjects where attendance is tracked in points rather than sessions. For example, if a lab awards 3 points per session, recommendations will be given in terms of lab sessions rather than individual points.

## Browser Compatibility

- Chrome (recommended)
- Firefox
- Safari
- Edge
- Opera

## Customization

### Adding Laboratory Subjects

To add support for additional laboratory subjects with point multipliers, edit the `labMultipliers` object in `script.js`:

```javascript
this.labMultipliers = {
    'Your Lab Name': 3,  // 3 points per session
    'Another Lab': 2,    // 2 points per session
};
```

### Changing Theme Colors

Modify CSS custom properties in `styles.css`:

```css
:root {
    --primary-color: #5b64e5;
    --success-color: #0ea574;
    --warning-color: #e89c0b;
    --danger-color: #dc3545;
}
```

## Privacy

All data processing happens locally in your browser. No attendance data is sent to any server or stored anywhere. When you close the browser, all data is cleared.

## Contributing

Contributions are welcome. If you find bugs or have feature suggestions, please open an issue or submit a pull request.

## License

This project is open source and available under the MIT License.

## Author

Developed by [Sujal Sokande](https://www.linkedin.com/in/sujal-sokande-1028a62b1/)

## Acknowledgments

- Chart.js for visualization capabilities
- Inter font family by Rasmus Andersson
- Inspired by the need for better attendance tracking tools for students

## Disclaimer

This tool is designed to help students track their attendance. Always verify important attendance information with your institution's official records. The developer is not responsible for any discrepancies or actions taken based on the analysis provided by this tool.
