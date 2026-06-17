# Easy RTL

תוסף Chrome לתמיכה ב-RTL (ימין לשמאל) — לעברית, ערבית ואנגלית מעורבים.

**מדיניות פרטיות:** [PRIVACY.md](./PRIVACY.md) · [GitHub Pages](https://hirezra.github.io/easy-rtl/PRIVACY)

---

## מה התוסף עושה?

Easy RTL מספק **שני מצבים נפרדים**:

| מצב | תיאור |
|-----|--------|
| **RTL לאתר** | היפוך כיוון העמוד (`html.rtl-enabled`) — רק באתרים שבחרת (Allowlist אישי) |
| **RTL ב-Claude** | תיקון חכם לטקסט דו-כיווני ב-`claude.ai` ו-`console.anthropic.com` — `dir="auto"` + CSS ל-bidi |

## תכונות עיקריות

- **Allowlist לפי אתר** — מפעילים RTL רק באתרים שבחרתם; הרשימה נשמרת ב-`chrome.storage.sync`
- **מצב Claude נפרד** — מתג ייעודי לשיחות מעורבות עברית / ערבית / אנגלית
- **קיצור מקלדת** — `Alt+Shift+R` מחליף מצב לפי הלשונית הפעילה (אתר או Claude)
- **ללא איסוף נתונים** — אין analytics, אין בקשות רשת, אין שיתוף עם צד שלישי
- **הרשאות מצומצמות** — `storage`, `activeTab`, `scripting`; אין `host_permissions` רחבות

## איך משתמשים?

1. לחצו על אייקון התוסף בסרגל הכלים
2. **RTL לאתר זה** — מוסיף את האתר הנוכחי ל-Allowlist (HTTPS בלבד)
3. **RTL ב-Claude** — מפעיל/מכבה תיקון bidi ב-Claude
4. **אפס הגדרות** — מחזיר ברירות מחדל (רשימת אתרים ריקה, Claude מופעל)

ניתן לשנות את קיצור המקלדת ב-`chrome://extensions/shortcuts`.

## פרטיות

התוסף לא אוסף מידע אישי. נשמרות רק שתי העדפות מקומיות:

- `globalRtlSites` — רשימת hostnames עם RTL לאתר
- `claudeRtlEnabled` — מצב Claude (on/off)

פרטים מלאים: **[מדיניות פרטיות](https://hirezra.github.io/easy-rtl/PRIVACY)**

## אודות מאגר זה

מאגר GitHub זה מארח את **מדיניות הפרטיות** של התוסף (נדרש לפרסום ב-Chrome Web Store).  
קוד המקור של התוסף אינו מפורסם כאן.

---

# Easy RTL (English)

Chrome extension for RTL (right-to-left) support — Hebrew, Arabic, and mixed English text.

**Privacy policy:** [PRIVACY.md](./PRIVACY.md) · [GitHub Pages](https://hirezra.github.io/easy-rtl/PRIVACY)

## What it does

| Mode | Description |
|------|-------------|
| **Per-site RTL** | Page direction flip (`html.rtl-enabled`) on user-selected HTTPS sites only |
| **Claude RTL** | Smart bidirectional text on `claude.ai` and `console.anthropic.com` |

## Highlights

- Personal allowlist — RTL applies only on sites you enable
- Separate Claude mode for mixed RTL/LTR conversations
- Keyboard shortcut: `Alt+Shift+R`
- No data collection, no network requests, no third-party trackers
- Minimal permissions: `storage`, `activeTab`, `scripting`

## Privacy

Only two preference values are stored locally via `chrome.storage.sync`.  
Full details: **[Privacy Policy](https://hirezra.github.io/easy-rtl/PRIVACY)**

## About this repository

This repo hosts the extension's **privacy policy** (required for Chrome Web Store).  
Extension source code is not published here.

---

*Easy RTL is an independent project and is not affiliated with Anthropic, Google, or Chrome.*
