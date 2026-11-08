# ရိုမန်တစ် 💕

အချစ်လမ်းညွှန် Android App (Capacitor + Tailwind)။ GitHub Actions က APK ကို အလိုအလျောက် ထုတ်ပေးပါတယ်။

## APK ထုတ်နည်း (ကွန်ပျူတာမလိုပါ)
1. GitHub မှာ repository အသစ်ဆောက်ပါ။
2. ဒီ project ထဲက ဖိုင်/ဖိုလ်ဒါ အားလုံးကို upload လုပ်ပါ (`.github` ဖိုလ်ဒါပါ ပါရမယ်)။
3. **Actions** tab → **Build Android APK** → ပြီးသည်အထိ စောင့်ပါ (၅–၁၀ မိနစ်)။
4. Run အောက်ဆုံးက **Artifacts → romantic-apk** ကို download လုပ်ပြီး zip ဖြေကာ `romantic.apk` ကို ဖုန်းမှာ install လုပ်ပါ။
   (Unknown sources ခွင့်ပြုချက် လိုနိုင်ပါတယ်)

Release အဖြစ် ထုတ်ချင်ရင် tag တင်ပါ: `git tag v1.0.0 && git push --tags`

## ပြင်ချင်ရင်
- အကြောင်းအရာ/UI → `www/index.html`
- Logo/icon → `assets/` ထဲက ပုံတွေ (icon-only.png 1024×1024)၊ `www/logo.png`
- App နာမည် → `capacitor.config.json` ထဲက `appName`
- Style → `src/input.css`, `tailwind.config.js`

## Computer မှာ စမ်းချင်ရင်
```
npm install
npm run build:css
npx cap add android && npx capacitor-assets generate --android && npx cap sync android
cd android && ./gradlew assembleDebug
```
