# Email Signature Generator

A client-side email signature generator for St. Edward Church & School staff.

## Features

- Church/School toggle (auto-switches phone, fax, and address)
- Clergy titles (Fr., Dcn., Msgr., Sr., Br.) plus standard honorifics
- Optional credentials field
- Extension field for direct lines
- Auto-includes both websites and social media links
- Copy to clipboard or download HTML file
- Live preview

## Deployment on Render.com

1. Push to GitHub
2. Go to render.com and create a new Static Site
3. Connect your GitHub repo
4. Build command: leave empty
5. Publish directory: `.`
6. Deploy

## Configuration

The `CONFIG` object in the JavaScript section contains:

- Logo URL
- Phone numbers, addresses, fax for Church and School
- Website URLs
- Social media links
- Brand colors

To change any of these, edit the CONFIG object near line 280 in `index.html`.

## Customization

### Adding Titles/Honorifics

Edit the `<select id="honorific">` dropdown in the HTML.

### Changing Colors

CSS variables at the top of the `<style>` block:
- `--navy`: #003764
- `--dark-green`: #005921
- `--green`: #00843d
- `--gold`: #daaa00
- `--off-white`: #eef4f1

### Social Icons

Social icons are embedded as base64 SVGs in St. Edward green (#005921) for email client compatibility. The source SVG files are also in this repo:
- `facebook-svgrepo-com.svg`
- `instagram-svgrepo-com.svg`
- `youtube-168-svgrepo-com.svg`

To change them, update the `SOCIAL_ICONS` object in the JavaScript.

## Browser Support

Works in all modern browsers. Uses Clipboard API with fallback for older browsers.
