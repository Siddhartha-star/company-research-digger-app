# Company Research Digger App - Deployment Guide

## ✅ Pre-Deployment Checklist

Your app is **READY FOR DEPLOYMENT**! All dependencies are installed and the build is working.

## 🚀 Deploy to Vercel

### Step 1: Create Vercel Account
1. Go to [vercel.com](https://vercel.com)
2. Sign up with GitHub

### Step 2: Import Project
1. Click **"Add New Project"**
2. Import your GitHub repository: `Siddhartha-star/company-research-digger-app`
3. **IMPORTANT:** Set the Root Directory to: `account-plan-agent/account-plan-agent`

### Step 3: Configure Build Settings
Vercel should auto-detect these, but verify:
- **Framework Preset:** Vite
- **Build Command:** `npm run build`
- **Output Directory:** `dist`
- **Install Command:** `npm install`

### Step 4: Add Environment Variables
Click **"Environment Variables"** and add these (use your actual API keys):

```
VITE_GEMINI_API_KEY=your_actual_gemini_api_key
VITE_FIREBASE_API_KEY=your_actual_firebase_api_key
VITE_FIREBASE_AUTH_DOMAIN=web-app-27e0f.firebaseapp.com
VITE_FIREBASE_PROJECT_ID=web-app-27e0f
VITE_FIREBASE_STORAGE_BUCKET=web-app-27e0f.firebasestorage.app
VITE_FIREBASE_MESSAGING_SENDER_ID=772741851188
VITE_FIREBASE_APP_ID=1:772741851188:web:18453671f70bb48be5c261
VITE_FIREBASE_MEASUREMENT_ID=G-Z6WJYE1BK1
```

⚠️ **Important:** Copy these values from your local `.env` file (with your new API keys)

### Step 5: Deploy!
Click **"Deploy"** and wait 2-3 minutes. Done! 🎉

## 📦 What's Included

✅ All dependencies installed (20 packages)  
✅ Firebase Firestore configured  
✅ Gemini AI API integrated  
✅ Vite build system configured  
✅ Tailwind CSS styling  
✅ Environment variables properly set up  
✅ Vercel routing configured  
✅ No backend needed - fully serverless!  

## 🏗️ Architecture

This is a **frontend-only** application:
- **Frontend:** React + Vite (deployed on Vercel)
- **Database:** Firebase Firestore (serverless)
- **AI:** Google Gemini API (serverless)
- **Analytics:** Firebase Analytics (serverless)

**No separate backend deployment needed!** Everything runs serverless.

## 🔒 Security

✅ No API keys in code  
✅ All credentials in environment variables  
✅ .env files git-ignored  
✅ Keys rotated after exposure  

## 📝 Local Development

```bash
# Install dependencies
npm install

# Start dev server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## 🐛 Troubleshooting

### Build fails on Vercel
- Check Root Directory is set to: `account-plan-agent/account-plan-agent`
- Verify all environment variables are added
- Check build logs for missing dependencies

### App loads but doesn't work
- Verify all environment variables are set correctly
- Check browser console for API errors
- Ensure Firebase and Gemini API keys are active

### "Failed to fetch" errors
- Check API keys are valid and not revoked
- Verify Firebase project is active
- Check API quotas/limits

## 📞 Support

If deployment fails, check:
1. Root directory setting
2. Environment variables
3. Build logs in Vercel dashboard

---

**Built with:** React, Vite, Firebase, Gemini AI, Tailwind CSS
