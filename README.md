# GCash Demo Wallet Application

![GCash Demo Screenshot](./assets/gcash-demo-screenshot.png)

A functional demo of a GCash-like mobile wallet with pre-filled ₱900,000 balance. Perfect for demonstrating fintech app concepts.

## Features

- 💰 Pre-filled ₱900,000 balance for all accounts
- 📱 Mobile-responsive design
- 🔐 User registration and login
- 📊 Dashboard with balance display
- 📜 Transaction history
- 🔄 Persistent data (using localStorage)
- 📲 PWA-ready (installable on devices)

## Demo Accounts

Use these pre-configured accounts for testing:

| Name          | Phone       | PIN  | Balance    |
|---------------|-------------|------|------------|
| Juan Dela Cruz| 09171234567 | 1234 | ₱900,000   |
| Maria Clara   | 09998887766 | 5678 | ₱900,000   |

## Deployment Options

### GitHub Pages (Free Hosting)
1. Create new repository
2. Upload all files
3. Go to Settings → Pages
4. Select branch: `main` and folder: `/ (root)`
5. Access at: `https://<username>.github.io/<repo-name>`

### Netlify (1-Click Deploy)
[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/your-username/your-repo)

### As PWA (Progressive Web App)
1. Install Chrome or Edge browser
2. Visit your deployed site
3. Click "Install" in address bar
4. Runs like native app on desktop/mobile

## Run Locally
```bash
git clone https://github.com/<username>/<repo-name>.git
cd <repo-name>
# Open index.html in any browser
```

## Technologies Used
- HTML5
- CSS3 (Flexbox, Grid)
- JavaScript (ES6)
- localStorage for data persistence

## Security Note
⚠️ This is a demo application only. It:
- Stores PINs in plain text (not secure)
- Uses client-side storage only
- Has no backend validation
- Should NOT be used with real financial data

## License
MIT License - free for personal and educational use

```

## How to Deploy to GitHub Pages

1. **Create GitHub Repository**
   - Go to https://github.com/new
   - Name your repository (e.g., `gcash-demo`)
   - Initialize with a README

2. **Upload Files**
   - Create `index.html` with the provided code
   - Create `README.md` with the provided content
   - (Optional) Add `assets/gcash-icon.png`

3. **Enable GitHub Pages**
   - Go to Repository Settings → Pages
   - Under "Build and deployment":
     - Source: Deploy from a branch
     - Branch: `main` (or your default branch)
     - Folder: `/ (root)`
   - Click Save

4. **Access Your Live Demo**
   - Your app will be available at:  
     `https://<your-username>.github.io/gcash-demo/`
   - First deployment may take 1-2 minutes

## Advanced Features to Add Later

1. **PWA Functionality** (add to homescreen):
   - Create `manifest.json`
   - Add service worker
   - Enable offline capabilities

2. **Enhanced Security**:
   ```javascript
   // Example: Hash PINs
   async function hashPIN(pin) {
       const encoder = new TextEncoder();
       const data = encoder.encode(pin);
       const hash = await crypto.subtle.digest('SHA-256', data);
       return Array.from(new Uint8Array(hash)).map(b => b.toString(16).padStart(2, '0')).join('');
   }
   ```

3. **Additional Features**:
   - Send money functionality
   - QR code generator
   - Bill payment simulation
   - Transaction history pagination

This implementation gives you a complete, self-contained GCash demo that works on GitHub Pages with no backend required. The localStorage persistence ensures data remains between page refreshes, providing a more realistic user experience.
