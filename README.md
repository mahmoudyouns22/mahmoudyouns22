# Mahmoud Youns Mahmoud

**Cybersecurity undergraduate · Co-founder & Head of Technology at Nexaura · Erbil, Kurdistan**

I build AI systems that run — not prototypes that stop at an accuracy score.
Most of my work sits where machine learning meets security: detecting attacks
in live traffic, responding to them without a human in the loop, and stopping
ransomware before it finishes encrypting.

---

### What I'm building

**[ai-cyber-defense-system](https://github.com/mahmoudyouns22/ai-cyber-defense-system)** — Intrusion detection that acts on its own
Random Forest over 41 NSL-KDD traffic features. Scapy captures live packets,
the model scores them, attackers get redirected into a Flask honeypot,
enriched with geolocation, and auto-blocked. A Streamlit dashboard shows it
happening in real time.
`99.87%` on a held-out split · `77.93%` on the KDDTest+ benchmark — both
reported, because only one of them is honest.

**[web-vuln-scanner](https://github.com/mahmoudyouns22/web-vuln-scanner)** — Reconnaissance from raw sockets
Port scanning with banner grabbing, plus a web audit for missing security
headers and exposed files like `/.env`. Built without wrapping `nmap`,
because the point was to understand what a scan actually is.

**AI Ransomware Defense** *(in progress)* — Containment, not detection
An engine that watches filesystem activity for encryption-like behaviour,
halts the responsible processes the moment it appears, and triggers an
automated counter-response. Aimed at the gap signature-based antivirus
leaves open: strains that have no signature yet.

---

### At Nexaura

I co-founded Nexaura and own the entire technology function — architecture,
development, deployment, delivery. We build web platforms, applications, and
technical consulting for clients, including work shipped for companies in
Denmark.

---

### Working with

```
AI / ML        scikit-learn · pandas · NumPy · Random Forest · anomaly detection
Security       Scapy · Burp Suite · Nmap · Wireshark · honeypots · incident response
Languages      Python · C++ · TypeScript · SQL
Building       Flask · Streamlit · Next.js · Git
```

---

### Elsewhere

8th place, 11th National Innovation Competition in Engineering (NICE 2026),
Tishk International University.

Kurdish · Arabic · English

[Email](mailto:mahmoudyouns2004110@gmail.com)
