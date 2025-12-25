# 🚀 Website Deployment Guide

## Understanding the Problem

**Current Situation**: Your website only works when your computer is on because you're running it locally.

**Solution**: Deploy your website to Netlify's servers so it's live 24/7 on the internet.

---

## ✅ Deploy to Netlify (Make Your Website Live 24/7)

### Method 1: Drag & Drop (Easiest - Takes 2 Minutes)

1. **Go to Netlify**
   - Visit: https://app.netlify.com
   - Sign up for a free account (or login if you have one)

2. **Deploy Your Site**
   - Click "Add new site" button
   - Select "Deploy manually"
   - Drag the entire `pegas-lk-website` folder into the upload area
   - Wait 30-60 seconds for deployment

3. **Your Site is Live!**
   - You'll get a URL like: `https://random-name-12345.netlify.app`
   - This URL works 24/7 from anywhere in the world
   - You can close your computer and it stays online!

4. **Get a Better URL (Optional)**
   - Click "Site settings" → "Change site name"
   - Choose something like: `pegas-company.netlify.app`

---

### Method 2: Deploy via GitHub (Best for Updates)

1. **Push Your Code to GitHub**
   ```bash
   # If not already done
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

2. **Connect GitHub to Netlify**
   - Go to https://app.netlify.com
   - Click "Add new site" → "Import an existing project"
   - Choose "GitHub"
   - Authorize Netlify to access your GitHub
   - Select the `Pegas_Website` repository

3. **Configure Build Settings**
   - **Branch to deploy**: `main`
   - **Build command**: (leave empty)
   - **Publish directory**: `.` (just a dot)
   - Click "Deploy site"

4. **Automatic Updates**
   - Every time you push to GitHub, your site updates automatically!
   - No need to manually redeploy

---

### Method 3: Using Netlify CLI

1. **Install Netlify CLI**
   ```powershell
   npm install -g netlify-cli
   ```

2. **Login to Netlify**
   ```powershell
   netlify login
   ```

3. **Deploy Your Site**
   ```powershell
   cd c:\Users\hp\Desktop\new\pegas-lk-website
   netlify deploy --prod
   ```

4. **Follow the prompts**:
   - Create a new site or link to existing
   - Publish directory: `.` (current directory)
   - Confirm deployment

---

## 🔍 How to Check If Your Site is Live

1. **Visit Your Netlify Dashboard**: https://app.netlify.com
2. **Check Site Status**: Should show "Published"
3. **Test Your URL**: Click on your site URL
4. **Test from Another Device**: Try opening the URL on your phone or another computer
5. **Turn Off Your Computer**: The site should still work!

---

## 🛠️ Troubleshooting

### Issue: "Page Not Found" (404 Error)
**Solution**: Check that your `index.html` is in the root of your project folder

### Issue: "Build Failed"
**Solution**: This is a static site - make sure Build command is empty and Publish directory is `.`

### Issue: "Site Not Updating"
**Solution**: 
- Clear your browser cache (Ctrl + Shift + R)
- Check Netlify dashboard for deployment status
- Wait a few minutes for DNS propagation

### Issue: "Custom Domain Not Working"
**Solution**: 
- Add your domain in Site Settings → Domain management
- Update your domain's DNS settings as shown by Netlify
- Wait 24-48 hours for DNS propagation

---

## 📱 After Deployment Checklist

✅ Site opens on different browsers  
✅ Site opens on mobile devices  
✅ Site works when computer is OFF  
✅ All images load correctly  
✅ All links work properly  
✅ Contact form works (if applicable)  
✅ Site appears in Google search (takes 1-2 weeks)  

---

## 🎯 Custom Domain (Optional)

1. **Buy a Domain**: Get a domain like `pegascompany.com` from:
   - Namecheap
   - GoDaddy
   - Google Domains

2. **Connect to Netlify**:
   - Netlify Dashboard → Site Settings → Domain management
   - Click "Add custom domain"
   - Enter your domain name
   - Follow DNS configuration instructions

3. **Free SSL Certificate**: Netlify provides HTTPS automatically!

---

## 💡 Key Points to Remember

1. **Local vs Live**:
   - **Local**: Only works on your computer
   - **Live (Deployed)**: Works 24/7 on the internet

2. **Free Hosting**: Netlify is FREE for static websites like yours

3. **Making Updates**:
   - Edit your files
   - Deploy again (drag & drop OR push to GitHub)
   - Changes appear in 30-60 seconds

4. **Your Site Will Have**:
   - 99.9% uptime (almost always online)
   - Fast global CDN
   - Free HTTPS/SSL certificate
   - Automatic backups

---

## 🆘 Need Help?

- Netlify Support: https://answers.netlify.com/
- Netlify Documentation: https://docs.netlify.com/
- Video Tutorial: Search "How to deploy to Netlify" on YouTube

---

**Your website will be live 24/7 after deployment - no need to keep your computer on!** 🎉
