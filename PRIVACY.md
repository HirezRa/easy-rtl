# מדיניות פרטיות — Easy RTL

*עדכון אחרון: 17 ביוני 2026*

**Easy RTL** הוא תוסף Chrome שמספק תמיכה ב-RTL (ימין לשמאל) בשני מצבים: היפוך עמוד לפי אתר (Allowlist) ב-HTTPS, ותיקון טקסט דו-כיווני ב-`claude.ai` ו-`console.anthropic.com`.

## איזה מידע נאסף?

**אף מידע.** התוסף לא אוסף, לא שולח ולא משתף נתונים אישיים, היסטוריית גלישה, תוכן הודעות או analytics.

## מה נשמר מקומית?

התוסף משתמש ב-`chrome.storage.sync` של Chrome כדי לזכור העדפות בלבד:

- `globalRtlSites` — רשימת hostnames שבהם RTL לאתר מופעל
- `claudeRtlEnabled` — האם מצב Claude מופעל (boolean)

ההגדרות נשמרות בפרופיל Chrome שלך ומסונכרנות בין מכשירים מחוברים (אם Sync פעיל). למפתחי התוסף אין גישה לנתונים אלה.

## גישה לאתרים

- **RTL לאתר** — רץ רק על hostnames שהמשתמש הוסיף ל-Allowlist (נרשמים דינמית ב-`chrome.scripting`). מוסיף class `rtl-enabled` ל-`<html>`.
- **RTL ב-Claude** — רץ על `claude.ai` ו-`console.anthropic.com`. מוסיף `dir="auto"` לאלמנטי טקסט (מסומנים ב-`data-easyrtl-stamped`) ו-CSS ל-bidi.

התוסף משנה את ה-DOM רק לצורך תצוגת RTL. הוא לא קורא תוכן לשום מטרה אחרת ולא מעביר מידע מהמחשב שלך.

## בקשות רשת

התוסף לא מבצע בקשות רשת. אין תקשורת עם שרתים, כולל שרתי המפתח.

## צד שלישי

לא משתפים מידע עם צד שלישי. אין ספריות חיצוניות או trackers.

## הרשאות

- `storage` — שמירת העדפות on/off בין הפעלות.
- `activeTab` — גישה ללשונית הפעילה בעת לחיצה על התוסף או קיצור מקלדת.
- `scripting` — רישום content scripts רק ל-hostnames ב-Allowlist של המשתמש.

אין `host_permissions` רחבות — אין גישה ל-`https://*/*`.

## שינויים במדיניות

שינויים יפורסמו בדף זה עם עדכון תאריך "עדכון אחרון".

---

*Easy RTL הוא פרויקט עצמאי ואינו קשור ל-Anthropic, Google או Chrome.*

---

# Privacy Policy — Easy RTL

*Last updated: June 17, 2026*

**Easy RTL** is a Chrome extension for RTL support: per-site page flip on HTTPS (allowlist), and smart bidirectional text on `claude.ai` and `console.anthropic.com`.

## Data collection

**None.** No personal data, browsing history, message content, or analytics are collected or transmitted.

## Local storage

`globalRtlSites` (hostname array) and `claudeRtlEnabled` (boolean) via `chrome.storage.sync`. Settings stay in the user's Chrome profile; the developer has no access.

## Site access

- **Per-site RTL:** Scripts register only for user-selected hostnames via `chrome.scripting`. Adds `rtl-enabled` to `<html>`.
- **Claude RTL:** Runs on `claude.ai` and `console.anthropic.com`. Applies `dir="auto"` and bidirectional CSS to stamped text elements.

DOM changes are limited to RTL display. No content is read or transmitted off-device.

## Network

No network requests. No third-party libraries or trackers.

## Permissions

- `storage` — persist on/off preferences.
- `activeTab` — active tab only when the user opens the popup or uses the keyboard shortcut.
- `scripting` — dynamic content-script registration for allowlisted hostnames only.

No broad `host_permissions` (no `https://*/*`).

## Policy changes

Updates will be posted on this page with a revised "last updated" date.

---

*Easy RTL is an independent project and is not affiliated with Anthropic, Google, or Chrome.*
