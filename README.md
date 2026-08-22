# Calculator App

यह project Windows computer के लिए `.exe` और Android mobile के लिए `.apk` बनाता है।

## GitHub से build करना

1. इस folder की सभी files GitHub repository में upload करें।
2. GitHub में **Actions** tab खोलें।
3. **Build calculator installers** चुनें और **Run workflow** दबाएं।
4. Workflow पूरा होने के बाद run के नीचे से ये artifacts download करें:
   - `Calculator-Windows-Installer`: `Calculator-Setup.exe` वाला ZIP
   - `Calculator-Android`: `.apk` वाला ZIP

## Computer पर install

`Calculator-Windows-Installer` ZIP को download करके extract करें। अंदर `Calculator-Setup.exe` पर double-click करें, फिर **Next -> Install -> Finish** दबाएं। Setup Desktop shortcut, Start Menu shortcut और Windows uninstall entry बनाएगा।

## Android पर install

`Calculator-Android` ZIP download करके extract करें। अंदर की `.apk` file phone में भेजें, उस पर tap करें और Android के पूछने पर **Install unknown apps** की अनुमति दें। फिर **Install** दबाएं।

Android build `mobile_app.py` और Kivy का उपयोग करता है; Windows build `CAL.PY` और Tkinter का उपयोग करता है।

## Android HTML app install करना

`index.html`, `manifest.webmanifest`, `service-worker.js` और `icon.svg` GitHub repository में रखें। Repository में **Settings -> Pages -> Source: GitHub Actions** चुनें। `Deploy calculator to GitHub Pages` workflow पूरा होने के बाद उसका URL Android Chrome में खोलें, फिर browser menu से **Add to Home screen** या **Install app** दबाएं।

यह PWA है, APK नहीं। पहली बार URL खोलने के लिए internet जरूरी है; उसके बाद app offline भी चल सकती है।

दोनों installers में calculator का custom icon शामिल है।