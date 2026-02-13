# AgriSarthi AI - Setup & Deployment Guide

## 🚀 Quick Start

### Development Setup

1. **Install dependencies**
   ```bash
   npm install
   # or
   pnpm install
   ```

2. **Start development server**
   ```bash
   npm run dev
   ```

3. **Open in browser**
   ```
   http://localhost:5173
   ```

## 📦 Production Build

```bash
npm run build
```

The production build will be in the `dist/` folder.

## 🌐 Deployment Options

### Option 1: Netlify (Recommended)

1. Push code to GitHub
2. Connect GitHub repo to Netlify
3. Build command: `npm run build`
4. Publish directory: `dist`
5. Deploy!

### Option 2: Vercel

1. Install Vercel CLI
   ```bash
   npm i -g vercel
   ```

2. Deploy
   ```bash
   vercel
   ```

### Option 3: GitHub Pages

1. Install gh-pages
   ```bash
   npm install -D gh-pages
   ```

2. Add to package.json:
   ```json
   {
     "scripts": {
       "deploy": "npm run build && gh-pages -d dist"
     }
   }
   ```

3. Deploy
   ```bash
   npm run deploy
   ```

### Option 4: Firebase Hosting

1. Install Firebase CLI
   ```bash
   npm install -g firebase-tools
   ```

2. Login and initialize
   ```bash
   firebase login
   firebase init hosting
   ```

3. Build and deploy
   ```bash
   npm run build
   firebase deploy
   ```

## 📱 Mobile App (WebView Approach)

### Android APK using Cordova/Capacitor

#### Using Capacitor (Recommended)

1. **Install Capacitor**
   ```bash
   npm install @capacitor/core @capacitor/cli
   npm install @capacitor/android
   ```

2. **Initialize Capacitor**
   ```bash
   npx cap init
   ```
   - App name: AgriSarthi AI
   - Package ID: com.agrisarthi.app

3. **Build the web app**
   ```bash
   npm run build
   ```

4. **Add Android platform**
   ```bash
   npx cap add android
   ```

5. **Copy web assets**
   ```bash
   npx cap sync
   ```

6. **Open in Android Studio**
   ```bash
   npx cap open android
   ```

7. **Build APK in Android Studio**
   - Build > Build Bundle(s) / APK(s) > Build APK(s)
   - APK will be in `android/app/build/outputs/apk/`

#### Using Cordova

1. **Install Cordova**
   ```bash
   npm install -g cordova
   ```

2. **Create Cordova project**
   ```bash
   cordova create agrisarthi-app com.agrisarthi.app AgriSarthiAI
   cd agrisarthi-app
   ```

3. **Add Android platform**
   ```bash
   cordova platform add android
   ```

4. **Copy your dist folder to www/**
   ```bash
   # Build your React app first
   npm run build
   # Then copy
   cp -r ../dist/* www/
   ```

5. **Build APK**
   ```bash
   cordova build android --release
   ```

### iOS App (requires Mac)

1. **Add iOS platform**
   ```bash
   npx cap add ios
   ```

2. **Open in Xcode**
   ```bash
   npx cap open ios
   ```

3. **Build in Xcode**

## 🔧 Configuration

### Environment Variables

Create `.env` file for any API keys (optional):

```env
VITE_WEATHER_API_KEY=your_api_key_here
```

### Base URL Configuration

If deploying to subdirectory, update `vite.config.ts`:

```typescript
export default defineConfig({
  base: '/your-subdirectory/',
  // ... rest of config
})
```

## 📊 Performance Optimization

### 1. Image Optimization
- Use WebP format for images
- Compress images before upload
- Implement lazy loading

### 2. Code Splitting
Already implemented via React Router lazy loading

### 3. PWA (Progressive Web App)

Install Vite PWA plugin:

```bash
npm install -D vite-plugin-pwa
```

Update `vite.config.ts`:

```typescript
import { VitePWA } from 'vite-plugin-pwa'

export default defineConfig({
  plugins: [
    VitePWA({
      registerType: 'autoUpdate',
      manifest: {
        name: 'AgriSarthi AI',
        short_name: 'AgriSarthi',
        description: 'Smart Farming Assistant',
        theme_color: '#10b981',
        icons: [
          {
            src: 'icon-192.png',
            sizes: '192x192',
            type: 'image/png'
          },
          {
            src: 'icon-512.png',
            sizes: '512x512',
            type: 'image/png'
          }
        ]
      }
    })
  ]
})
```

## 🔒 Security Best Practices

1. **API Keys**: Never commit API keys
2. **Content Security Policy**: Add CSP headers
3. **HTTPS**: Always use HTTPS in production
4. **Input Validation**: Implemented client-side

## 🐛 Troubleshooting

### Build Errors

**Issue**: Module not found
```bash
# Clear node_modules and reinstall
rm -rf node_modules package-lock.json
npm install
```

**Issue**: Port already in use
```bash
# Kill process on port 5173
npx kill-port 5173
```

### Runtime Errors

**Issue**: LocalStorage not working
- Check browser privacy settings
- Ensure not in incognito mode

**Issue**: Voice not working
- Check browser microphone permissions
- Ensure HTTPS (required for some browsers)

## 📱 Testing

### Browser Testing
- Chrome/Edge (recommended)
- Firefox
- Safari
- Mobile browsers

### Responsive Testing
```bash
# Use Chrome DevTools
F12 > Toggle Device Toolbar
```

### Lighthouse Score
```bash
# Run Lighthouse audit
npm run build
npx serve dist
# Open Chrome DevTools > Lighthouse
```

## 🔄 Updates & Maintenance

### Dependency Updates
```bash
# Check for updates
npm outdated

# Update all dependencies
npm update

# Update specific package
npm install package@latest
```

### Version Control
```bash
# Tag versions
git tag -a v1.0.0 -m "Version 1.0.0"
git push origin v1.0.0
```

## 📈 Analytics (Optional)

Add Google Analytics or similar:

```bash
npm install react-ga4
```

## 🎯 Next Steps for Production

1. [ ] Set up proper backend API
2. [ ] Implement real ML models
3. [ ] Add user authentication
4. [ ] Set up database
5. [ ] Implement real-time weather API
6. [ ] Add payment gateway for premium features
7. [ ] Set up error monitoring (Sentry)
8. [ ] Add analytics
9. [ ] Implement CI/CD pipeline
10. [ ] Add automated testing

## 📞 Support Resources

- React Documentation: https://react.dev
- Vite Documentation: https://vitejs.dev
- Tailwind CSS: https://tailwindcss.com
- Capacitor: https://capacitorjs.com

---

**Ready to deploy! 🚀**

For production deployment, ensure you:
- Use environment variables for sensitive data
- Enable HTTPS
- Optimize images and assets
- Test on multiple devices
- Monitor performance
- Set up error tracking
