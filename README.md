# ☢️ RadioEdu AI - Landing Page

<div align="center">

![RadioEdu AI Banner](https://img.shields.io/badge/RadioEdu-AI%20Powered-00d4ff?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cGF0aCBkPSJNMTIgMkM2LjQ4IDIgMiA2LjQ4IDIgMTJzNC40OCAxMCAxMCAxMCAxMC00LjQ4IDEwLTEwUzE3LjUyIDIgMTIgMnoiIGZpbGw9IiMwMGQ0ZmYiLz48L3N2Zz4=)
[![Status](https://img.shields.io/badge/Status-Coming%20Soon-yellow?style=for-the-badge)](https://radioedu.netlify.app)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

**أول منصة عربية ذكية لتعليم تقنيات الأشعة**

*The First Arabic AI-Powered Radiology Education Platform*

[🌐 زيارة الموقع](https://radioedu.netlify.app) • [📱 Instagram](https://www.instagram.com/s0_17iq) • [💬 Telegram](https://t.me/radioedu_ai) • [📧 تواصل معنا](mailto:hackerkwzaky4@gmail.com)

</div>

---

## 📖 نظرة عامة | Overview

**RadioEdu AI** هي منصة تعليمية ثورية مصممة لسد الفجوة بين التعليم النظري والممارسة السريرية لتقنيي الأشعة الناطقين بالعربية. نستخدم الذكاء الاصطناعي المتقدم لتوفير تجربة تدريب واقعية وتفاعلية.

RadioEdu AI is a revolutionary educational platform designed to bridge the gap between theoretical radiology education and clinical practice for Arabic-speaking radiologic technologists. We use advanced artificial intelligence to provide realistic and interactive training experiences.

---

## ✨ المميزات الرئيسية | Key Features

### 🤖 **ذكاء اصطناعي متخصص**
- مُدرّب على أكثر من **5000 صورة إشعاعية** متنوعة
- تحليل دقيق للتفاصيل التشريحية والمرضية
- تغذية راجعة فورية ومخصصة

### 🏥 **المركز السريري**
- مواجهة حالات طوارئ حقيقية (كسور، أورام، حالات صدرية)
- بيئة تدريب آمنة قبل الممارسة الفعلية
- سيناريوهات سريرية واقعية

### 🔬 **موسوعة تشريحية تفاعلية**
- استكشاف شامل للجسم البشري إشعاعياً
- مواد تعليمية منظمة ومبسطة
- تدريب تفاعلي بالذكاء الاصطناعي

### 🎮 **نظام تطوير الخبرة (XP)**
- تتبع تقدمك في الوقت الفعلي
- مكافآت ونقاط خبرة
- رحلة تعليمية ممتعة وتحفيزية

---

## 🛠️ التقنيات المستخدمة | Tech Stack

### **Frontend**
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

### **Backend & Database**
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white)

### **Hosting & Deployment**
![Netlify](https://img.shields.io/badge/Netlify-00C7B7?style=flat-square&logo=netlify&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)

### **Design Features**
- 🎨 Glassmorphism UI
- 🌙 Dark Mode Design
- 📱 Fully Responsive
- ⚡ Smooth Animations
- 🎯 Modern Gradients

---

## 🚀 التثبيت والإعداد | Installation & Setup

### المتطلبات الأساسية | Prerequisites
- حساب على [Supabase](https://supabase.com)
- حساب على [Netlify](https://netlify.com) (اختياري للنشر)

### خطوات التثبيت | Installation Steps

1. **استنساخ المستودع | Clone the repository**
```bash
git clone https://github.com/YOUR_USERNAME/radioedu-landing.git
cd radioedu-landing
```

2. **إعداد Supabase | Setup Supabase**

أنشئ مشروع جديد على Supabase وقم بإنشاء جدول البيانات:

```sql
CREATE TABLE email_subscribers (
  id BIGSERIAL PRIMARY KEY,
  email TEXT NOT NULL UNIQUE,
  name TEXT,
  phone TEXT,
  source TEXT DEFAULT 'landing_page',
  created_at TIMESTAMPTZ DEFAULT NOW()
);

-- Enable Row Level Security
ALTER TABLE email_subscribers ENABLE ROW LEVEL SECURITY;

-- Create policies
CREATE POLICY "Allow public insert"
ON email_subscribers
FOR INSERT
TO anon
WITH CHECK (true);

CREATE POLICY "Allow public read count"
ON email_subscribers
FOR SELECT
TO anon
USING (true);
```

3. **تحديث المفاتيح | Update API Keys**

افتح ملف `index.html` وابحث عن:

```javascript
const SUPABASE_URL = 'YOUR_SUPABASE_URL';
const SUPABASE_ANON_KEY = 'YOUR_SUPABASE_ANON_KEY';
```

استبدلها بمفاتيحك من **Settings → API** في Supabase.

4. **التشغيل محلياً | Run Locally**

```bash
# افتح الملف في المتصفح مباشرة
open index.html

# أو استخدم Live Server في VS Code
# أو أي HTTP server محلي
python -m http.server 8000
```

5. **النشر على Netlify | Deploy to Netlify**

```bash
# الطريقة 1: السحب والإفلات
# اذهب إلى netlify.com واسحب مجلد المشروع

# الطريقة 2: من خلال GitHub
# اربط المستودع مع Netlify وسيتم النشر تلقائياً
```

---

## 📁 هيكل المشروع | Project Structure

```
radioedu-landing/
│
├── index.html              # الملف الرئيسي | Main HTML file
├── README.md              # هذا الملف | This file
├── LICENSE                # رخصة المشروع | License
│
└── assets/               # (اختياري) للملفات الإضافية
    ├── images/          # الصور
    ├── fonts/           # الخطوط
    └── icons/           # الأيقونات
```

---

## 🎯 الميزات المميزة | Special Features

### ⚡ الأداء | Performance
- ⏱️ **تحميل سريع**: أقل من 2 ثانية
- 📱 **متجاوب بالكامل**: يعمل على جميع الأجهزة
- 🔒 **آمن**: HTTPS و SSL تلقائي

### 🎨 التصميم | Design
- 🌈 **تدرجات حديثة**: ألوان نابضة بالحياة
- 💎 **Glassmorphism**: تأثيرات زجاجية أنيقة
- ✨ **رسوم متحركة**: حركات سلسة وجذابة
- 🎭 **Dark Mode**: تصميم داكن مريح للعين

### 📊 التحليلات | Analytics
- 👥 **عداد المشتركين**: يتحدث في الوقت الفعلي
- ⏰ **عداد تنازلي**: للإطلاق القادم
- 📈 **تتبع التحويلات**: معدل التسجيل

---

## 📱 التواصل الاجتماعي | Social Media

<div align="center">

[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/s0_17iq)
[![TikTok](https://img.shields.io/badge/TikTok-000000?style=for-the-badge&logo=tiktok&logoColor=white)](https://tiktok.com/@radioedu.ai)
[![Telegram](https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/radioedu_ai)
[![WhatsApp](https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://wa.me/9647838819550)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:hackerkwzaky4@gmail.com)

</div>

---

## 🗺️ خارطة الطريق | Roadmap

### ✅ المرحلة 1 - الإطلاق الأولي (الآن)
- [x] تصميم صفحة الهبوط
- [x] ربط قاعدة البيانات
- [x] نظام التسجيل المبكر
- [x] تتبع المشتركين

### 🚧 المرحلة 2 - النسخة التجريبية (قريباً)
- [ ] إطلاق النسخة التجريبية
- [ ] المركز السريري الأساسي
- [ ] 100+ حالة سريرية
- [ ] نظام الـ XP الأساسي

### 🔮 المرحلة 3 - الإطلاق الرسمي (2026)
- [ ] 5000+ حالة سريرية
- [ ] الموسوعة التشريحية الكاملة
- [ ] تطبيق الجوال
- [ ] شهادات معتمدة

---

## 🤝 المساهمة | Contributing

نرحب بمساهماتكم! إذا كنت تريد المساعدة:

1. Fork المشروع
2. أنشئ branch جديد (`git checkout -b feature/AmazingFeature`)
3. Commit التغييرات (`git commit -m 'Add some AmazingFeature'`)
4. Push إلى الـ Branch (`git push origin feature/AmazingFeature`)
5. افتح Pull Request

---

## 📄 الرخصة | License

هذا المشروع مرخص تحت **MIT License** - راجع ملف [LICENSE](LICENSE) للتفاصيل.

---

## 👨‍💻 المطور | Developer

<div align="center">

**تم التطوير بمن قبل SAJAD JAMAA زميل لزملائه**

صُمم هذا المشروع من قبل خريج تقنيات أشعة لسد الفجوة بين التعليم النظري والممارسة السريرية

[![Instagram](https://img.shields.io/badge/@s0__17iq-E4405F?style=flat-square&logo=instagram&logoColor=white)](https://www.instagram.com/s0_17iq)
[![Email](https://img.shields.io/badge/Email-hackerkwzaky4@gmail.com-red?style=flat-square&logo=gmail&logoColor=white)](mailto:hackerkwzaky4@gmail.com)

</div>

---

## 📊 إحصائيات المشروع | Project Stats

<div align="center">

![GitHub Stars](https://img.shields.io/github/stars/YOUR_USERNAME/radioedu-landing?style=social)
![GitHub Forks](https://img.shields.io/github/forks/YOUR_USERNAME/radioedu-landing?style=social)
![GitHub Watchers](https://img.shields.io/github/watchers/YOUR_USERNAME/radioedu-landing?style=social)

</div>

---

## 🙏 شكر وتقدير | Acknowledgments

- شكراً لكل من ساهم في اختبار المنصة
- شكراً لمجتمع تقنيي الأشعة العرب على الدعم المستمر
- شكراً لـ Supabase و Netlify على الخدمات المجانية الرائعة

---

<div align="center">

**⭐ إذا أعجبك المشروع، لا تنسى إعطاءه نجمة! ⭐**

**Made By SAJAD JAMAA for ☢️ the Radiology Community**

</div>
