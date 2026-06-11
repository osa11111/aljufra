# دليل النشر الكامل

## 🚀 خيارات النشر المجاني

هذا الموقع يمكن نشره مجاناً على عدة منصات. اختر الخيار الأنسب لك:

---

## 1️⃣ GitHub Pages (الأسهل والأكثر شيوعاً)

### الخطوات:

#### أ) إنشاء حساب GitHub
1. اذهب إلى [github.com](https://github.com)
2. انقر على "Sign up"
3. أكمل عملية التسجيل

#### ب) إنشاء مستودع جديد
1. بعد تسجيل الدخول، انقر على "+" في الزاوية العلوية اليمنى
2. اختر "New repository"
3. أدخل اسم المستودع: `strategic-plan-website`
4. اختر "Public"
5. انقر على "Create repository"

#### ج) رفع الملفات
**الطريقة 1: عبر الويب**
1. انقر على "Add file" → "Upload files"
2. اسحب جميع الملفات من مجلد المشروع
3. انقر على "Commit changes"

**الطريقة 2: عبر Git (للمتقدمين)**
```bash
cd /path/to/strategic-plan-website
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/strategic-plan-website.git
git push -u origin main
```

#### د) تفعيل GitHub Pages
1. اذهب إلى "Settings"
2. اختر "Pages" من القائمة اليسرى
3. تحت "Source"، اختر "Deploy from a branch"
4. اختر "main" و "/" (root)
5. انقر على "Save"

#### هـ) الموقع الخاص بك
سيكون متاحاً على: `https://YOUR_USERNAME.github.io/strategic-plan-website`

---

## 2️⃣ Netlify (الأسرع والأفضل للأداء)

### الخطوات:

#### أ) التسجيل
1. اذهب إلى [netlify.com](https://netlify.com)
2. انقر على "Sign up"
3. اختر "GitHub" للتسجيل السريع

#### ب) ربط المستودع
1. بعد التسجيل، انقر على "New site from Git"
2. اختر "GitHub"
3. ابحث عن مستودعك `strategic-plan-website`
4. اختره

#### ج) الإعدادات
- Build command: اتركه فارغاً
- Publish directory: `.`
- انقر على "Deploy site"

#### د) الموقع الخاص بك
سيكون متاحاً على: `https://your-site-name.netlify.app`

---

## 3️⃣ Vercel (الخيار الأفضل للأداء)

### الخطوات:

#### أ) التسجيل
1. اذهب إلى [vercel.com](https://vercel.com)
2. انقر على "Sign Up"
3. اختر "GitHub" للتسجيل السريع

#### ب) استيراد المشروع
1. انقر على "New Project"
2. اختر "Import Git Repository"
3. ابحث عن `strategic-plan-website`
4. انقر على "Import"

#### ج) النشر
- سيتم النشر تلقائياً
- الموقع الخاص بك: `https://strategic-plan-website.vercel.app`

---

## 4️⃣ Cloudflare Pages

### الخطوات:

#### أ) التسجيل
1. اذهب إلى [pages.cloudflare.com](https://pages.cloudflare.com)
2. انقر على "Sign up"

#### ب) إنشاء مشروع
1. انقر على "Create a project"
2. اختر "Connect to Git"
3. ربط حسابك على GitHub
4. اختر المستودع

#### ج) الإعدادات
- Framework preset: None
- Build command: اتركه فارغاً
- Build output directory: `.`
- انقر على "Save and Deploy"

#### د) الموقع الخاص بك
سيكون متاحاً على: `https://strategic-plan-website.pages.dev`

---

## 🌐 نشر على خادم خاص

إذا كان لديك خادم ويب خاص:

### عبر FTP:
1. استخدم برنامج FTP مثل FileZilla
2. انسخ جميع الملفات من المشروع
3. الصقها في مجلد `public_html` أو الجذر

### عبر SSH:
```bash
scp -r /path/to/strategic-plan-website/* user@yourserver.com:/var/www/html/
```

---

## ✅ التحقق من النشر

بعد النشر، تأكد من:

1. ✓ الصفحة الرئيسية تحمل بشكل صحيح
2. ✓ جميع الروابط تعمل
3. ✓ الوضع الليلي يعمل
4. ✓ القائمة الجوال تعمل على الهاتف
5. ✓ الصور والخطوط تحمل بشكل صحيح

---

## 🔧 تحديث الموقع

### بعد النشر على GitHub:
```bash
cd /path/to/strategic-plan-website
# قم بالتعديلات المطلوبة
git add .
git commit -m "Update description"
git push
```

سيتم التحديث تلقائياً على Netlify/Vercel/Cloudflare خلال دقائق.

---

## 📊 مراقبة الأداء

### Google Analytics:
1. اذهب إلى [analytics.google.com](https://analytics.google.com)
2. أنشئ حساباً جديداً
3. أضف الكود في `<head>` من `index.html`

### Lighthouse:
1. افتح الموقع في Chrome
2. اضغط F12 لفتح Developer Tools
3. اذهب إلى "Lighthouse"
4. انقر على "Generate report"

---

## 🔒 الأمان والخصوصية

- ✅ الموقع آمن تماماً (بدون قواعد بيانات)
- ✅ لا توجد بيانات شخصية يتم جمعها
- ✅ جميع المنصات توفر HTTPS تلقائياً
- ✅ الملفات ثابتة وآمنة

---

## 💡 نصائح إضافية

### تحسين الأداء:
- استخدم Cloudflare CDN للسرعة العالمية
- قم بضغط الصور قبل الرفع
- استخدم خدمات التخزين المؤقت (Caching)

### تحسين SEO:
- أضف وصفاً دقيقاً في `<meta name="description">`
- استخدم كلمات مفتاحية في العناوين
- أضف روابط داخلية بين الأقسام

### النسخ الاحتياطية:
- احتفظ بنسخة محلية من المشروع
- استخدم Git للتحكم بالإصدارات
- قم بنسخ احتياطية دورية

---

## 📞 الدعم والمساعدة

إذا واجهت مشكلة:

1. تحقق من أن جميع الملفات موجودة
2. تأكد من أن `index.html` في الجذر
3. امسح الذاكرة المؤقتة (Cache) في المتصفح
4. جرب متصفحاً آخر

---

**تم إنشاؤه بواسطة:** Manus AI  
**آخر تحديث:** 2024  
**الإصدار:** 1.0.0
