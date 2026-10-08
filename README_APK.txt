ZPHS TV Palli ప్రగతి — PWABuilder ద్వారా APK
రాయ్ ఎడ్యుకేషన్ | https://raayeducation.in
=============================================

PWABuilder కు ఫైల్ కాదు, HTTPS లింక్ కావాలి. Blogger లో ఈ ఫైల్స్ పెట్టలేము,
కాబట్టి GitHub Pages (ఉచితం) వాడండి.

1. GitHub లో ఫైల్స్ పెట్టడం
   - github.com → Sign up / Login
   - "+" → New repository → పేరు: zphs-pragathi → Public → Create
   - "uploading an existing file" నొక్కి ఈ ZIP లోని ఫైల్స్ అన్నీ
     (ZIP కాదు, లోపలి ఫైల్స్) అప్‌లోడ్ → Commit changes
   - Settings → Pages → Branch: main, /(root) → Save
   - 1–2 నిమిషాల్లో లింక్ వస్తుంది:  https://<మీ-username>.github.io/zphs-pragathi/
   - Chrome లో ఆ లింక్ తెరిచి యాప్ పనిచేస్తుందో చూడండి

2. PWABuilder
   - pwabuilder.com → ఆ లింక్ పేస్ట్ → Start
   - Manifest, Service Worker, HTTPS — మూడూ ✔ రావాలి
   - Package for stores → Android → Generate
       * Package ID: in.raayeducation.zphspragathi
       * App name: ZPHS ప్రగతి
       * Signing key: "Create new"
   - Download → ZIP లో .apk (ఫోన్‌లో ఇన్‌స్టాల్), .aab (Play Store),
     signing.keystore + signing-key-info.txt
   - signing.keystore, key-info జాగ్రత్తగా దాచుకోండి — తర్వాత అప్‌డేట్ APK కి అవే కావాలి

3. (ఐచ్ఛికం) మీ డొమైన్‌తో:  app.raayeducation.in
   - Hostinger DNS → CNAME:  app  →  <మీ-username>.github.io
   - GitHub → Settings → Pages → Custom domain: app.raayeducation.in → Enforce HTTPS
   - PWABuilder లో ఆ లింక్ ఇవ్వండి

అడ్రస్ బార్ వస్తే
   - APK పైన చిన్న అడ్రస్ బార్ కనిపిస్తే: PWABuilder ZIP లోని assetlinks.json ను
     రిపోజిటరీలో .well-known/assetlinks.json గా పెట్టాలి.
     ఇది డొమైన్ మూలం (root) లో ఉండాలి — కాబట్టి app.raayeducation.in లాంటి
     కస్టమ్ డొమైన్‌తో అయితేనే సులభంగా పనిచేస్తుంది.

గమనికలు
   - తర్వాత మార్పు వస్తే GitHub లో index.html మాత్రమే మార్చండి — APK మళ్ళీ చేయనక్కర్లేదు,
     ఇంటర్నెట్ ఉన్నప్పుడు యాప్ తెరిస్తే కొత్తది వస్తుంది (sw.js లో v2 → v3 మార్చండి).
   - అదే లింక్‌ను ఫోన్ Chrome లో తెరిస్తే యాప్ డేటానే కనిపిస్తుంది.
     పాత .html ఫైల్ డేటా రావాలంటే: పాత ఫైల్‌లో ⬇️ బ్యాకప్ → యాప్‌లో ⬆️ బ్యాకప్ ఎక్కించు.
   - ఈ పద్ధతిలో 🖨️ ప్రింట్ / PDF యాప్‌లోనూ పనిచేస్తుంది. ఒకసారి తెరిచాక ఆఫ్‌లైన్‌లోనూ పనిచేస్తుంది.
