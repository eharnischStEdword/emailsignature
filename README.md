# Email Signature Generator

A simple, client-side email signature generator for St. Edward Church & School.

## Setup

1. Clone this repository
2. Edit `index.html` and update the `CONFIG` object near the bottom of the file:
   - `logoUrl`: URL to your logo image
   - `orgName`: Organization name
   - `address`: Street address
   - `cityStateZip`: City, State ZIP
   - `website`: Display URL
   - `websiteUrl`: Full URL with https://
   - `primaryColor`: Hex color for branding
   - `facebook`, `twitter`, `instagram`: Social media URLs (leave empty to hide)

3. Deploy to Render.com as a Static Site, or any other static hosting

## Customization

### Adding/Removing Form Fields

Edit the HTML form in the left card, then update the corresponding JavaScript:
- Add input to the `inputs` object
- Update `generateSignatureHTML()` and `generatePlainText()` functions

### Changing Departments

Edit the `<select id="department">` dropdown options in the HTML.

### Styling

CSS variables at the top of the `<style>` block control the main colors of the generator interface (not the signature itself).

## Deployment on Render.com

1. Push to GitHub
2. Go to render.com and create a new Static Site
3. Connect your GitHub repo
4. Set build command to empty (or just leave it)
5. Set publish directory to `.` (root)
6. Deploy

## Files

- `index.html` - The entire application (self-contained)

## Browser Support

Works in all modern browsers. The copy-to-clipboard feature uses the modern Clipboard API with fallback for older browsers.
