@title[Einführung]

#### Schutz der Privatsphäre
<br>
<br>
<span class="byline">[ code-a.io/privacy-guide ]</span>

Note:
Vorstellung
Bisherige Kenntnisse?
Wollt ihr was bestimmtes lernen?
Jederzeit Fragen! 

---

@title[Vorstellung]
#### code-a.io

  * IT-Kollektiv
  * Entwicklung freier Software
  * Fokus auf IT-Sicherheit für End-Nutzer
  
---

@title[Projekte]

#### Projekte

  * IT-Infrastruktur
  * Privacy Guide
  * YunoHide

---

@title[YunoHide]
#### YunoHide

Server-Betriebssystem für sichere Kollaboration durch Verschlüsselung & Anonymisierung.

  * Stand: Experimentell
  * Mail-Server als Hidden Service
  * XMPP-Server als Hidden Service

---

#### YunoHide: Weitere Ziele

  * Stabilisierung
  * Apps
    * Cryptpad
    * Nextcloud/Seafile
---

@title[Einführung]

#### Schutz der Privatsphäre
<br>
<br>
<span class="byline">[ code-a.io/privacy-guide ]</span>

Note:
Vorstellung
Bisherige Kenntnisse?
Wollt ihr was bestimmtes lernen?
Jederzeit Fragen! 

---

@title[Übersicht]

#### Übersicht

  * Freie vs unfreie Software
  * Passwörter
  * Systemverschlüsselung
  * Anonymisierung
  * Email-Verschlüsselung
  * Verschlüsselte Messenger
<br>
<span class="aside">...</span>

---

@title[Sensibilisierung]

#### Warum Schutzmaßnahmen?

  * Aktive Angriffe  (staatlich/politisch) 
  * Staatliche/Private Überwachung
  * Diebstahl
  * Hausdurchsuchung

#### Probleme

  * Öffentliches WLAN
  * Internetbetreiber kooperieren mit den Cops
  * Metadaten 
  * Unverschlüsselte Seiten

Note:
Linke Anbieter nutzen und unterstützen!
„We kill people based on metadata“ - ehem. NSA-Chef
Probe RequestsBeispiel: Big Data (Spiegelmining)




---

@title[Freie vs unfreie Software]

#### Unfreie/Proprietäre Software
Grobe Definition: Software deren Nutzung aktiv eingeschränkt wird und deren Quelltext nicht einsehbar/änderbar ist.

**Beispiele:**

  * Microsoft Windows
  * MacOS
  * Microsoft Word
  * ...

---

##### Probleme bei proprietärer/unfreier Software

  * **Quelltext nicht einsehbar**
    * Schwierigkeit bei Suche nach Sicherheitslücken/Hintertüren
    * 

---

##### Probleme bei proprietärer/unfreier Software

  * Software nicht legal änderbar
    * Kommerzielle Lizenz -> Sicherheitslücken **dürfen nicht** durch Dritte geschlossen werden.
    * Beispiel: WannaCry und Windows XP

---

##### Probleme bei proprietärer/unfreier Software  

  * Oftmals keine Möglichkeit ungewollte "Updates" zu unterbinden
  * Oftmals keine Möglichkeit ungewünschte Datenweitergabe zu unterbinden

---

#### Auswahl freier Betriebssysteme

  * **Tails:** GNU/Linux optimiert für den Schutz der Privatsphäre
  * Debian/Ubuntu/Mint (kann unfreie Software enthalten)
  * Arch/Manjaro Linux

---

@title[Mobile Plattformen]
#### Mobile Plattformen
Können generell als unsicher eingestuft werden.

  * Updates für ältere Geräte werden nicht gepflegt
  * Unerwünschte Apps

---
#### Mobile Platformen

  * Einschränkungen bei Nutzbarkeit
    * z.B. Eingabe von langen Passwörtern
  * Telefonverschlüsselung fast immer **unsicher**

---

@title[Passwörter]

#### Passwörter

  * Länge wichtiger als Komplexität
  * Keine Zitate
  * Keine aus Zitaten abgeleiteten Passwörter

---
#### Passwörter

  * Passwort-Manager Empfehlung:  KeePassXC
  * Starkes Master-Passwort
  * OpenSource

---

#### Master-Passwort mit Würfel erstellen
**Voraussetzungen:**

  * 6 Würfel
  * EFF SSD Wortliste

**Anleitung mit Links im Anhang**

---

#### Festplatten-/Systemverschlüsselung
  * **Empfohlen**
  * Sollte freie Software sein
  * Bei den meisten GNU/Linux-Systemen schon bei der Installation einrichtbar

---

#### Fall-Beispiel 1: Jeremy Hammond

  * Aktivist, Hacktivist, Antifaschist
  * 24.12.2012: Stratfor-Hack(Privatwirtschaftlicher Geheimdienst)
    * Überweisung von ~1.000.000 USD and das Rote Kreuz 
    * Global Intelligence Files
  * 2013: Verurteilung zu 10 Jahren Haft

---

#### Jeremy Hammond
**Jeremy's Fehler:**

  * **MacOS:** Proprietäre Systemverschlüsselung wurde vom FBI geknackt
  * **Passwort für VeraCrypt-Container:** Chewy1234

---

**Und wenn man alles richtig gemacht hat?**

Was kann dann schon schief gehen?

---

#### Fall-Beispiel 2: Muhammad Rabbani

  * Britischer Aktivist
  * Setzt sich für die Rechte muslimischer Gefangener ein

---

  * 2017: Festnahme am Flughafen wegen der Weigerung der Passwortherausgabe für verschlüsselte Geräte
  * 12 Monate Haft auf Bewährung
  * Geldstrafe

---

#### Die Lage in Deutschland

  * Kein Zwang zur Passwortherausgabe
  * Aber in Zukunft wahrscheinlich mehr Repression

---

#### Reform des Polizeigesetzes in Bayern

**3 Monate Vorbeugehaft ohne richterliche Zustimmung möglich**

---

#### Anonymität

Verhinderung der Verfolgung von Online-Aktivitäten mit Tor

---

#### Wie funktioniert Tor?

<img src="https://www.torproject.org/images/htw2.png">

---

#### Anonym surfen

**Empfehlung: Tor-Browser-Bundle**

Anleitung im Anhang

---

#### Emails Pseudonymisieren

Empfehlung: Thunderbird & TorBirdy

Anleitung im Anhang

---

#### Email-Verschlüsselung mit OpenPGP

  * Öffentliche Schlüssel müssen vorher ausgetauscht werden
  * Nachrichteninhalte sind verschlüsselt
  * Enigmail: Betreff ist auch verschlüsselt

---

#### Email-Verschlüsselung mit OpenPGP

**Empfehlung: Thunderbird & Enigmail**

Anleitung im Anhang

---

#### Verschlüsselte Messenger

Wer benutzt Signal?

---

#### Verschlüsselte Messenger

Wer hat mindestens einmal Fingerprints abgeglichen?

---

#### Still not loving Signal

  * Keine Dezentralisierung
  * Ablehnung von freien Ablegern die auf proprietäre Bestandteile verzichten

---
#### Still not loving Signal

  * Handynummer als ID -> Meta-Daten
  * Kontakte werden an Signal-Server gesendet

---

#### Still not loving Signal

  * Keine Protokoll-Standardisierung
  * Distribution über Google Play
  * Niemand überprüft Fingerabdrücke

#### Verschlüsselte Messenger Alternative

Protokoll:

  * XMPP
  * OMEMO

---

#### Verschlüsselte Messenger Alternative

  * Android: Conversations
  * iOS: ChatSecure
  * Desktop: Gajim + OMEMO-Plugin

---

#### Empfehlungen

  * Privacy Guide: code-a.io/privacy-guide
  * Tails Anleitung: capulcu.blackblogs.org/neu-2
