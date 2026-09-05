# AI INSTRUCTIONS — Lovable

راهنمای اختصاصی Lovable (پلتفرم تولید/توسعهٔ اپلیکیشن با AI) برای رعایت
Universal Project Governance & Collaboration Skill. از آنجا که Lovable معمولاً
مستقیماً روی یک پروژهٔ متصل به GitHub تغییر اعمال می‌کند، رعایت این قوانین
به‌ویژه برای جلوگیری از تغییرات ناخواسته در معماری/Database اهمیت دارد.

## فعال‌سازی

پیش از شروع کار روی یک پروژه، در اولین Prompt تأیید کن:

```
PROJECT NAME:
REPOSITORY (GitHub Sync):
BRANCH:
PROJECT OWNER:
PROJECT MANAGER:
```

`GOVERNANCE STATUS: ACTIVE`

## قبل از هر تغییر

1. اگر پروژه به GitHub Sync شده و پوشهٔ `project-governance/` وجود دارد، محتوای آن را
   (به‌ویژه `PROJECT_POLICY.md` و `PROJECT_CONTEXT.md`) پیش از تغییر بررسی کن.
2. اگر وجود ندارد، به کاربر پیشنهاد بده آن را از `templates/` این Kit اضافه کند —
   به‌ویژه چون Lovable اغلب توسط افراد غیر-فنی استفاده می‌شود، این پیشنهاد را
   ساده و بدون اصطلاحات فنی پیچیده بیان کن.
3. پیش از هر تغییری که شامل موارد زیر است، **متوقف شو و تأیید بگیر** (این‌ها معمولاً
   پرهزینه یا برگشت‌ناپذیرند):
   - تغییر Schema پایگاه‌داده (Supabase/Postgres)
   - تغییر سیستم احراز هویت
   - اتصال به یک سرویس پرداخت/API خارجی جدید
   - حذف صفحه/قابلیتی که کاربران از آن استفاده می‌کنند
4. برای تغییرات کوچک UI/متن/استایل، نیازی به توقف نیست؛ اما همچنان باید ثبت شود (پایین را ببین).

## بعد از هر تغییر

- یک خلاصهٔ ساده (بدون جارگون فنی سنگین) برای اضافه‌شدن به `CHANGELOG_AI_HUMAN.md` بده:
  چه چیزی تغییر کرد، چرا، و آیا نیاز به بررسی توسط یک توسعه‌دهندهٔ فنی دارد یا نه.
- اگر تصمیمی گرفته شد که بعداً برگشت آن سخت است (مثلاً انتخاب یک سرویس Backend خاص)، آن را به‌عنوان یک رکورد ساده در `DECISIONS.md` پیشنهاد بده.

## نکات خاص Lovable

- کاربران Lovable معمولاً غیر-فنی‌اند؛ توضیحات را ساده، کوتاه و بدون اصطلاح غیرضروری بنویس.
- هرگز بدون تأیید صریح، تغییری که هزینهٔ مالی (Upgrade پلن، سرویس Paid جدید) ایجاد می‌کند اعمال نکن.
- اگر ابهامی هست دربارهٔ اینکه کاربر دقیقاً چه می‌خواهد، حدس نزن — با یک سؤال ساده روشن کن.

## اصل پایانی

```
READ → ANALYZE → PLAN → CHANGE → TEST → DOCUMENT
```


## Resource Access Rule

If the current task requires another repository, service, project, or registered resource:
1. Check `project-governance/PROJECT_RESOURCES.md`.
2. Do not assume access.
3. Declare exactly what resource is needed and why.
4. Request the minimum required access from the Project Manager.
5. After access is granted, read that resource's context and governance files before making changes.
6. If access cannot be granted, provide a PATCH/DIFF/ZIP with implementation notes instead.
