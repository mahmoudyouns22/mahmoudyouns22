# Mahmoud Youns Mahmoud

**Cybersecurity undergraduate · Co-founder & Head of Technology at Nexaura · Erbil, Kurdistan**

I build AI systems that run — not prototypes that stop at an accuracy score.
Most of my work sits where machine learning meets security: detecting attacks
in live traffic, responding to them without a human in the loop, and stopping
ransomware before it finishes encrypting.

---

### What I'm building

#### [kurdish-scam-detector](https://github.com/mahmoudyouns22/kurdish-scam-detector) — scam messages, caught in the language they arrive in

Sorani Kurdish and Iraqi Arabic SMS fraud detection. Arabic phishing detection
is well published; for Kurdish, as far as I could find, nothing existed — so
the corpus is part of the contribution. Character n-grams over an Arabic-script
normalisation layer, plus 28 interpretable signals.

Five-fold scam-F1 `0.938 ± 0.026`. Train on Arabic, test on Kurdish: `0.890`
against `0.949` in-language, on concept-grouped splits so parallel translations
cannot leak. The whole classifier is `719 KB` of JSON running in your browser —
nothing is uploaded, because the tool asks people to paste an SMS that may hold
their bank details.

The README states the synthetic-corpus caveat and the failure cases up front.

#### [ai-cyber-defense-system](https://github.com/mahmoudyouns22/ai-cyber-defense-system) — intrusion detection that acts on its own

Random Forest over 41 NSL-KDD traffic features. Scapy captures live packets,
the model scores them, attackers get redirected into a Flask honeypot,
enriched with geolocation, and auto-blocked. A Streamlit dashboard shows it
happening in real time.

`99.87%` on a held-out split · `77.93%` on the KDDTest+ benchmark — both
reported, because only one of them is honest.

#### [web-vuln-scanner](https://github.com/mahmoudyouns22/web-vuln-scanner) — reconnaissance from raw sockets

Port scanning with banner grabbing, plus a web audit for missing security
headers and exposed files like `/.env`. Built without wrapping `nmap`,
because the point was to understand what a scan actually is.

#### AI Ransomware Defense *(in progress)* — containment, not detection

An engine that watches filesystem activity for encryption-like behaviour,
halts the responsible processes the moment it appears, and triggers an
automated counter-response. Aimed at the gap signature-based antivirus
leaves open: strains that have no signature yet.

---

### At Nexaura . Padborg, Denmark

I co-founded Nexaura and own the entire technology function — architecture,
development, deployment, delivery.

#### [callaz.dk](https://callaz.dk) — production site for a Danish client

Next.js and TypeScript, bilingual Danish/English with locale-aware routing,
Tailwind, Zod-validated contact flows. Live.

#### Nexaura Client Portal — internal product

Next.js, Prisma over PostgreSQL, transactional email through Resend,
react-hook-form with Zod, multi-language. Built end to end: schema, API
routes, validation, delivery.

#### [mz-phone-store](https://github.com/mahmoudyouns22/mz-phone-store) — Arabic RTL storefront

~5,700 lines of vanilla JavaScript against Firebase Auth and Firestore, with
an admin panel and WhatsApp checkout. No framework and no build step, on
purpose: the owner updates products from a phone, and the site had to stay
fast on mobile data.

---

### Working with

```
AI / ML        scikit-learn · pandas · NumPy · Random Forest · anomaly detection
Security       Scapy · Burp Suite · Nmap · Wireshark · honeypots · incident response
Languages      Python · TypeScript · JavaScript · C++ · SQL
Building       Flask · Streamlit · Next.js · Prisma · Firebase · Tailwind · Git
```

---

### Elsewhere

8th place, 11th National Innovation Competition in Engineering (NICE 2026),
Tishk International University.

Kurdish · Arabic · English

[Email](mailto:mahmoudyouns2004110@gmail.com)
