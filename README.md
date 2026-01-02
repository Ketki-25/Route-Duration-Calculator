# Route Duration Calculator

A simple, offline-capable web tool for calculating work hours from Excel timesheets. Groups data by route and calculates total duration from first to last timestamp.

## 📖 Background Story

I work at a snow removal company where we manage multiple routes across the city. Each route has multiple workers, and tracking the total time spent on each route was becoming a time-consuming manual task. Our team was spending hours each week manually processing Excel timesheets to calculate route durations.

I noticed my colleagues were struggling with this repetitive work, so I decided to build a solution. Using Claude AI as my coding assistant, I developed this browser-based calculator that automates the entire process. What used to take hours now takes seconds - just drag, drop, and download.

The tool groups all timestamps by route, finds the first and last activity time, and calculates the duration automatically. It's been a huge time-saver for our operations team, and I'm sharing it here hoping it helps others facing similar challenges.

**Built with:** HTML, JavaScript, and the SheetJS library  
**Development assistant:** Claude AI (Anthropic)  
**Created to:** Save my colleagues' time and reduce manual data processing

## ✨ Features

- **100% Browser-based** - No server required, works completely offline
- **Drag & Drop Support** - Easy file upload interface
- **Route-based Grouping** - Combines all users working on the same route
- **Excel Export** - Download processed results as Excel file
- **Cross-platform** - Works on Windows, Mac, Linux
- **No Installation** - Just open the HTML file and start using

## 📋 Requirements

- Modern web browser (Chrome, Firefox, Safari, Edge)
- Excel file (.xlsx or .xls) with the following columns:
  - `Date` - Work date
  - `Time` - Timestamp
  - `Route Name` - Route identifier
  - `Visit (Service)` - Optional service type

## 🚀 Usage

1. Download `route-duration-calculator.html`
2. Double-click to open in your browser
3. Drag and drop your Excel file or click to browse
4. View results in the table
5. Download processed data as Excel

## 📊 What It Does

The calculator:
1. Reads your Excel timesheet
2. Groups entries by **Route Name**
3. Finds the **earliest** and **latest** timestamp for each route
4. Calculates: `Total Duration = Last Timestamp - First Timestamp`
5. Displays results sorted A→Z by route name

### Example

**Input:**
```
Date       | Time     | Route Name | User
2025-12-10 | 08:00:00 | Route A    | John
2025-12-10 | 09:30:00 | Route A    | Jane
2025-12-10 | 17:00:00 | Route A    | John
```

**Output:**
```
Date       | Route Name | Total Duration in Hrs
2025-12-10 | Route A    | 9.00
```
(17:00:00 - 08:00:00 = 9 hours)

## 🔧 Supported Date/Time Formats

**Dates:**
- Excel serial numbers (45998, 45999)
- YYYY-MM-DD (2025-12-10)
- MM-DD-YYYY (12-10-2025)
- DD-MM-YYYY (10-12-2025)
- M/D/YY (12/10/25)

**Times:**
- Excel time fractions (0.5 = 12:00 PM)
- HH:MM:SS (14:30:00)
- HH:MM (14:30)
- 24-hour format

## 🎨 Features

- Clean, modern UI with green color scheme
- Responsive design (works on mobile)
- Real-time statistics (total entries, unique routes, total hours)
- Compact table layout with minimal spacing
- Visual feedback during file processing

## 🔒 Privacy

- All processing happens in your browser
- No data is sent to any server
- Files are never uploaded anywhere
- Works completely offline after first load

## 📝 License

MIT License - Feel free to use and modify

## 🤝 Contributing

Contributions welcome! Feel free to:
- Report bugs
- Suggest features
- Submit pull requests

## 💡 Tips

- For best results, ensure your Excel file has consistent date/time formats
- The tool ignores the "Duration" column if present - it calculates fresh from timestamps
- Multiple users on the same route are automatically combined
- Results are always sorted alphabetically by route name

## 🏢 Use Cases

Originally built for snow removal operations, but works for any route-based work:
- **Snow Removal Companies** - Track time per snow route
- **Delivery Services** - Calculate route durations for logistics
- **Field Services** - Monitor service route efficiency
- **Maintenance Crews** - Track work hours by location/route
- **Any Route-Based Operations** - Where multiple workers share routes

## 🛠️ How It Was Built

This tool was created using:
- **Claude AI (Anthropic)** for development assistance
- **SheetJS** library for Excel file processing
- **Vanilla JavaScript** for maximum compatibility
- **No frameworks** - just clean HTML/CSS/JS
- **Offline-first design** - works without internet after initial load

The entire calculator is a single HTML file, making it easy to deploy and use anywhere.

## ⚠️ Browser Compatibility

Tested and working on:
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

---

**Built to streamline route-based operations and save valuable time**

*Developed for the snow removal industry, applicable to any route-based workflow.*
