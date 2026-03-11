---
marp: true
theme: custom
footer: ![w:280](img/dhbw-ka.svg)

---

<style scoped>
h1 { font-size: 70pt; }
h2 { font-size: 40pt; }
</style>


# KI-Systemen und IT-Sicherheit


---

<!-- Sprechertext:
Begrüßung der Studierenden, kurzer Überblick über das Thema. Ziel: Verständnis dafür schaffen, warum KI-Sicherheit ein eigenständiges Feld ist und welche Risiken und Chancen KI in der IT-Sicherheit bietet.
-->

# 1. Motivation & Einführung

- KI-Systeme als kritische Infrastruktur
- Neue Angriffsflächen durch ML-Modelle
- Reale Vorfälle zeigen Verwundbarkeit
- KI verändert Angriffs- und Verteidigungsstrategien

---

<!-- Sprechertext:
Hier erläutere ich, warum KI-Sicherheit heute unverzichtbar ist. Beispiele wie Jailbreaks, Datenlecks oder Deepfakes helfen, die Relevanz zu verdeutlichen. Ich betone, dass KI nicht nur ein Werkzeug, sondern auch ein Angriffsziel ist.
-->

# Besonderheiten von KI-Systemen

- Datenabhängigkeit
- Probabilistische Entscheidungen
- Black-Box-Charakter
- Andere Angriffsvektoren als klassische Software

---

<!-- Sprechertext:
Ich erkläre, warum KI-Systeme sich fundamental von klassischer Software unterscheiden. Besonders wichtig: Modelle sind nur so gut wie ihre Daten, und ihre Entscheidungen sind nicht deterministisch.
-->

# Bedrohungsmodelle für KI

- Angriffe auf Daten
- Angriffe auf Modelle
- Angriffe auf KI-gestützte Systeme
- Angriffe durch KI

---

<!-- Sprechertext:
Ich stelle ein strukturiertes Bedrohungsmodell vor. Das hilft den Studierenden, die Vielzahl möglicher Angriffe einzuordnen.
-->

# 2. Angriffe während des Trainings

## Data Poisoning

- Manipulation der Trainingsdaten
- Label-Flipping
- Backdoor-Injektionen
- Risiken bei Web-Scraping

---

<!-- Sprechertext:
Ich erkläre typische Data-Poisoning-Angriffe und zeige Beispiele. Besonders spannend: Backdoors, die nur durch spezielle Trigger aktiviert werden.
-->

# Model Poisoning

- Verteiltes Training (Federated Learning)
- Gradient Manipulation
- Supply-Chain-Angriffe auf Modelle

---

<!-- Sprechertext:
Hier zeige ich, wie Angreifer Modelle selbst manipulieren können, besonders in kollaborativen Trainingsumgebungen. Supply-Chain-Angriffe sind ein wachsendes Risiko.
-->

# Schutzmaßnahmen (Training)

- Datenvalidierung
- Monitoring der Trainingspipelines
- Secure Model Supply Chain
- Robustheitsanalysen

---

<!-- Sprechertext:
Ich bespreche Gegenmaßnahmen und betone, dass KI-Sicherheit schon beim Training beginnt. Besonders wichtig: Integrität der Daten und Modelle.
-->

# 3. Angriffe während der Nutzung

## Prompt Injection

- Direkte Prompt Injection
- Indirekte Prompt Injection
- Jailbreaks
- Cross-Application Injection

---

<!-- Sprechertext:
Ich erkläre, wie Angreifer durch geschickte Eingaben Modelle manipulieren können. Beispiele aus Chatbots und KI-Agenten machen das Thema greifbar.
-->

# Adversarial Examples

- Manipulierte Eingaben
- Evasion Attacks
- Bild-, Audio-, Textdomänen
- Transferability

---

<!-- Sprechertext:
Ich zeige, wie minimale Veränderungen an Eingaben Modelle täuschen können. Beispiele aus der Bildverarbeitung sind besonders eindrucksvoll.
-->

# Model Extraction & Inversion

- API-basierte Modellrekonstruktion
- Rekonstruktion von Trainingsdaten
- Datenschutzrisiken

---

<!-- Sprechertext:
Ich erkläre, wie Angreifer Modelle oder Trainingsdaten rekonstruieren können. Besonders relevant für Datenschutz und geistiges Eigentum.
-->

# Schutzmaßnahmen (Nutzung)

- Input-Filter
- Rate-Limiting
- Differential Privacy
- Red-Teaming

---

<!-- Sprechertext:
Ich stelle konkrete Schutzmaßnahmen vor und betone die Bedeutung von Red-Teaming und Privacy-Techniken.
-->

# 4. KI als Werkzeug für Angreifer

## Automatisierte Schwachstellensuche

- KI-gestützte Codeanalyse
- KI-Fuzzing
- Automatisierte Exploit-Generierung

---

<!-- Sprechertext:
Ich zeige, wie KI Angreifern hilft, schneller Schwachstellen zu finden. Wichtig: ethische Einordnung.
-->

# Social Engineering

- Deepfakes
- KI-generierte Phishing-Kampagnen
- Voice Cloning

---

<!-- Sprechertext:
Ich bespreche die Rolle von KI im Social Engineering. Deepfakes und Voice Cloning sind besonders gefährlich.
-->

# Malware-Entwicklung

- KI zur Obfuskation
- KI zur Anpassung an AV/EDR-Systeme

---

<!-- Sprechertext:
Ich erkläre, wie KI Malware intelligenter und schwerer erkennbar macht. Fokus auf realistische Szenarien.
-->

# 5. KI als Verteidigungswerkzeug

## Anomalieerkennung

- ML-basierte IDS/IPS
- UEBA
- Erkennung von Zero-Day-Verhalten

---

<!-- Sprechertext:
Ich zeige, wie KI zur Erkennung von Angriffen eingesetzt wird. Besonders spannend: Zero-Day-Erkennung durch Verhaltensanalyse.
-->

# Automatisierte Reaktionen

- KI in SOAR-Systemen
- Policy-basierte Gegenmaßnahmen
- Risiken autonomer Verteidigung

---

<!-- Sprechertext:
Ich diskutiere Chancen und Risiken autonomer Reaktionen. Wichtig: menschliche Kontrolle.
-->

# Threat Intelligence

- Mustererkennung in großen Datenmengen
- Automatisierte Korrelation von Angriffskampagnen

---

<!-- Sprechertext:
Ich erkläre, wie KI hilft, komplexe Angriffsmuster zu erkennen und Threat Intelligence zu verbessern.
-->

# 6. Governance, Ethik & Regulierung

- EU AI Act
- Bias & Fairness
- Halluzinationen als Risiko
- Haftungsfragen

---

<!-- Sprechertext:
Ich bespreche rechtliche und ethische Aspekte. Besonders wichtig: Sicherheit vs. Fairness und die Rolle von Regulierung.
-->

# 7. Praktische Übungen

- Prompt Injection Challenge
- Adversarial Image Crafting
- Modellrobustheit testen
- KI-basiertes IDS

---

<!-- Sprechertext:
Ich stelle die geplanten Übungen vor und motiviere die Studierenden, aktiv mitzudenken und auszuprobieren.
-->

# 8. Fallstudien

- Analyse eines KI-Sicherheitsvorfalls
- Supply-Chain-Angriff auf ein Modell
- Lessons Learned

---

<!-- Sprechertext:
Ich bespreche reale Vorfälle und leite daraus Erkenntnisse ab. Ziel: Transfer in die Praxis.
-->

# 9. Ausblick

- KI-Agenten & autonome Systeme
- Multi-Agent-Sicherheit
- KI in kritischen Infrastrukturen
- Zukunft des AI Red Teaming

---

<!-- Sprechertext:
Ich gebe einen Ausblick auf zukünftige Entwicklungen und zeige, wie sich das Feld weiterentwickeln wird.
-->

# 10. Zusammenfassung

- Wichtigste Erkenntnisse
- Zentrale Risiken & Schutzmaßnahmen
- Bedeutung von KI-Sicherheit für die Zukunft

---

<!-- Sprechertext:
Ich fasse die wichtigsten Punkte zusammen und schließe die Vorlesung ab. Einladung zu Fragen und Diskussion.
-->
