---
marp: true
theme: custom
footer: ![w:280](img/dhbw-ka.svg)

---

<style scoped>
h1 { font-size: 70pt; }
h2 { font-size: 40pt; }
</style>

# DSGVO  
## Aus Sicht eines Informatikers

---

# Ziele der DSGVO

- Schutz personenbezogener Daten  
- Stärkung der Rechte von Betroffenen  
- Vereinheitlichung des Datenschutzrechts in der EU  
- Verpflichtung von Unternehmen zu sicherer Datenverarbeitung  
- Transparenz über Datenflüsse

---

# Was sind personenbezogene Daten?

**Personenbezogene Daten = alle Informationen, die sich auf eine identifizierte oder identifizierbare Person beziehen.**

Beispiele:
- Name, Adresse, E-Mail  
- IP-Adresse  
- Standortdaten  
- Cookies (wenn identifizierend)  
- Nutzerverhalten, Logdaten  
- Gesundheitsdaten, biometrische Daten (besonders sensibel)

---

# Wichtige Rechtsgrundlagen (Art. 6 DSGVO)

## Wann darf man Daten verarbeiten?

- **Einwilligung** (freiwillig, informiert, widerrufbar)  
- **Vertragserfüllung**  
- **Rechtliche Verpflichtung**  
- **Lebenswichtige Interessen**  
- **Öffentliches Interesse**  
- **Berechtigtes Interesse** (mit Interessenabwägung)

**Für Informatiker wichtig:**  
Jedes IT‑System braucht eine dokumentierte Rechtsgrundlage für jede Datenverarbeitung.

---

# Grundprinzipien der DSGVO (Art. 5)

- **Rechtmäßigkeit, Transparenz**  
- **Zweckbindung**  
- **Datenminimierung**  
- **Richtigkeit**  
- **Speicherbegrenzung**  
- **Integrität & Vertraulichkeit**  
- **Rechenschaftspflicht**

Diese Prinzipien müssen sich in Architektur, Logging, Datenmodellen und Prozessen widerspiegeln.

---

# Technische und organisatorische Maßnahmen (TOMs)

Beispiele für Anforderungen:

- Verschlüsselung (Transport + Ruhe)  
- Zugriffskontrollen (RBAC, MFA)  
- Protokollierung & Monitoring  
- Backup & Recovery  
- Pseudonymisierung  
- Minimierung von Datenfeldern  
- Sichere Softwareentwicklung (Secure SDLC)  
- Patch‑ und Schwachstellenmanagement

---

# Privacy by Design & Default (Art. 25)

**Privacy by Design:**  
Datenschutz muss in die Architektur eingebaut sein, nicht nachträglich.

**Privacy by Default:**  
Voreinstellungen müssen datensparsam sein.

Beispiele:
- Opt‑in statt Opt‑out  
- Logging ohne personenbezogene Daten  
- Standardmäßig deaktivierte Tracking‑Funktionen  
- Minimale Datenspeicherung in Datenbanken

---

# Pflichten für IT‑Systeme

- **Verzeichnis von Verarbeitungstätigkeiten**  
- **Datenschutz-Folgenabschätzung (DSFA)** bei hohem Risiko  
- **Meldung von Datenpannen** innerhalb von 72 Stunden  
- **Auftragsverarbeitungsverträge** mit Dienstleistern  
- **Dokumentation aller technischen Maßnahmen**  
- **Löschkonzepte** (automatisiert!)  
- **Rechte der Betroffenen technisch ermöglichen**

---

# Rechte der Betroffenen

IT‑Systeme müssen Funktionen bereitstellen für:

- Auskunft (Welche Daten liegen vor?)  
- Berichtigung  
- Löschung („Recht auf Vergessenwerden“)  
- Einschränkung der Verarbeitung  
- Datenübertragbarkeit  
- Widerspruch  
- Widerruf von Einwilligungen

**Technische Herausforderung:**  
Diese Rechte müssen effizient, sicher und nachvollziehbar umgesetzt werden.

---

# Große DSGVO‑Verstöße

## Meta (Facebook) – 1,2 Mrd. €  
- Unzulässige Datenübermittlung in die USA  
- Fehlende rechtliche Grundlage

## Amazon – 746 Mio. €  
- Unzulässige personalisierte Werbung  
- Mangelhafte Einwilligungsmechanismen

---

# Große DSGVO‑Verstöße

## WhatsApp – 225 Mio. €  
- Intransparente Datenweitergabe an Facebook

## Google – mehrere hundert Mio. €  
- Unklare Einwilligungen, intransparente Datenverarbeitung

## British Airways – 204 Mio. €  
- Datenpanne durch unzureichende Sicherheitsmaßnahmen

---

# Kritik an der DSGVO

## Aus technischer Sicht
- Unklare Begriffe (z. B. „berechtigtes Interesse“)  
- Hoher Dokumentationsaufwand  
- Komplexe Anforderungen an Löschkonzepte  
- Unpraktikable Datenminimierung bei modernen ML‑Systemen  
- Unklare Regeln für Logging und IP‑Adressen  
- Hemmnis für Innovation (z. B. KI‑Forschung)

---

# Kritik an der DSGVO

## Aus wirtschaftlicher Sicht
- Hohe Kosten für Compliance  
- Wettbewerbsnachteil gegenüber nicht‑EU‑Unternehmen

## Aus gesellschaftlicher Sicht
- Uneinheitliche Auslegung durch nationale Behörden  
- Große Unternehmen können Bußgelder „einpreisen“  
- Kleine Unternehmen sind überfordert

---

# Fazit

- DSGVO ist technisch anspruchsvoll, aber zentral für moderne IT‑Systeme  
- Informatiker müssen rechtliche Grundlagen verstehen  
- Datenschutz ist ein Architekturthema, kein Add‑on  
- Gute Dokumentation und Privacy‑by‑Design reduzieren Risiken  
- DSGVO bleibt ein dynamisches, umstrittenes Regelwerk
