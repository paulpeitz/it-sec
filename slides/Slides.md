---
marp: true
theme: custom-gaia
footer: ![w:250](img/dhbw-ka.svg)
---
![bg opacity:.1](img/chain.jpg)
# Identity and Access Management (IAM)

## Authentifizierung und Autorisierung

---
![bg opacity:.1](img/chain.jpg)
# Agenda

- Identity & Access Management (IAM)
- Grundlagen: Authentifizierung vs. Autorisierung
- Authentifizierung (1): Passwörter und ihre Schwächen
- Authentifizierung (2): 2-Faktor-Authentifizierung (2FA)
- Authentifizierung (3): FIDO2
- Passkeys statt Passwörter
- Autorisierung (1): Berechtigungsmanagement
- Autorisierung (2): Single Sign-On (SSO)

----
![bg opacity:.1](img/chain.jpg)
## Identity & Access Management (IAM)

IAM ist das Framework aus Richtlinien, Prozessen und Technologien, das sicherstellt, dass die richtigen Entitäten (Benutzer oder Systeme) den richtigen Zugriff auf die richtigen Ressourcen (Daten, Anwendungen) zur richtigen Zeit und aus den richtigen Gründen erhalten.

---
![bg opacity:.1](img/chain.jpg)
## Grundlagen: Authentifizierung vs. Autorisierung

- Authentifizierung (AuthN): Wer sind Sie?
  - Der Prozess der Überprüfung einer Identität.
  - Der Benutzer beweist, dass er derjenige ist, für den er sich ausgibt.
  - Analogie: Das Vorzeigen Ihres Personalausweises an der Tür.

---
![bg opacity:.1](img/chain.jpg)
## Grundlagen: Authentifizierung vs. Autorisierung

- Autorisierung (AuthZ): Was dürfen Sie tun?
  - Der Prozess der Gewährung oder Verweigerung von Rechten.
  - Dieser Schritt erfolgt nach einer erfolgreichen Authentifizierung.
  - Definiert, auf welche Ressourcen (Dateien, API-Endpunkte, Admin-Dashboards) der authentifizierte Benutzer zugreifen darf.
  - Analogie: Eine Hausordnung

---

![bg opacity:.1](img/chain.jpg)
# Authentifizierung

## Wer sind Sie?

---
![bg opacity:.1](img/chain.jpg)
## Grundlagen der Authentifizierung

- Die drei Faktoren der Authentifizierung:
  * Wissen: Etwas, das Sie wissen (Passwort, PIN).
  * Besitz: Etwas, das Sie haben (Smartphone, USB-Token, Smartcard).
  * Sein (Inhärenz): Etwas, das Sie sind (Fingerabdruck, Gesichtsscan, Iris).

---

![bg opacity:.1](img/passwort.jpg)
## Wissen - Passwörter

- Passwörter sind der "klassische" Authentifizierungsfaktor: Wissen
- Das Passwort ist ein Single Point of Failure, der auf Geheimhaltung basiert. 
- Sobald dieses Geheimnis – sei es durch Raten, Phishing oder Leaks – preisgegeben wird, ist die Authentifizierung gebrochen.

---

![bg opacity:.1](img/passwort.jpg)
## Passwörter - Menschliche Schwächen

- Geringe Entropie (Schwache Passwörter)
  - Gängige Wörter ("Passwort", "Sonne")
  - Sequenzen ("123456", "qwertz")
  - Persönliche Daten (Geburtstage, Namen von Kindern oder Haustieren)
  - Keine/Wenige Sonderzeichen

---

![bg opacity:.1](img/passwort.jpg)
## Passwörter - Menschliche Schwächen

- Passwort-Wiederverwendung (Password Reuse)
  - Benutzer verwenden dasselbe (oft schwache) Passwort für Dutzende verschiedene Dienste. 
  - Wird nur ein dieser Dienste kompromittiert, können Angreifer diese Anmeldedaten bei vielen anderen Diensten ausprobieren ("Credential Stuffing").
  - 
---

![bg opacity:.1](img/passwort.jpg)
## Passwörter - Menschliche Schwächen

- Unsichere Aufbewahrung: Das "Wissen" wird oft physisch oder digital unsicher gespeichert – sei es auf einem Post-it am Monitor, in einer unverschlüsselten Textdatei (passwoerter.txt) oder im Browser-Speicher ohne Master-Passwort.
- Mangelndes Bewusstsein für Social Engineering: Benutzer sind anfällig für Phishing-Angriffe, bei denen sie dazu verleitet werden, ihr Passwort auf einer gefälschten Webseite einzugeben.
---
 
## Passwort-Rotation (Änderungsfrequenz)

Wie oft muss ein Passwort geändert werde?

- Ursprüngliche Idee: Falls ein Passwort kompromittiert wurde (z.B. durch Abhören im Netzwerk oder einen Trojaner), soll die Gültigkeitsdauer des gestohlenen Passworts begrenzt werden.
- Warum diese Regel heute oft kontraproduktiv ist:
  - Benutzer, die zur häufigen Änderung gezwungen werden, neigen dazu, minimale Änderungen vorzunehmen (zB. P@ssw0rt_01 -> P@ssw0rt_02).
  - Die kognitive Last führt zu schwächeren, leichter zu merkenden (und damit leichter zu erratenden) Passwörtern.
  - Benutzer schreiben Passwörter auf (z.B. Post-it am Monitor).

---
 
## Passwort-Rotation (Änderungsfrequenz)

Moderne Empfehlung (NIST, BSI):

- Keine erzwungene, periodische Rotation für Benutzerpasswörter.
- Passwörter sollten unbegrenzt gültig sein, solange sie stark sind.
- Änderungspflicht nur bei Anzeichen einer Kompromittierung (z.B. verdächtige Anmeldeversuche, Auftauchen in einem Datenleck).


---

# Passwortregeln (Komplexität)

Das Ziel: Erhöhung der Entropie und Schutz vor Angriffen

- Traditionelle Komplexitätsanforderungen:
  - Mindestlänge (oft 8-12 Zeichen)
  - Mindestens ein Großbuchstabe (A-Z)
  - Mindestens ein Kleinbuchstabe (a-z)
  - Mindestens eine Ziffer (0-9)
  - Mindestens ein Sonderzeichen (z.B. !§$%&?)
  - 
---

# Passwortregeln (Komplexität)

Probleme & Moderne Sichtweise (NIST SP 800-63B):

- Problem: Komplexe Regeln führen oft zu vorhersehbaren Mustern. Ein Benutzer wählt Sommer2024! statt Sommer2023!. Dies ist für Angreifer leicht auszunutzen ("Pattern-based attacks").
- Problem: Menschen können sich komplexe, zufällige Passwörter schlecht merken.
- Moderne Priorität: Länge ist wichtiger als Komplexität. Eine Passphrase (z.B. vier-schoene-baeume-im-garten) ist oft sicherer und leichter zu merken als P@ssw0rt1!.
- Moderne Anforderung: Statt erzwungener Sonderzeichen ist die Prüfung gegen "Blocklists" (bekannte Passwörter, kompromittierte Passwörter, kontextspezifische Wörter wie der Name des Dienstes) entscheidend.


---

