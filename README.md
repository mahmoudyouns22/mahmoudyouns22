# Mahmoud Youns Mahmoud

**Cybersecurity undergraduate · Co-founder & Head of Technology at Nexaura · Erbil, Kurdistan**

I build AI systems that run — not prototypes that stop at an accuracy score.
Most of my work sits where machine learning meets security: detecting attacks
in live traffic and responding to them without a human in the loop.

---

### What I'm building

#### [destdeng](https://github.com/mahmoudyouns22/destdeng) — sign language to text, in the language the reader needs · [live](https://mahmoudyouns22.github.io/destdeng/)

There are roughly 10,000 deaf people in the Kurdistan Region and, as of 2024,
five working sign language interpreters. Kurdish Sign Language is its own
language with its own dialects, and there is no public dataset for it — every
off-the-shelf sign recogniser is trained on a language nobody here signs.

A camera reads 21 hand keypoints per hand. The classifier outputs a
language-neutral label, and the label is written in English, Arabic or Sorani
Kurdish — whichever the person reading the screen actually reads, switchable
mid-conversation because the reader is often not the person holding the device.

The metric is not accuracy. A wrong translation in a hospital is worse than no
translation, so recognition passes two independent gates and refuses rather
than guesses — feeding the trained model pure noise produced a `100%` confident
answer before the novelty gate existed. Both gates are asserted in the test
suites, in Python and again in JavaScript, because a gate that exists in one
language and is assumed in the other is not a gate.

Two front ends over one pipeline: a desktop app, and a browser build that runs
entirely on the device with nothing uploaded. The two feature implementations
are held to numerical equality by a parity check, since a vector built
differently is not a worse input but a meaningless one scored with confidence.

The word board works today, in all three languages, with no model at all.
Recording the vocabulary is the step still under way.

#### Radd *(pre-launch)* — a WhatsApp receptionist that speaks the customer's dialect

An assistant that takes restaurant orders and clinic bookings over WhatsApp in
Iraqi Arabic and Sorani Kurdish — by text, by voice note, or on a live call. It
is my own venture, built on Python, FastAPI and Gemini.

The rules that matter live in code, not in the prompt. Prices are computed
from the menu, never by the model. Every reply is checked before it is sent,
for prices that are not on the menu and for leaked model names. Complaints and
allergies go straight to a person, and nothing is confirmed until a member of
staff presses a button.

`122` automated tests, and a `30`-case Arabic and Kurdish evaluation run
against the live model. Text and voice ordering work end to end; WhatsApp call
integration and launch are still ahead. The code is private.

#### [kurdish-scam-detector](https://github.com/mahmoudyouns22/kurdish-scam-detector) — scam messages, caught in the language they arrive in

Sorani Kurdish and Iraqi Arabic SMS fraud detection. Arabic phishing detection
is well published; for Kurdish, as far as I could find, nothing existed — so
the corpus is part of the contribution. Character n-grams over an Arabic-script
normalisation layer, plus 28 interpretable signals.

Five-fold scam-F1 `0.961 ± 0.012`. Latin-script Kurdish — how a lot of Sorani
is actually typed on a phone — used to be its worst case at `0.483`; trained on
one romanisation and tested on a different, unseen one, it now reaches `0.886`
with false positives on legitimate messages unchanged.

Train on Arabic, test on Kurdish: `0.832` against `0.884` in-language, on
concept-grouped splits so parallel translations cannot leak. Strip the
hand-built signals and transfer falls to about `0.48` — the shared script
carries far less of it than it first appeared.

The whole classifier is `1.2 MB` of JSON running in your browser — nothing is
uploaded, because the tool asks people to paste an SMS that may hold their bank
details. The README states the synthetic-corpus caveat and the failure cases up
front, including a regression the romanisation fix itself caused.

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
Languages      Python · TypeScript · JavaScript · C++ · SQL . HTML . CSS
Building       Flask · Streamlit · Next.js · Prisma · Firebase · Tailwind · Git
```

---

### Elsewhere

Selected participant, **AI Olympiad 2026** — one of 100 chosen across the
Kurdistan Region; organised by Ovanya with the Consulate General of the Republic
of Korea in Erbil and the KRG Department of Technology.

12th place, 11th National Innovation Competition in Engineering (NICE 2026),
Tishk International University.

Kurdish · Arabic · English

[Email](mailto:mahmoudyouns2004110@gmail.com)
