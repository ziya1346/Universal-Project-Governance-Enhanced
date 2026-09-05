# AI INSTRUCTIONS — ChatGPT / GPT-based Agents (OpenAI)

راهنمای اختصاصی ChatGPT (Chat، Custom GPT، یا Agent مبتنی بر GPT/Codex API) برای
رعایت Universal Project Governance & Collaboration Skill.

## فعال‌سازی

پیش از هر کار فنی، این بلوک را از کاربر بخواه یا در Custom Instructions/System Prompt پروژه قرار بده:

```
ACTIVATE UNIVERSAL PROJECT GOVERNANCE SKILL
PROJECT:
REPOSITORY:
BRANCH:
PROJECT OWNER:
PROJECT MANAGER:
```

سپس تأیید کن: `GOVERNANCE STATUS: ACTIVE`

## قبل از هر تغییر

1. اگر به فایل‌ها دسترسی داری (Code Interpreter / Actions / Connectors به Repository)، حتماً بخوان:
   `project-governance/PROJECT_POLICY.md`, `PROJECT_CONTEXT.md`, `CHANGELOG_AI_HUMAN.md`, `DECISIONS.md`, `OPEN_QUESTIONS.md`
2. اگر دسترسی مستقیم نداری (چت معمولی بدون افزونه)، از کاربر بخواه محتوای این فایل‌ها را Paste کند یا خلاصه بدهد — بدون این Context، تغییر پیشنهاد نده.
3. اثر تغییر را تحلیل کن: چه فایل/ماژولی تحت تأثیر است، آیا با معماری فعلی سازگار است.
4. اگر تغییر جزو موارد نیازمند تأیید مدیر است، به‌جای نوشتن کد، یک **Proposal** طبق `templates/PROPOSAL.template.md` بنویس.
5. در ابهام حدس نزن؛ سؤال مشخص بپرس و پیشنهاد بده در `OPEN_QUESTIONS.md` ثبت شود.

## بعد از هر تغییر

- یک رکورد جدید طبق `templates/CHANGELOG.template.md` تولید کن و به کاربر بده تا در `CHANGELOG_AI_HUMAN.md` اضافه کند (یا اگر ابزار نوشتن فایل داری، خودت اضافه کن).
- اگر تصمیم معماری مهمی گرفته شد، رکورد `DECISIONS.md` را هم پیشنهاد بده.

## نکات خاص ChatGPT/Codex Agent

- در حالت Agent با اجرای کد/دسترسی به ترمینال: از `git diff`/`git log` برای گرفتن Context واقعی به‌جای حدس استفاده کن.
- خروجی طولانی/غیرمرتبط تولید نکن — گزارش باید کوتاه، دقیق و قابل استناد باشد (بخش ۲۰ Skill اصلی).
- هرگز تاریخچهٔ `DECISIONS.md` را حذف نکن؛ تصمیم قدیمی را `Superseded` علامت بزن، نه پاک.

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
