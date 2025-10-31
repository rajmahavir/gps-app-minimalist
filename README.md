# GPS Watermark Batch Processor

A professional, browser-based tool for batch processing images with GPS watermarks and location data overlays.

## Features

- **Batch Processing**: Process multiple images simultaneously with GPS data from Excel
- **Custom Overlays**: Add map overlays to images
- **Flexible Output**: Multiple size options (1280×960, 1920×1080, 1920×1440, or original)
- **Export Options**: Download as ZIP or PowerPoint presentation
- **Customizable Naming**: Multiple file naming patterns including date-based naming
- **No Installation Required**: Runs entirely in your browser - no server needed

## How to Use

### 1. Prepare Your Files

**Excel File Requirements:**
- Should contain columns: `datetime` and `Time`
- DateTime values should be in Excel date format
- One row per image to be processed

**Images:**
- Any standard image format (JPG, PNG, etc.)
- Multiple images can be uploaded at once

**Map Overlay:**
- A semi-transparent map image to overlay on photos
- Should match your desired output dimensions

### 2. Upload Files

1. **Step 1**: Upload your Excel file with GPS data
2. **Step 2**: Upload all images to process
3. **Step 3**: Upload the map overlay image

### 3. Configure Settings

- **Output Size**: Choose from preset sizes or keep original dimensions
- **Crop Mode**:
  - **Cover**: Fills the entire frame, crops excess (no bars)
  - **Contain**: Fits entire image, adds bars if needed
- **Image Quality**: 1-100 (higher = better quality, larger file)
- **File Naming**: Choose from preset patterns or create custom prefix
- **Location Data**: Customize location text, address, and coordinates

### 4. Process & Download

Click "Process Images" and wait for completion. Then:
- **Download ZIP**: All processed images in a compressed file
- **Download PowerPoint**: Images formatted as presentation slides

## Browser Compatibility

This application requires a modern browser with support for:
- HTML5 Canvas API
- File API and FileReader
- ES6+ JavaScript

### Recommended Browsers:
- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+

## Technical Details

### Dependencies (Loaded from CDN)
- **xlsx.js** (v0.18.5) - Excel file parsing
- **jszip.js** (v3.10.1) - ZIP file generation
- **pptxgenjs** (v3.12.0) - PowerPoint generation

### Privacy & Security
- **100% Client-Side**: All processing happens in your browser
- **No Data Upload**: Your files never leave your computer
- **No Tracking**: No analytics or tracking scripts

## Deployment

### Option 1: Simple Hosting
Upload `gps-app-minimalist.html` to any web hosting service:
- GitHub Pages
- Netlify
- Vercel
- Any static hosting provider

### Option 2: Local Use
Simply open the HTML file directly in your browser - no server required!

### Option 3: GitHub Pages Quick Deploy

```bash
# Clone the repository
git clone <your-repo-url>
cd gps-app-minimalist

# Enable GitHub Pages in your repository settings
# Point it to the main branch, root directory
```

Your app will be available at: `https://<username>.github.io/<repo-name>/gps-app-minimalist.html`

## Customization

### Changing Default Location Text
Edit lines 573-581 in the HTML file:

```javascript
<input type="text" id="locationText" value="Your City, State, Country">
<input type="text" id="addressText" value="Your Address Here">
<input type="text" id="coordinatesText" value="Lat XX.XXXX° Long YY.YYYY°">
```

### Adjusting Watermark Position
Modify the coordinates in the `addWatermarkText()` function (lines 1008-1034).

### Changing Colors/Styling
All styles are in the `<style>` block (lines 10-460). Key color variables:
- Primary blue: `#4299e1`
- Success green: `#48bb78`
- Background: `#f5f7fa`

## File Structure

```
gps-app-minimalist/
├── gps-app-minimalist.html    # Main application file
└── README.md                   # This file
```

## Troubleshooting

### Images not processing?
- Ensure Excel file has `datetime` and `Time` columns
- Check that image files are valid image formats
- Verify browser console for specific errors

### Overlay not showing?
- Make sure overlay image uploaded successfully
- Check that overlay has some transparency for visibility

### Download not working?
- Check browser's download settings
- Ensure pop-ups are allowed for the site
- Try a different browser if issues persist

## Performance Notes

- Processing time depends on:
  - Number of images
  - Image resolution
  - Selected output quality
  - Computer performance

- For large batches (100+ images):
  - Consider processing in smaller groups
  - Use lower quality settings if file size not critical
  - Close other browser tabs to free memory

## License

This project is open source. Feel free to use, modify, and distribute.

## Support

For issues or questions:
1. Check the Troubleshooting section above
2. Review browser console for error messages
3. Ensure all file requirements are met
4. Try with a smaller test batch first

## Credits

Built with:
- Vanilla JavaScript
- HTML5 Canvas API
- SheetJS Community Edition
- JSZip
- PptxGenJS

---

**Version**: 1.0
**Last Updated**: October 2025
