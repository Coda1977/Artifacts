# Claude Artifacts Repository

This folder contains all your Claude artifacts ready for deployment to Vercel.

## Structure

```
claude-artifacts/
├── vercel.json              (Vercel configuration)
├── example-artifact-1/      (Replace with your actual artifacts)
│   └── index.html
├── example-artifact-2/
│   └── index.html
└── README.md               (This file)
```

## How to Add New Artifacts

1. Download artifact code from Claude
2. Create a new folder with a descriptive name (e.g., `leadership-workshop-game`)
3. Paste your artifact code into `index.html` inside that folder
4. Deploy (see below)

**Naming tips:**
- Use lowercase with hyphens: `workshop-tool-1`, `management-sim`
- Avoid spaces or special characters
- The folder name becomes the URL path

## Deployment to Vercel

### Option 1: Direct Upload (Easiest for first time)

1. Go to [vercel.com](https://vercel.com) and sign up/login (free account)
2. Click "Add New" → "Project"
3. Drag and drop this entire `claude-artifacts` folder
4. Click "Deploy"
5. Done! Your artifacts will be at:
   - `your-project.vercel.app/example-artifact-1`
   - `your-project.vercel.app/example-artifact-2`

### Option 2: GitHub Integration (Best for ongoing updates)

1. Create a GitHub repository
2. Upload this folder to GitHub
3. In Vercel, click "Add New" → "Project" → "Import Git Repository"
4. Select your repo and deploy

**Benefits:** Every time you push new artifacts to GitHub, Vercel auto-deploys them!

## How URLs Work

- Each folder becomes a URL path
- Folder `leadership-game/` → `yoursite.vercel.app/leadership-game`
- No index page at root = no way to browse all artifacts
- Only people with direct links can access them

## Adding Artifacts After Deployment

### If using GitHub:
1. Add new folder with artifact code
2. Commit and push to GitHub
3. Vercel automatically deploys

### If using direct upload:
1. Go to your Vercel project dashboard
2. Click "Deployments" → "Upload"
3. Upload updated folder

## For Workshop Use

Share individual URLs with participants:
- `yoursite.vercel.app/workshop-tool-1` - for Tool 1
- `yoursite.vercel.app/management-game` - for Game
- etc.

They cannot navigate back to see your full collection because there's no index page!

## Custom Domain (Optional)

In Vercel project settings, you can:
- Add a custom domain (e.g., `workshops.yourdomain.com`)
- Then URLs become: `workshops.yourdomain.com/artifact-name`

## Notes

- Free tier: Generous limits, perfect for workshop artifacts
- Deployment time: Usually 30-60 seconds
- Updates: Push changes and they go live immediately
- No index.html at root = no homepage = no discovery

## Next Steps

1. Replace example-artifact-1 and example-artifact-2 with your actual Claude artifacts
2. Deploy to Vercel
3. Share individual URLs with workshop participants
4. Add more artifacts as needed!
