# AI INSTRUCTIONS — Claude (Anthropic)

راهنمای اختصاصی **Claude** (Claude.ai، Claude Code، Claude API) برای رعایت Universal Project Governance & Collaboration Skill است. اگر `SKILL.md` این Kit در دسترس Claude است (مثلاً در `/mnt/skills/` یا پوشهٔ Skills پروژه)، Claude باید آن را به‌عنوان مرجع اصلی در نظر بگیرد؛ این فایل مکمل آن است.

## فعال‌سازی

در ابتدای هر نشست، پیش از هر تغییری در کد، این اطلاعات را از کاربر بگیر (یا اگر از قبل در مکالمه/Memory موجود است، همان را تأیید کن):

```
PROJECT NAME:
REPOSITORY:
BRANCH:
PROJECT OWNER:
PROJECT MANAGER:
```

و پاسخ بده:
```
GOVERNANCE STATUS: ACTIVE
```

## فرآیند اجباری پیش از هر تغییر

1. اگر به فایل‌های مخزن دسترسی داری (Claude Code / Cowork / ابزار فایل): `project-governance/PROJECT_POLICY.md`, `PROJECT_CONTEXT.md`, `CHANGELOG_AI_HUMAN.md`, `DECISIONS.md`, `OPEN_QUESTIONS.md` را بخوان.
2. اگر این پوشه وجود ندارد و مخزن تازه معرفی شده، به کاربر پیشنهاد بده آن را از `templates/` این Kit بسازد (یا خودت بساز، در صورت دسترسی نوشتن).
3. تحلیل اثر تغییر (فایل‌ها/ماژول‌های وابسته، سازگاری معماری) را قبل از نوشتن کد انجام بده.
4. اگر تغییر جزو موارد نیازمند تأیید مدیر است (بخش ۴ `PROJECT_POLICY.md`) — کد را ننویس؛ به‌جایش یک Proposal پیشنهاد بده و از کاربر تأیید بخواه.
5. در صورت ابهام یا تناقض در اطلاعات، حدس نزن — سؤال کن و پیشنهاد بده که در `OPEN_QUESTIONS.md` ثبت شود.
6. بعد از تغییر: یک رکورد `CHANGE-ID` جدید طبق `templates/CHANGELOG.template.md` بنویس (یا به کاربر بده تا خودش commit کند).
7. اگر Claude Code/Cowork در حال کار روی چند فایل یا چند نشست است، پیش از پایان، `HANDOVER.md` را به‌روزرسانی کن.

## نکات خاص Claude

- در Claude.ai بدون دسترسی مستقیم به Repository: خروجی را به‌صورت Diff/Patch/فایل کامل + CHANGE REPORT ارائه بده تا کاربر خودش اعمال کند.
- در Claude Code: از ابزارهای فایل (view/str_replace/bash) برای خواندن و ویرایش مستقیم فایل‌های `project-governance/` استفاده کن.
- هرگز `DECISIONS.md` یا `CHANGELOG_AI_HUMAN.md` را بازنویسی (Overwrite) نکن؛ همیشه Append کن مگر کاربر صراحتاً درخواست ویرایش رکورد خاصی را بدهد.
- اگر Memory/Project Knowledge فعال است، اطلاعات `PROJECT_POLICY.md` را می‌توانی برای نشست‌های بعدی به خاطر بسپاری، اما همیشه نسخهٔ فایل را منبع حقیقت (Source of Truth) بدان، نه حافظهٔ خودت.

## جملهٔ کلیدی برای پایان هر پاسخ فنی مهم

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
