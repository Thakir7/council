# المجلس الاستشاري الذكي 🏛️

موقع ويب للمجلس الاستشاري المدعوم بالذكاء الاصطناعي.

---

## هيكل المشروع

```
council-project/
├── vercel.json          ← إعدادات Vercel
├── api/
│   └── chat.js          ← السيرفر الآمن (يحمل API Key)
└── public/
    └── index.html       ← واجهة الموقع
```

---

## خطوات الرفع على Vercel (مجاني)

### 1. أنشئ حساب على Vercel
- اذهب إلى https://vercel.com
- سجّل بحساب GitHub أو Google

### 2. ارفع المشروع
**الطريقة الأسهل — بدون GitHub:**
- اذهب إلى https://vercel.com/new
- اسحب مجلد `council-project` كاملاً وأفلته

**أو عبر GitHub:**
- ارفع المجلد على GitHub
- اربطه بـ Vercel

### 3. أضف API Key (الخطوة المهمة 🔑)
بعد الرفع، في لوحة تحكم Vercel:
1. افتح مشروعك
2. اذهب إلى **Settings** ← **Environment Variables**
3. أضف متغير جديد:
   - **Name:** `ANTHROPIC_API_KEY`
   - **Value:** مفتاحك من https://console.anthropic.com
4. اضغط **Save**
5. اضغط **Redeploy**

### 4. موقعك جاهز! 🎉
ستحصل على رابط مثل: `https://your-council.vercel.app`

---

## لماذا هذا الأسلوب آمن؟

- ✅ API Key محفوظ في متغيرات البيئة على Vercel
- ✅ المستخدم لا يرى الكود الخلفي أبداً
- ✅ المتصفح يتصل بـ `/api/chat` فقط (سيرفرك)
- ✅ السيرفر هو وحده من يتصل بـ Anthropic

---

## للحصول على API Key
1. اذهب إلى https://console.anthropic.com
2. سجّل دخول أو أنشئ حساباً
3. من القائمة اختر **API Keys**
4. اضغط **Create Key**
