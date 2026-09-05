# AI INSTRUCTIONS — Codex / Autonomous Coding Agents

راهنمای اختصاصی Codex و سایر Agentهای خودکار کدنویسی (که مستقیماً به ترمینال، Git و فایل‌سیستم مخزن دسترسی دارند) برای رعایت Universal Project Governance & Collaboration Skill.

## فعال‌سازی

پیش از اجرای هر Task، تأیید کن Repository/Branch هدف مشخص و صحیح است:

```
PROJECT NAME:
REPOSITORY:
BRANCH:
PROJECT OWNER:
PROJECT MANAGER:
```

`GOVERNANCE STATUS: ACTIVE`

## فرآیند اجباری

1. **READ:** حتماً پیش از هر Commit، `project-governance/PROJECT_POLICY.md`, `PROJECT_CONTEXT.md`, `CHANGELOG_AI_HUMAN.md`, `DECISIONS.md`, `OPEN_QUESTIONS.md` را بخوان. اگر پوشه وجود ندارد، آن را از `templates/` بساز و اطلاع بده.
2. **ANALYZE:** `git log --oneline -20` و `git diff` مرتبط را بررسی کن.
3. **PLAN:** پیش از نوشتن کد، فایل‌ها/ماژول‌های تحت تأثیر را فهرست کن.
4. تغییرات نیازمند تأیید مدیر را Commit نکن؛ Proposal بساز و منتظر تأیید بمان.
5. **CHANGE:** تغییر را در کوچک‌ترین واحد منطقی اعمال کن.
6. **TEST:** تست‌های مرتبط را اجرا کن؛ نتیجه را ثبت کن.
7. **DOCUMENT:** پیش از PR، Changelog را به‌روز کن و از `github/pull_request_template.md` استفاده کن.

## نکات خاص Codex

- هرگز PR را خودکار Merge نکن اگر تغییر نیازمند تأیید مدیر است.
- در صورت هشدار CI درباره Changelog، آن را اصلاح کن.
- تاریخچه Git و فایل‌های governance را force-push یا rewrite نکن.

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
