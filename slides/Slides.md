---
marp: true
theme: custom-gaia
footer: ![w:250](img/dhbw-ka.svg)
---
![bg opacity:.1](img/chain.jpg)
# Identity and Access Management (IAM)

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

## Passwörter - Menschliche Schwächen

- Geringe Entropie (Schwache Passwörter)
  - Gängige Wörter ("Passwort", "Sonne")
  - Sequenzen ("123456", "qwertz")
  - Persönliche Daten (Geburtstage, Namen von Kindern oder Haustieren)
  - Keine/Wenige Sonderzeichen

---

## Passwörter - Menschliche Schwächen

- Passwort-Wiederverwendung (Password Reuse)
  - Benutzer verwenden dasselbe (oft schwache) Passwort für Dutzende verschiedene Dienste. 
  - Wird nur ein dieser Dienste kompromittiert, können Angreifer diese Anmeldedaten bei vielen anderen Diensten ausprobieren ("Credential Stuffing").


---

## Mathe

Konzept: Zwei Parteien (Alice und Bob) einigen sich öffentlich auf eine Basis $g$ und einen Modulus $p$. Beide wählen je eine geheime Zahl ($a$ bzw. $b$) und berechnen ihre öffentlichen Werte ($A = g^a \pmod p$ bzw. $B = g^b \pmod p$). Sie tauschen $A$ und $B$ aus. Alice berechnet $K = B^a \pmod p$ und Bob berechnet $K = A^b \pmod p$. Das Ergebnis $K$ ist für beide dasselbe und der geheime gemeinsame Schlüssel, selbst wenn ein Lauscher $A$, $B$, $g$ und $p$ kennt.

---

# 9. <!--fit--> Large Text

---

