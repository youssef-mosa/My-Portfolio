# يوسف موسى — Shopify Developer | بورتفوليو

موقع بورتفوليو (صفحة واحدة) لـ **Youssef Mosa — Shopify Developer**، يعرض أعمال متاجر Shopify وباقات التنفيذ، جاهز للنشر على **GitHub Pages** مباشرة بدون build tools أو استضافة.

> **الـPositioning:** متخصص في بناء وتخصيص متاجر Shopify (تخصيص الثيم و Liquid، تصميم الأجزاء المخصصة، تجربة الموبايل، الأداء، تجربة الشراء، تكاملات Shopify Apps). لا يقدّم خدمات الإعلانات أو التسويق أو الـMedia Buying.

---

## ⚡️ النشر على GitHub Pages (5 دقايق)

### الطريقة 1 — ريبو باسم `youssef-mosa.github.io` (رابط أنضف)
1. اعمل ريبو جديد اسمه بالحرف `youssef-mosa.github.io` (Public).
2. ارفع ملف `index.html` (+ `README.md` لو حابب).
3. استنى دقيقة → الموقع شغال على: **https://youssef-mosa.github.io/**

### الطريقة 2 — أي ريبو عادي (مثلاً `portfolio`)
1. اعمل ريبو وارفع الملفات.
2. من الريبو: **Settings → Pages → Source: Deploy from a branch → Branch: `main` / `root` → Save**.
3. الرابط: **https://youssef-mosa.github.io/portfolio/**

> 💡 لازم الملف اسمه `index.html` بالحرف في الـroot عشان يفتح تلقائي.

```bash
git init
git add .
git commit -m "Portfolio: Shopify developer — work & packages"
git branch -M main
git remote add origin https://github.com/youssef-mosa/portfolio.git
git push -u origin main
# بعدها فعّل Pages من Settings → Pages
```

---

## 📁 هيكل الملفات

```
portfolio/
├── index.html        ← الموقع النهائي (ملف واحد: CSS + JS + الصور جوّاه) ← ده اللي ترفعه
├── build.py          ← سكربت يجمع الموقع من src/ + assets/
├── src/
│   ├── 00_head.html      (الـdesign system: الألوان، التايبوجرافي، الـanimations، الـresponsive)
│   ├── 10_top.html       (الـNavbar: Youssef Mosa / Shopify Developer + روابط + زر تواصل معي)
│   ├── 20_hero.html      (Hero: الصورة الشخصية + النص + الـCTA + شريط المهارات)
│   ├── 30_work.html      (6 مشاريع Shopify)
│   ├── 40_packages.html  (Starter / Growth / Advanced + الإضافات)
│   ├── 50_process.html   (طريقة الشغل 4 خطوات + عنّي + Skills + Why work with me)
│   ├── 60_faq.html       (الأسئلة الشائعة)
│   └── 70_contact.html   (التواصل + الفوتر + JavaScript)
├── assets/           ← صور المشاريع + الصورة الشخصية (jpg مضغوطة)
└── README.md
```

**ليه ملف واحد؟** عشان الصور والتصميم جوّه الـHTML نفسه — مفيش مسارات تتكسر ولا صور تختفي على GitHub Pages، والموقع يفتح من أي مكان حتى أوفلاين.

---

## ✏️ التعديل على المحتوى

| عايز تعدّل | الملف |
|---|---|
| الأسعار وتفاصيل الباقات والإضافات | `src/40_packages.html` (ابحث عن `3,000` / `5,000` / `8,000`) |
| المشاريع والصور والوصف | `src/30_work.html` |
| الصورة الشخصية والنص الرئيسي | `src/20_hero.html` |
| الأسئلة الشائعة | `src/60_faq.html` |
| رقم الواتساب / الإيميل / السوشيال | `src/70_contact.html` (ابحث عن `201067644849`) |
| الألوان والخطوط | `src/00_head.html` في `:root` (المتغير `--accent` هو البرتقالي) |

بعد أي تعديل:
```bash
python3 build.py     # يعيد بناء index.html
```

---

## ✨ المميزات

- عربي/إنجليزي بزر تبديل في الـNavbar مع RTL كامل للعربي.
- Hero يبرز الصورة الشخصية كعنصر أساسي + قائمة خدمات واضحة (Shopify, Liquid, Custom Store Design, Performance, Mobile UX).
- 6 مشاريع Shopify بصور Preview وزر "زيارة المتجر" ووصف مختصر لكل مشروع.
- 3 باقات بكل الفيتشرز ظاهرة مباشرة في الكارت (بدون قوائم مخفية) مع تمييز الميزات الأساسية وبعدها "وأيضًا تشمل".
- الدفع: Starter فيه الدفع عند الاستلام فقط؛ Growth و Advanced فيهم الدفع عند الاستلام + الدفع الأونلاين.
- إضافات اختيارية مرتبطة بخدمة Shopify فقط + توضيح ما هو غير مشمول في السعر.
- موبايل-فرست، سريع، بدون مكتبات خارجية، ومع Schema/SEO الأساسي.

**للتواصل:** +20 106 764 4849 · youssefmosa179@gmail.com

---

## 📱 التوافق مع الأجهزة (تم الاختبار فعليًا)

اتعمل اختبار آلي بمتصفح حقيقي (Chromium) على **20 مقاس شاشة** — النتيجة: **صفر مشاكل**.

| المجموعة | المقاسات المُختبرة | النتيجة |
|---|---|---|
| موبايلات صغيرة | 280 (Galaxy Fold)، 320 (iPhone SE 1)، 360 | ✅ |
| موبايلات شائعة | 375، 390 (iPhone 12–15)، 393 (Pixel)، 412 (Galaxy S21+) | ✅ |
| موبايلات كبيرة | 414 (XR/11)، 430 (15 Pro Max)، 480 | ✅ |
| تابلت | 600، 768 (iPad)، 820 (iPad Air)، 1024 (iPad Pro) | ✅ |
| كمبيوتر | 1280، 1440 | ✅ |
| موبايل بالعرضي | 667×375، 844×390، 915×412، 560×280 | ✅ |

الاختبار بيتأكد من: **مفيش scroll أفقي** على أي مقاس · الهيدر الثابت شغال · زر القائمة بيظهر ويفتح/يقفل صح على الموبايل · مساحات اللمس ≥ 40px · الصور والعناوين مش بتتراكب.

- سكرين شوتات للمراجعة: فولدر `mobile-preview/`
- سكربتات الاختبار (لو حبيت تعيد تشغيلها بعد أي تعديل): فولدر `tools/` — التفاصيل في `tools/README.md`

---

### English — quick notes
`index.html` is a single self-contained file (CSS, JS and images inlined) — push it to a GitHub repo named `youssef-mosa.github.io` (or enable Pages on `main`/root) and it goes live. Positioning: **Shopify Developer specialized in building and customizing Shopify stores** — no marketing, ads or media-buying services are offered. Edit content in `src/*.html`, then run `python3 build.py`.
