# Root-Me Challenge Writeups

Write-ups for challenges solved on [Root-Me](https://www.root-me.org), a hacking and information-security learning platform. This repo currently covers the **Web-Client** and **Web-Server** categories.

مستندات حل چند چلنج از پلتفرم [Root-Me](https://www.root-me.org) — پلتفرمی برای یادگیری هک و امنیت اطلاعات. این رپو در حال حاضر دسته‌های **Web-Client** و **Web-Server** رو پوشش میده.

---

## 🇬🇧 About this repo

Each challenge has its own folder with a bilingual (English / Persian) `README.md` explaining the statement, the thought process, the exploitation steps (with screenshots), the result, and a short security takeaway. The goal is to document the *reasoning*, not just drop the final answer.

> **Note:** unlike most public writeup repos, the passwords/flags found for each challenge **are shown in full** here (at the user's request) — Root-Me generally discourages publishing live challenge solutions, so if you intend to solve these challenges yourself, you may want to stop reading before the "Result" section of each writeup.

## 🇮🇷 درباره‌ی این رپو

هر چلنج پوشه‌ی مخصوص خودش رو داره، با یه `README.md` دوزبانه (انگلیسی/فارسی) که صورت مسئله، روند فکری، مراحل اکسپلویت (همراه با اسکرین‌شات)، نتیجه، و یه جمع‌بندی امنیتی کوتاه رو توضیح میده. هدف مستندسازی *روند فکری* هست، نه فقط گذاشتن جواب نهایی.

> **توجه:** برخلاف اکثر رپوهای writeup عمومی، پسورد/فلگ پیداشده برای هر چلنج اینجا **به‌طور کامل نمایش داده شده** (به درخواست صاحب رپو) — چون معمولاً Root-Me انتشار جواب چلنج‌های فعال رو توصیه نمی‌کنه، اگه قصد دارید خودتون این چلنج‌ها رو حل کنید، بهتره قبل از بخش «نتیجه»/«Result» هر writeup متوقف بشید.

---

## Challenges / چلنج‌ها

### Web-Client

| # | Challenge | Points | Technique |
|---|-----------|:------:|-----------|
| 1 | [HTML - Disabled buttons](web-client/01-html-disabled-buttons/) | 5 | Removing the `disabled` attribute via DevTools |
| 2 | [Javascript - Obfuscation 1](web-client/02-javascript-obfuscation-1/) | 10 | URL-decoding a password with CyberChef |
| 3 | [Javascript - Native code](web-client/03-javascript-native-code/) | 15 | Beautifying + decoding JSFuck-obfuscated JS |
| 4 | [Javascript - Obfuscation 3](web-client/04-javascript-obfuscation-3/) | 30 | Double-decoding (hex-escape → decimal ASCII) with dCode |
| 5 | [XSS - Stored 1](web-client/05-xss-stored-1/) | 30 | Stored XSS exfiltrating the admin cookie via Request Catcher |

### Web-Server

| # | Challenge | Points | Technique |
|---|-----------|:------:|-----------|
| 1 | [HTML - Source code](web-server/01-html-source-code/) | 5 | Password leaked in an HTML comment |
| 2 | [HTTP - User-agent](web-server/02-http-user-agent/) | 10 | Spoofing the `User-Agent` header with curl |
| 3 | [HTTP - Directory indexing](web-server/03-http-directory-indexing/) | 15 | Following a source-code hint through an exposed `admin/backup/` directory listing |
| 4 | [HTTP - Cookies](web-server/04-http-cookies/) | 20 | Editing a client-trusted role cookie (`visiteur` → `admin`) |
| 5 | [File upload - Double extensions](web-server/05-file-upload-double-extensions/) | 20 | Uploading a PHP web shell as `shell.php.png` to bypass an extension filter |

**Total: 10 challenges · 182 points**

---

## Tools used / ابزارهای استفاده‌شده

- Browser DevTools (Inspector / Console / Storage / Network)
- [CyberChef](https://gchq.github.io/CyberChef/) — encoding/decoding
- [dCode](https://www.dcode.fr/) — ASCII/hex/decimal conversions
- `curl` — crafting custom HTTP requests
- [Request Catcher](https://requestcatcher.com/) — capturing exfiltrated HTTP requests (XSS)
- An AI assistant (Claude), used as a decoding/analysis aid on one JSFuck-obfuscated challenge, with the result manually verified

---

## Disclaimer

This repository is for **educational purposes only**, documenting personal learning progress on publicly available training challenges from [Root-Me](https://www.root-me.org). All techniques shown are meant to be practiced only on systems you own or are explicitly authorized to test (such as Root-Me's own training environment).

این رپو صرفاً برای **اهداف آموزشی** ساخته شده و روند یادگیری شخصی روی چلنج‌های آموزشی عمومی پلتفرم [Root-Me](https://www.root-me.org) رو مستند میکنه. تمام تکنیک‌های نمایش‌داده‌شده فقط باید روی سیستم‌هایی که خودتون مالکشون هستید یا مجوز صریح برای تست دارید (مثل محیط آموزشی خود Root-Me) تمرین بشن.
