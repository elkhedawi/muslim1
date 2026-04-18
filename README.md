# 📱 تطبيق مُسْلِم — دليل البناء والنشر

## ما تم تجهيزه لك
✅ مشروع Capacitor كامل
✅ كود التطبيق محمّل داخل `www/index.html`
✅ إعدادات Android (AndroidManifest, Colors, Styles, Network Security)
✅ تهيئة Capacitor لدعم اللغة العربية والـ RTL

---

## الخطوات لبناء APK

### المتطلبات
1. [Android Studio](https://developer.android.com/studio) — مجاني
2. [Java JDK 17](https://adoptium.net/) — مجاني
3. Node.js — مثبت بالفعل

### الخطوات

```bash
# 1. افتح المجلد
cd muslim-app

# 2. ثبّت الحزم
npm install

# 3. زامن الملفات
npx cap sync android

# 4. افتح Android Studio
npx cap open android
```

### داخل Android Studio
1. انتظر Gradle Sync ينتهي (دقيقتين تقريباً)
2. **للاختبار على Emulator:** اضغط ▶ (Run)
3. **لبناء APK:**
   - قائمة `Build` → `Build Bundle(s) / APK(s)` → `Build APK(s)`
   - ستجد الملف في: `android/app/build/outputs/apk/debug/app-debug.apk`

### لبناء APK للنشر (Signed Release)
1. `Build` → `Generate Signed Bundle / APK`
2. أنشئ Keystore جديد (احفظه!)
3. اختر `APK` → `Release`
4. APK جاهز للنشر على Google Play

---

## النشر على Google Play
1. افتح [Google Play Console](https://play.google.com/console)
2. ادفع رسوم التسجيل مرة واحدة: **$25**
3. أنشئ تطبيق جديد
4. ارفع الـ APK أو AAB
5. أضف: وصف، screenshots، أيقونة 512×512
6. انتظر المراجعة: 1-3 أيام

---

## معلومات التطبيق
- **App ID:** `com.saifeltohamy.muslim`
- **App Name:** مُسْلِم
- **Version:** 1.0.0
- **Theme Color:** #1A2A1A (أخضر داكن)
- **Accent Color:** #B8860B (ذهبي)

---

## لإضافة iOS (يحتاج Mac + Xcode)
```bash
npx cap add ios
npx cap open ios
```

## تحديث محتوى التطبيق
1. عدّل `www/index.html`
2. شغّل `npx cap sync`
3. ابنِ APK جديد من Android Studio
