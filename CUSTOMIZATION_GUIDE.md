# دليل التخصيص الكامل

## 🎨 تخصيص التصميم والألوان

### تغيير الألوان الأساسية

افتح ملف `style.css` وعدّل متغيرات CSS في الجزء العلوي:

```css
:root {
    --primary-dark: #1a3a52;      /* الأزرق الداكن الأساسي */
    --primary-blue: #2c5aa0;      /* الأزرق الملكي */
    --secondary-blue: #4a90e2;    /* الأزرق الثانوي */
    --sky-blue: #87ceeb;          /* الأزرق السماوي */
    --white: #ffffff;             /* الأبيض */
    --light-gray: #f5f7fa;        /* الرمادي الفاتح */
    --medium-gray: #e0e6ed;       /* الرمادي المتوسط */
    --dark-gray: #2d3748;         /* الرمادي الغامق */
    --gold: #d4af37;              /* الذهبي */
    --gold-light: #e8d5a8;        /* الذهبي الفاتح */
}
```

### أمثلة على تغييرات اللون:

**تغيير إلى نمط أخضر:**
```css
--primary-dark: #1b4332;
--primary-blue: #2d6a4f;
--secondary-blue: #40916c;
--sky-blue: #52b788;
--gold: #74c69d;
```

**تغيير إلى نمط أحمر:**
```css
--primary-dark: #5a1a1a;
--primary-blue: #a01a1a;
--secondary-blue: #d32f2f;
--sky-blue: #f44336;
--gold: #ff9800;
```

---

## 📝 تخصيص المحتوى

### تغيير العنوان الرئيسي

في `index.html`، ابحث عن:
```html
<h1 class="hero-title">من الهشاشة إلى الاستدامة</h1>
```

وغيّره إلى:
```html
<h1 class="hero-title">عنوانك الجديد هنا</h1>
```

### تغيير الوصف

ابحث عن:
```html
<p class="hero-subtitle">رؤية استراتيجية لتطوير منظومة تعليمية مرنة وشاملة</p>
```

وغيّره إلى:
```html
<p class="hero-subtitle">وصفك الجديد هنا</p>
```

### تغيير محتوى الأقسام

ابحث عن القسم المطلوب (مثل `#executive-summary`) وعدّل النصوص مباشرة.

---

## 🖼️ إضافة الصور

### إنشاء مجلد الصور:
```bash
mkdir -p assets/images
```

### إضافة صورة في HTML:
```html
<img src="assets/images/your-image.jpg" alt="وصف الصورة">
```

### تحسين الصور:
```html
<!-- صورة مع lazy loading -->
<img src="assets/images/image.jpg" alt="الوصف" loading="lazy">

<!-- صورة مع عدة أحجام -->
<picture>
    <source media="(max-width: 600px)" srcset="assets/images/small.jpg">
    <source media="(min-width: 601px)" srcset="assets/images/large.jpg">
    <img src="assets/images/large.jpg" alt="الوصف">
</picture>
```

---

## 🔤 تخصيص الخطوط

### إضافة خط جديد من Google Fonts:

1. اذهب إلى [fonts.google.com](https://fonts.google.com)
2. اختر الخط المطلوب
3. انسخ رابط `<link>`
4. الصقه في `<head>` من `index.html`

مثال:
```html
<link href="https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&display=swap" rel="stylesheet">
```

### استخدام الخط الجديد في CSS:
```css
body {
    font-family: 'Amiri', 'Cairo', sans-serif;
}
```

---

## 🎬 تخصيص الحركات والتأثيرات

### تغيير سرعة الحركات:

في `style.css`:
```css
:root {
    --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}
```

غيّر `0.3s` إلى:
- `0.1s` - حركة سريعة جداً
- `0.5s` - حركة بطيئة
- `1s` - حركة بطيئة جداً

### تعديل حركة الدخول:

```css
@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(30px);  /* غيّر هذا الرقم */
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}
```

---

## 🔗 تخصيص الروابط والقوائم

### تغيير روابط الملاحة:

في `index.html`، ابحث عن:
```html
<ul class="nav-menu" id="navMenu">
    <li><a href="#hero" class="nav-link">الرئيسية</a></li>
    <!-- أضف روابط جديدة هنا -->
</ul>
```

### إضافة قسم جديد:

1. أضف رابط في القائمة:
```html
<li><a href="#new-section" class="nav-link">القسم الجديد</a></li>
```

2. أضف القسم في الصفحة:
```html
<section id="new-section" class="section">
    <div class="container">
        <div class="section-header">
            <h2>عنوان القسم الجديد</h2>
            <div class="header-line"></div>
        </div>
        <!-- محتوى القسم -->
    </div>
</section>
```

---

## 🎯 تخصيص الأزرار

### تغيير نص الزر:

```html
<button class="btn btn-primary" onclick="alert('تم النقر!')">
    اضغط هنا
</button>
```

### إضافة زر جديد:

```html
<div class="hero-buttons">
    <button class="btn btn-primary">الزر الأساسي</button>
    <button class="btn btn-secondary">الزر الثانوي</button>
    <button class="btn btn-custom">زر مخصص</button>
</div>
```

### تصميم زر مخصص:

```css
.btn-custom {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
}

.btn-custom:hover {
    transform: scale(1.05);
}
```

---

## 📱 تخصيص الاستجابة (Responsive)

### تغيير نقاط التوقف (Breakpoints):

في `style.css`:
```css
/* للأجهزة اللوحية */
@media (max-width: 768px) {
    /* أضف التعديلات هنا */
}

/* للهواتف الذكية */
@media (max-width: 480px) {
    /* أضف التعديلات هنا */
}

/* للأجهزة الصغيرة جداً */
@media (max-width: 360px) {
    /* أضف التعديلات هنا */
}
```

---

## 🌙 تخصيص الوضع الليلي

### تغيير ألوان الوضع الليلي:

```css
[data-theme="dark"] {
    --primary-dark: #0f1419;
    --primary-blue: #1a2f4a;
    --white: #1e2a3a;
    --dark-gray: #e0e6ed;
}
```

---

## 📊 إضافة محتوى ديناميكي

### إضافة عداد جديد:

```html
<div class="stat-box">
    <div class="stat-number" data-target="500">0</div>
    <div class="stat-label">طالب مستفيد</div>
</div>
```

الرقم سيتم عده من 0 إلى 500 تلقائياً عند التمرير.

### إضافة بطاقة جديدة:

```html
<div class="summary-card fade-in-up">
    <div class="card-icon">🎓</div>
    <h3>العنوان</h3>
    <p>الوصف هنا</p>
</div>
```

---

## 🔍 تخصيص SEO

### تحديث معلومات الصفحة:

في `<head>` من `index.html`:
```html
<title>عنوان الصفحة الجديد</title>
<meta name="description" content="وصف الصفحة الجديد">
<meta name="keywords" content="كلمات مفتاحية">
```

### إضافة Open Graph للمشاركة:

```html
<meta property="og:title" content="عنوان الصفحة">
<meta property="og:description" content="الوصف">
<meta property="og:image" content="صورة.jpg">
<meta property="og:url" content="https://yoursite.com">
```

---

## 🛠️ تخصيص JavaScript

### إضافة دالة جديدة:

في `script.js`:
```javascript
function myCustomFunction() {
    console.log('دالتي المخصصة');
}

// استدعاء الدالة
document.addEventListener('DOMContentLoaded', myCustomFunction);
```

### تعديل سلوك الأزرار:

```javascript
document.querySelector('.btn-primary').addEventListener('click', () => {
    alert('تم النقر على الزر!');
});
```

---

## 📧 إضافة نموذج اتصال

### إضافة نموذج HTML:

```html
<form id="contactForm">
    <input type="text" placeholder="اسمك" required>
    <input type="email" placeholder="بريدك الإلكتروني" required>
    <textarea placeholder="رسالتك" required></textarea>
    <button type="submit" class="btn btn-primary">إرسال</button>
</form>
```

### معالجة النموذج بـ JavaScript:

```javascript
document.getElementById('contactForm').addEventListener('submit', (e) => {
    e.preventDefault();
    alert('شكراً لرسالتك!');
    // هنا يمكنك إضافة كود لإرسال البيانات
});
```

---

## 🚀 نصائح للتخصيص المتقدم

1. **استخدم DevTools**: اضغط F12 في المتصفح لفحص العناصر
2. **اختبر التغييرات**: افتح الملف في المتصفح بعد كل تعديل
3. **احتفظ بنسخة احتياطية**: قبل إجراء تغييرات كبيرة
4. **استخدم التعليقات**: أضف تعليقات في الكود لتتذكر التغييرات

---

**تم إنشاؤه بواسطة:** Manus AI  
**آخر تحديث:** 2024
