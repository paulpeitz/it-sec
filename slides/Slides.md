---
marp: true
theme: custom-gaia
---
![bg opacity](img/chain.jpg)
# Identity and Access Management (IAM)

---

# Agenda

* Identity & Access Management (IAM)
* Grundlagen: Authentifizierung vs. Autorisierung
* Authentifizierung (1): Passwörter und ihre Schwächen
* Authentifizierung (2): 2-Faktor-Authentifizierung (2FA)
* Authentifizierung (3): FIDO2
* Passkeys statt Passwörter
* Autorisierung (1): Berechtigungsmanagement
* Autorisierung (2): Single Sign-On (SSO)

----
![bg opacity](img/chain.jpg)
## Identity & Access Management (IAM)

IAM ist das Framework aus Richtlinien, Prozessen und Technologien, das sicherstellt, dass die richtigen Entitäten (Benutzer oder Systeme) den richtigen Zugriff auf die richtigen Ressourcen (Daten, Anwendungen) zur richtigen Zeit und aus den richtigen Gründen erhalten.

---
![bg opacity](img/chain.jpg)
## Grundlagen: Authentifizierung vs. Autorisierung

* Authentifizierung (AuthN): Wer sind Sie?
  * Der Prozess der Überprüfung einer Identität.
  * Der Benutzer beweist, dass er derjenige ist, für den er sich ausgibt.
  * Analogie: Das Vorzeigen Ihres Personalausweises an der Tür.

* Autorisierung (AuthZ): Was dürfen Sie tun?
  * Der Prozess der Gewährung oder Verweigerung von Rechten.
  * Dieser Schritt erfolgt nach einer erfolgreichen Authentifizierung.
  * Definiert, auf welche Ressourcen (Dateien, API-Endpunkte, Admin-Dashboards) der authentifizierte Benutzer zugreifen darf.
  * Analogie: Eine Hausordnung

---
![bg opacity](img/chain.jpg)
# Authentifizierung

## Wer sind Sie?

---
![bg opacity](img/chain.jpg)
## Grundlagen der Authentifizierung

* Die drei Faktoren der Authentifizierung:
  * Wissen: Etwas, das Sie wissen (Passwort, PIN).
  * Besitz: Etwas, das Sie haben (Smartphone, USB-Token, Smartcard).
  * Sein (Inhärenz): Etwas, das Sie sind (Fingerabdruck, Gesichtsscan, Iris).

---
![bg opacity](img/passwort.jpg)
## Wissen - Passwörter

* Passwörter sind der "klassische" Authentifizierungsfaktor: Wissen
* Das Passwort ist ein Single Point of Failure, der auf Geheimhaltung basiert. 
* Sobald dieses Geheimnis – sei es durch Raten, Phishing oder Leaks – preisgegeben wird, ist die Authentifizierung gebrochen.

---
![bg opacity](img/passwort.jpg)
## Passwörter - Menschliche Schwächen 1

* Geringe Entropie (Schwache Passwörter)
  * Gängige Wörter ("Passwort", "Sonne")
  * Sequenzen ("123456", "qwertz")
  * Persönliche Daten (Geburtstage, Namen von Kindern oder Haustieren)
  * Keine/Wenige Sonderzeichen

* Passwort-Wiederverwendung (Password Reuse)
  * Benutzer verwenden dasselbe (oft schwache) Passwort für Dutzende verschiedene Dienste. 
  * Wird nur ein dieser Dienste kompromittiert, können Angreifer diese Anmeldedaten bei vielen anderen Diensten ausprobieren ("Credential Stuffing").


---

## 8. Icons

<i class="fa-brands fa-twitter"></i> Twitter: 
<i class="fa-brands fa-mastodon"></i> Mastodon: 
<i class="fa-brands fa-linkedin"></i> LinkedIn: 
<i class="fa fa-window-maximize"></i> Blog: 
<i class="fa-brands fa-github"></i> GitHub: 

---

# 9. <!--fit--> Large Text

---

<!-- Needed for mermaid, can be anywhere in file except frontmatter -->
<script type="module">
  import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@11/dist/mermaid.esm.min.mjs';
  mermaid.initialize({ startOnLoad: true });
</script>

# 10. Mermaid

<div class="mermaid">
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
</div>
