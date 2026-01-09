# Pegas Website Deployment Guide

## ✅ Fixes Applied

### 1. **Cache Busting Version Updated**
- Updated all asset versions from `v=7.0` to `v=10.0`
- This forces browsers to download fresh copies of CSS and JavaScript files
- Files updated:
  - `styles.css?v=10.0`
  - `script.js?v=10.0`
  - All favicon images

### 2. **Optimized Netlify Configuration**
- Added proper cache control headers
- HTML files: immediate revalidation (no stale cache)
- CSS/JS files: long-term cache with `immutable` flag (since they're versioned)
- Images: optimized caching

## 🚀 Deployment Steps

### Step 1: Deploy to Netlify

```bash
# If using Git deployment (recommended):
git add .
git commit -m "Fix production deployment - update cache busting and headers"
git push origin main
```

### Step 2: Clear Netlify CDN Cache

After deployment, **you must clear Netlify's CDN cache**:

#### Option A: Via Netlify Dashboard
1. Go to https://app.netlify.com
2. Select your Pegas website
3. Go to **Deploys** tab
4. Click **Trigger deploy** > **Clear cache and deploy site**

#### Option B: Via Netlify CLI
```bash
netlify build --clear-cache
netlify deploy --prod
```

### Step 3: Clear Browser Cache

After deployment, clear cache in your browser:

#### Chrome/Edge:
1. Open pegas.lk
2. Press `Ctrl + Shift + Delete` (Windows) or `Cmd + Shift + Delete` (Mac)
3. Select "Cached images and files"
4. Click "Clear data"
5. **Hard reload**: Press `Ctrl + Shift + R` (Windows) or `Cmd + Shift + R` (Mac)

#### Or use Incognito/Private mode:
- `Ctrl + Shift + N` (Windows) or `Cmd + Shift + N` (Mac)
- Visit pegas.lk in private window

## 🔍 Verification Checklist

After deployment, verify on pegas.lk:

- [ ] All animations working (scroll effects, hover effects)
- [ ] Navigation menu working smoothly
- [ ] All sections displaying correctly
- [ ] Division cards expanding properly
- [ ] Contact form functioning
- [ ] Counter animations triggering
- [ ] Styles matching localhost appearance
- [ ] Mobile responsive design working

## 🛠️ If Issues Persist

### Check Browser Console
1. Open Developer Tools (F12)
2. Check Console tab for errors
3. Check Network tab - all resources should return 200 status

### Verify Files Loaded
Look for this in console:
```
✅ All resources loaded successfully
✅ Animations active
```

### Common Issues & Solutions

**Issue**: Old CSS/JS still loading
- **Solution**: Hard refresh browser (Ctrl+Shift+R)
- **Solution**: Clear Netlify CDN cache (see Step 2 above)

**Issue**: Animations not working
- **Solution**: Check browser console for JavaScript errors
- **Solution**: Ensure `script.js?v=10.0` is loading (check Network tab)

**Issue**: Styles not applied
- **Solution**: Ensure `styles.css?v=10.0` is loading (check Network tab)
- **Solution**: Check for CSS conflicts or missing files

## 📝 Best Practices for Future Updates

1. **Always update version numbers** when changing CSS/JS:
   - Change `?v=10.0` to `?v=11.0` after modifications
   
2. **Clear Netlify cache** after each deployment:
   - Use "Clear cache and deploy" option

3. **Test in incognito mode** first:
   - Ensures you're seeing fresh content without local cache

4. **Monitor deployments**:
   - Check Netlify deploy logs for errors
   - Verify build success before testing

## 🌐 Current Version

- **CSS Version**: 10.0
- **JavaScript Version**: 10.0
- **Favicon Version**: 10.0

---

**Note**: The version number in the URL query string (`?v=10.0`) is the primary cache-busting mechanism. Increment this number whenever you make changes to ensure users get the latest version.
