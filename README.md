Here’s a well-structured, detailed roadmap covering **all** XSS labs and documentation from your given URL. You can copy this into a Markdown/Word document and convert it to PDF using tools like Pandoc or Microsoft Word.

---

## 🚀 XSS Learning Roadmap & Labs

### 1. 📘 Intro & Theory

* **What is XSS?**
  Overview of reflected, stored, and DOM-based XSS ([portswigger.net][1], [portswigger.net][2])
* **XSS contexts**
  Locate injection points: HTML content, attributes, JS strings, template literals, etc.&#x20;
* **Preventing XSS**
  Strategies: output encoding, input validation, templating, CSP ([arxiv.org][3])
* **Cheat sheet**
  Comprehensive bypass vectors, downloadable as PDF ([portswigger.net][4])

---

### 2. 🧪 Reflected XSS (Server-side immediate response)

1. **Lab: Reflected XSS into HTML context with nothing encoded**
   Target: `<script>alert(1)</script>` ([portswigger.net][5])
2. **Lab: Reflected XSS into attribute with angle brackets HTML‑encoded**
   Target: break out into attribute, e.g., `onmouseover=alert(1)` ([portswigger.net][6])
3. **Lab: Reflected XSS into a JavaScript string with angle brackets HTML‑encoded**
   Break JS string, inject `'-alert(1)-'` ([portswigger.net][1])
4. **Lab: Reflected XSS into JS string with single‑quote/backslash escape**
   Use `</script><script>alert(1)</script>` ([portswigger.net][7])
5. **Lab: Reflected XSS into JS string with angle brackets & double‑quote HTML‑encoded**
   Payload: `\'-alert(1)//` ([portswigger.net][8])
6. **Lab: Reflected XSS into JS template literal**
   Use `${alert(1)}` ([portswigger.net][9])
7. **Lab: Reflected XSS into HTML with all standard tags blocked**
   Use a custom tag + `onfocus`, exfiltrates cookies ([portswigger.net][10])

---

### 3. 🏠 Stored XSS (Persisted attack via database)

* **Overview** of stored XSS & impact ([portswigger.net][11])

1. **Lab: Exploiting XSS to steal cookies** (PRACTITIONER) ([portswigger.net][12])
2. **Lab: Exploiting XSS to capture passwords** (PRACTITIONER) ([portswigger.net][13])
3. **Lab: Exploiting XSS to bypass CSRF defenses** (PRACTITIONER) ([portswigger.net][14])

---

### 4. 🧩 DOM‑based XSS (Client-side only)

* **DOM XSS overview**: sources, sinks, how to detect ([portswigger.net][15])

*(Labs use scanner/manual testing; no explicit lab links, but you’ll apply knowledge learned above in DOM context.)*

---

### 5. 🧰 Exploitation Techniques & Advanced Impact

* **Exploiting XSS**: stealing cookies, credentials, CSRF tokens ([portswigger.net][14])

---

## 🎓 How to Learn – Step-by-Step

| Stage        | Focus                                                                 |
| ------------ | --------------------------------------------------------------------- |
| **Theory**   | Study basic concepts (section 1), contexts and prevention strategies  |
| **Practice** | Work labs from Reflected → Stored → DOM contexts in order             |
| **Advanced** | Practice exploits: cookies, CSRF tokens, credentials                  |
| **Review**   | Use cheat sheet, revisit labs if needed, grab advanced bypass vectors |

➡️ Next, copy the structure above into a Markdown or Word document. Then, use one of these methods to convert to PDF:

* **Pandoc**:

  ```bash
  pandoc roadmap.md -o roadmap.pdf
  ```
* **Microsoft Word / Google Docs**: paste, then File → Download as PDF.

Let me know if you’d like me to generate the PDF content here or package it another way!

[1]: https://portswigger.net/web-security/cross-site-scripting/contexts/lab-javascript-string-angle-brackets-html-encoded?utm_source=chatgpt.com "Lab: Reflected XSS into a JavaScript string with angle brackets ..."
[2]: https://portswigger.net/web-security/cross-site-scripting?utm_source=chatgpt.com "What is cross-site scripting (XSS) and how to prevent it? - PortSwigger"
[3]: https://arxiv.org/abs/1810.01017?utm_source=chatgpt.com "Fighting Against XSS Attacks: A Usability Evaluation of OWASP ESAPI Output Encoding"
[4]: https://portswigger.net/web-security/cross-site-scripting/cheat-sheet?utm_source=chatgpt.com "Cross-Site Scripting (XSS) Cheat Sheet - 2025 Edition - PortSwigger"
[5]: https://portswigger.net/web-security/cross-site-scripting/reflected/lab-html-context-nothing-encoded?utm_source=chatgpt.com "Lab: Reflected XSS into HTML context with nothing encoded"
[6]: https://portswigger.net/web-security/cross-site-scripting/contexts/lab-attribute-angle-brackets-html-encoded?utm_source=chatgpt.com "Lab: Reflected XSS into attribute with angle brackets HTML-encoded"
[7]: https://portswigger.net/web-security/cross-site-scripting/contexts/lab-javascript-string-single-quote-backslash-escaped?utm_source=chatgpt.com "Lab: Reflected XSS into a JavaScript string with single quote and ..."
[8]: https://portswigger.net/web-security/cross-site-scripting/contexts/lab-javascript-string-angle-brackets-double-quotes-encoded-single-quotes-escaped?utm_source=chatgpt.com "Lab: Reflected XSS into a JavaScript string with angle brackets and ..."
[9]: https://portswigger.net/web-security/cross-site-scripting/contexts/lab-javascript-template-literal-angle-brackets-single-double-quotes-backslash-backticks-escaped?utm_source=chatgpt.com "Lab: Reflected XSS into a template literal with angle brackets, single ..."
[10]: https://portswigger.net/web-security/cross-site-scripting/contexts/lab-html-context-with-all-standard-tags-blocked?utm_source=chatgpt.com "Lab: Reflected XSS into HTML context with all tags blocked except ..."
[11]: https://portswigger.net/web-security/cross-site-scripting/stored?utm_source=chatgpt.com "stored XSS - Cross-site scripting - PortSwigger"
[12]: https://portswigger.net/web-security/cross-site-scripting/exploiting/lab-stealing-cookies?utm_source=chatgpt.com "Lab: Exploiting cross-site scripting to steal cookies - PortSwigger"
[13]: https://portswigger.net/web-security/cross-site-scripting/exploiting/lab-capturing-passwords?utm_source=chatgpt.com "Lab: Exploiting cross-site scripting to capture passwords - PortSwigger"
[14]: https://portswigger.net/web-security/cross-site-scripting/exploiting/lab-perform-csrf?utm_source=chatgpt.com "Lab: Exploiting XSS to bypass CSRF defenses - PortSwigger"
[15]: https://portswigger.net/web-security/cross-site-scripting/dom-based?utm_source=chatgpt.com "DOM-based XSS - Cross-site scripting - PortSwigger"
