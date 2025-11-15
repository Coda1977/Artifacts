# Claude Artifacts Repository - Single Page Version

Your personal dashboard for managing and sharing workshop artifacts with QR codes - all in one HTML file!

## 🎯 How It Works

- **Main Dashboard**: `yoursite.vercel.app` - YOUR private page with all artifacts and QR codes
- **Artifact URLs**: `yoursite.vercel.app#artifact-name` - Shareable pages (note the `#`)
- **Security**: Artifacts don't link back to dashboard, visitors can't discover your collection
- **Super Easy**: Add/edit artifacts directly in the browser - no folders needed!

## ✨ Key Features

- ✅ Add artifacts directly in the dashboard (paste code, click save)
- ✅ Edit artifacts anytime
- ✅ Delete artifacts with one click
- ✅ Automatic QR code generation
- ✅ Copy URLs with one click
- ✅ All data stored in browser (localStorage)
- ✅ Single HTML file - easy to deploy

## 🚀 Quick Start

### 1. Deploy to Vercel

1. Go to [vercel.com](https://vercel.com) and sign up (free)
2. Click "Add New" → "Project"
3. Drag ONLY the `index.html` file to Vercel (you can delete the old folders)
4. Click "Deploy"

### 2. Add Your First Artifact

1. Visit `your-project.vercel.app`
2. Click "Add New Artifact"
3. Fill in:
   - **Name**: Leadership Workshop Game
   - **Description**: Interactive tool for exploring leadership styles
   - **Code**: Paste your Claude artifact code
4. Click "Save Artifact"
5. Done! Your artifact is now at `your-project.vercel.app#leadership-workshop-game-123456`

## 📱 Using in Workshops

### For You (Dashboard):
Visit: `yoursite.vercel.app`
- See all artifacts
- View QR codes
- Copy URLs
- Edit/delete artifacts

### For Participants:
Share: `yoursite.vercel.app#artifact-name`
- They see ONLY that specific artifact
- No way to navigate back to your dashboard
- Can't discover other artifacts

### Sharing Methods:

**1. Direct Link**
Copy the URL from the dashboard and share it

**2. QR Code**
- Right-click the QR code on your dashboard
- Save image
- Print or include in presentations

**3. Shortened URL** (optional)
Use a URL shortener:
- `yoursite.vercel.app#leadership-game-123` → `bit.ly/workshop23`

## 🔄 Managing Artifacts

### Add New Artifact
1. Click "Add New Artifact"
2. Enter name, description, and code
3. Save

### Edit Artifact
1. Click the ✏️ icon on any artifact card
2. Modify as needed
3. Save

### Delete Artifact
1. Click the 🗑️ icon on any artifact card
2. Confirm deletion
3. Done

## 💾 Data Storage

- Artifacts stored in **browser localStorage**
- Data persists across sessions
- No database needed
- **Important**: Data is per-browser
  - If you use different browsers/devices, you'll need to add artifacts to each
  - Consider bookmarking your deployment URL

## 🔧 Technical Details

### URL Format
- Dashboard: `yoursite.vercel.app`
- Artifacts: `yoursite.vercel.app#artifact-id`
- The `#` makes it a hash URL (client-side routing)

### Browser Compatibility
- Works in all modern browsers
- Requires JavaScript enabled
- QR codes generated using qrcode.js

### File Structure
Everything is in one `index.html` file:
- Dashboard view
- Artifact renderer
- Add/edit modal
- All JavaScript
- All CSS

## 🎨 Customization

### Change Colors
Edit the CSS gradient (line 13):
```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

### Change Title
Edit the HTML (line 323):
```html
<h1>🎨 My Artifacts Dashboard</h1>
```

## ⚠️ Important Notes

### Limitations
- Hash URLs include `#` instead of `/` (e.g., `site.com#artifact` not `site.com/artifact`)
- Data is stored in browser (if you clear browser data, artifacts are deleted)
- Single-page app (all artifacts load client-side)

### Backup Your Data
To backup your artifacts:
1. Open browser console (F12)
2. Type: `console.log(localStorage.getItem('artifacts'))`
3. Copy the output
4. Save to a text file

To restore:
1. Open browser console
2. Type: `localStorage.setItem('artifacts', 'PASTE_YOUR_DATA_HERE')`
3. Refresh page

## 🔐 Security

### How Your Dashboard Stays Private
- No links from artifact pages to dashboard
- Visitors need to guess the exact root URL
- Only share artifact hash URLs (with `#`)
- Don't share your root domain

### What Visitors Can/Cannot Do

✅ Visitors CAN:
- View individual artifacts via hash URL
- Use the artifact interactively
- Share the artifact URL with others

❌ Visitors CANNOT:
- Navigate to your dashboard
- See list of other artifacts
- Edit or delete artifacts
- Access dashboard without knowing the root URL

## 📋 Old Folders

The old folder-based structure (`example-artifact-1`, `example-artifact-2`, etc.) is no longer needed. You can delete those folders. Everything is now managed through the single `index.html` file.

## 🆘 Troubleshooting

**Artifacts not saving:**
- Check if JavaScript is enabled
- Try a different browser
- Check browser console for errors

**QR code not generating:**
- Requires internet connection (loads qrcode.js from CDN)
- Check browser console for errors

**Lost my artifacts:**
- Data is in browser localStorage
- Clearing browser data deletes artifacts
- Use backup method above

**Someone found my dashboard:**
- Make sure artifact code doesn't include links to root
- Only share hash URLs (with `#`)
- Consider using a custom domain with obscure name

## 🎉 Getting Started

1. Deploy `index.html` to Vercel
2. Visit your site
3. Click "Add New Artifact"
4. Paste your Claude artifact code
5. Get shareable URL with QR code
6. Share with workshop participants!

That's it! No folders, no complex setup, just paste and share. 🚀
