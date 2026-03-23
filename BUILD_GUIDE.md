# EnglishPlus App - APK Build Guide
## மொபைல் APK உருவாக்க வழிமுறை

---

## OPTION 1: PWABuilder (Easiest - Free) ⭐ RECOMMENDED
### முறை 1: PWABuilder (மிக எளிது - இலவசம்)

1. Deploy your app to a free hosting:
   - Go to https://vercel.com (free)
   - Sign in with GitHub
   - Drag & drop your `english-app` folder
   - Get your URL like: https://englishplus.vercel.app

2. Go to https://www.pwabuilder.com
   - Enter your deployed URL
   - Click "Start" → wait for analysis
   - Click "Package for Stores" → Android (.apk / .aab)
   - Download the signed APK

3. Install on Android:
   - Enable "Install from unknown sources" in Settings
   - Transfer APK to phone and install!

---

## OPTION 2: Capacitor (Professional APK) ⭐ FOR PLAY STORE

### Requirements:
- Node.js 18+
- Android Studio
- Java 17+

### Steps:
```bash
# 1. Install Capacitor
npm install @capacitor/core @capacitor/cli @capacitor/android

# 2. Initialize
npx cap init "EnglishPlus" "com.englishplus.app" --web-dir "."

# 3. Add Android platform
npx cap add android

# 4. Sync files
npx cap sync android

# 5. Open in Android Studio
npx cap open android

# 6. In Android Studio: Build → Generate Signed APK
```

---

## OPTION 3: Bubblewrap / Google TWA

```bash
npm install -g @bubblewrap/cli
bubblewrap init --manifest https://your-deployed-url/manifest.json
bubblewrap build
```
Output: `app-release-signed.apk`

---

## OPTION 4: Online APK Generators (Instant)

1. **AppsGeyser** - https://appsgeyser.com
   - Choose "WebSite App"
   - Enter your deployed URL
   - Download APK instantly

2. **WebIntoApp** - https://www.webintoapp.com
   - Upload HTML or enter URL
   - Generate APK for free

---

## GEMINI API KEY SETUP
### Gemini AI செயல்பட API Key வேண்டும்

1. Go to: https://aistudio.google.com
2. Click "Get API Key" (FREE)
3. Copy the key (starts with AIza...)
4. In the app → AI Speaking screen → Enter key → Save

**Free tier includes:**
- 15 requests per minute
- 1 million tokens per day
- Completely FREE for learning!

---

## APP FEATURES INCLUDED:
✅ Grammar - 7 lessons (Basic to Advanced) with Tamil translation
✅ Vocabulary - 12 words with Tamil meanings + Word of Day
✅ AI Speaking - Gemini powered chat (Practice/Translate/Correct)
✅ Translator - English ↔ Tamil, Telugu, Malayalam, Kannada
✅ Quiz system for each grammar lesson
✅ Offline capable (PWA)
✅ Voice input support
✅ Progress tracking
✅ Dark theme optimized for mobile

---

## FILES INCLUDED:
- `index.html` — Complete app (single file)
- `manifest.json` — PWA manifest for Android
- `sw.js` — Service worker (offline support)
- `BUILD_GUIDE.md` — This file

---

## TO ADD MORE CONTENT:
Edit the `LESSONS` array in index.html to add more grammar lessons.
Edit the `VOCAB` array to add more vocabulary words.
All content follows the same pattern with English + Tamil translation.

---

## PUBLISH TO PLAY STORE:
1. Use Capacitor method above to generate .aab file
2. Create Google Play Console account ($25 one-time fee)
3. Upload .aab → Fill store listing → Publish!

---

*Built with ❤️ for Tamil students learning English*
*தமிழ் மாணவர்களுக்காக கட்டப்பட்டது*
