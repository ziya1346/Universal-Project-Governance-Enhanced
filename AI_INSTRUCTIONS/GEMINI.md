AI INSTRUCTIONS — Gemini (Google)
راهنمای اختصاصی Gemini (Gemini App، Gemini Code Assist، یا Agent مبتنی بر Gemini API) برای رعایت Universal Project Governance & Collaboration Skill.

فعال‌سازی
پیش از هر فعالیت فنی روی مخزن، این اطلاعات باید مشخص شود (از کاربر بگیر یا در System Instruction ابزار قرار بده):

PROJECT NAME:
REPOSITORY:
BRANCH:
PROJECT OWNER:
PROJECT MANAGER:

سپس: GOVERNANCE STATUS: ACTIVE

قبل از هر تغییر
اگر از طریق Gemini Code Assist / یک Connector به مخزن دسترسی داری، فایل‌های زیر را بخوان: project-governance/PROJECT_POLICY.md, PROJECT_CONTEXT.md, CHANGELOG_AI_HUMAN.md, DECISIONS.md, OPEN_QUESTIONS.md
اگر دسترسی نداری، از کاربر بخواه این فایل‌ها را در Prompt وارد کند؛ بدون آن‌ها فرض نساز.
تحلیل اثر (Impact Analysis) قبل از تولید کد: چه چیزی تغییر می‌کند، چه چیزی وابسته است.
اگر تغییر در دستهٔ موارد نیازمند تأیید مدیر است (بخش ۴ PROJECT_POLICY.md)، به‌جای اجرای مستقیم، یک Proposal طبق templates/PROPOSAL.template.md تولید کن.
در صورت تناقض بین دستور کاربر و مستندات پروژه، اجرا نکن — تناقض را توضیح بده و سؤال کن.
بعد از هر تغییر
رکورد جدید طبق templates/CHANGELOG.template.md بنویس.
در صورت تصمیم مهم معماری، رکورد DECISIONS.md را هم پیشنهاد بده.
در پایان کار روی یک وظیفهٔ چندمرحله‌ای، HANDOVER.md را به‌روزرسانی کن یا محتوای پیشنهادی آن را بده.
نکات خاص Gemini
برای پروژه‌های چندمخزنی، همیشه تأیید کن کدام Repository/Branch فعال است پیش از اجرای دستور — فعال‌سازی روی یک مخزن روی مخزن دیگر اثر ندارد.
از خروجی بیش‌ازحد پرحجم پرهیز کن؛ گزارش باید کوتاه و متمرکز باشد.
اصل پایانی
READ → ANALYZE → PLAN → CHANGE → TEST → DOCUMENT

Resource Access Rule
If the current task requires another repository, service, project, or registered resource:

Check project-governance/PROJECT_RESOURCES.md.
Do not assume access.
Declare exactly what resource is needed and why.
Request the minimum required access from the Project Manager.
After access is granted, read that resource's context and governance files before making changes.
If access cannot be granted, provide a PATCH/DIFF/ZIP with implementation notes instead.
