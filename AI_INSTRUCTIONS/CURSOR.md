# AI INSTRUCTIONS — Cursor (In-IDE AI Agent)

راهنمای اختصاصی Cursor برای رعایت Universal Project Governance & Collaboration Skill.
توصیه می‌شود محتوای این فایل (یا خلاصه‌ای از آن) در `.cursorrules` یا `.cursor/rules/` پروژه قرار گیرد تا در هر Session به‌صورت خودکار اعمال شود.

## فعال‌سازی

در اولین تعامل با این مخزن، تأیید کن:

```
PROJECT NAME:
REPOSITORY:
BRANCH:
PROJECT OWNER:
PROJECT MANAGER:
```

`GOVERNANCE STATUS: ACTIVE`

## قبل از پیشنهاد/اعمال هر تغییر

1. پیش از تولید Diff، `project-governance/PROJECT_POLICY.md`, `PROJECT_CONTEXT.md`, `CHANGELOG_AI_HUMAN.md`, `DECISIONS.md`, `OPEN_QUESTIONS.md` را بخوان.
2. اگر این پوشه در مخزن وجود ندارد، پیشنهاد بده از `templates/` ساخته شود.
3. سازگاری تغییر با معماری و تصمیمات ثبت‌شده را بررسی کن.
4. تغییرات حساس را به Proposal تبدیل کن و منتظر تأیید صریح بمان.

## بعد از هر تغییر

- بلوک آماده برای Changelog ارائه کن.
- در صورت تصمیم معماری، رکورد DECISIONS را پیشنهاد بده.

## نکات خاص Cursor

- پیش از نصب پکیج، تغییر Schema یا حذف فایل توقف کن و تأیید بگیر.
- Diff را کوچک و قابل Review نگه دار.
- تناقض `.cursorrules` قدیمی با Skill را اعلام کن.

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
