# Privacy Guide

- [Software](#software)
  * [System-Verschlüsselung](#system-verschl-sselung)
  * [Passwort-Manager: KeepassXC](#passwort-manager--keepassxc)
  * [Anonym Surfen: Tor-Browser](#anonym-surfen--tor-browser)
  * [OpenPGP verschlüsselte Emails: Thunderbird & Enigmail](#openpgp-verschl-sselte-emails--thunderbird---enigmail)
  * [Pseudonymiserte Emails: TorBirdy](#pseudonymiserte-emails--torbirdy)
  * [OMEMO-verschlüsselt chatten: Conversations & ChatSecure](#omemo-verschl-sselt-chatten--conversations---chatsecure)
  * [Verschlüsselte Container: VeraCrypt](#verschl-sselte-container--veracrypt)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>


**Themen**

  * Freie Betriebssysteme
  * Desktop vs. Mobile OS
  * Freie Software
  * Passwörter: https://www.eff.org/dice
  * Full-Disk-Encryption
  * Tor-Browser zum Surfen
  * Email-Verschlüsselung
  * Chat-Verschlüsselung mit XMPP+OMEMO

# Software
## System-Verschlüsselung
//TODO:

## Passwort-Manager: KeepassXC
**Installation:**

KeepassXC unter folgender Adresse herunterladen und installieren: https://keepassxc.org

**Einrichtung:**

  * KeepassXC starten
  * Eine neue Passwort-Datenbank anlegen
  * Passwörter hinzufügen/bearbeiten/generieren

**Firefox-Addon:**

Um Passwörter direkt in Webseiten einfügen zu lassen und neue Passwörter direkt im Browser genereiren und speichern zu lassen kann KeepassXC-Browser installiert werden.

Das Addon ist unter folgender Adresse zu finden: https://addons.mozilla.org/de/firefox/addon/keepassxc-browser/

## Anonym Surfen: Tor-Browser
**Installation:**

//TODO:

## OpenPGP verschlüsselte Emails: Thunderbird & Enigmail

**Schritt 1:** Thunderbird herunterladen und installieren

Lade dir Thunderbird von der folgenden Seite herunter und installiere es anschließend:

https://www.mozilla.org/thunderbird/


**Schritt 2:** Enigmail herunterladen und installieren

Öffne Thunderbird und klicke auf das Menü-Symbol in der oberen rechten Ecke.

Klicke dann im Menü auf den Eintrag “Addons”. Wähle auf der darauf folgenden Seite im linken Bereich “Erweiterungen” bzw. ”Extensions” aus.

Gebe anschließend in der Suchleiste oben rechts “Enigmail” ein und installiere das Addon.

Starte Thunderbird nach der Installation neu.


**Schritt 3:** Schlüsselpaar erzeugen

Nach dem Neustart von Thunderbird sollte der Installationsassistent von Enigmail automatisch starten. Falls nicht, starte ihn über Menü → Enigmail → Einrichtungsassistent. Nutze bei der Einrichtung die Standardoptionen außer bei folgenden Punkten:

  * Im Schritt “Verschlüsselung”, wähle “Verschlüssle alle meine Nachrichten”
  * Im Schritt “Unterschreiben”/”Signatur”, wähle “Meine nachrichten sollen nicht standardmäßig unterschrieben werden”
  * Im Schritt “Schlüsselauswahl”, wähle “Ich möchte ein neues Schlüsselpaar erzeugen”
  * Im Schritt “OpenPGP-Schlüssel erzeugen” sollte ein starkes Passwort verwendet werden, das von einem Passwort-Manager erzeugt wurde.


Der Schritt “Schlüsselerzeugung” wird einige Minuten dauern. Während dieses Schrittes sollte der Computer für andere Dinge, z.B. zum Surfen, genutzt werden, da hierdurch der Schlüssel schneller generiert wird.

Klicke im Schritt “Enigmail-Bestätigung” auf Zertifikat erzeugen und speichere es in deinem Benutzerverzeichnis in einem Ordner mit dem Namen “Widerrufszertifikat”.


**Schritt 4:** Öffentlichen Schlüssel weitergeben

**Schritt 4.1:** als Email-Anhang

Der einfachste Weg deinen Schlüssel weiterzugeben ist, diesen als Anhang in einer Email zu versenden. Falls du den Schlüssel auf diese Weise weitergibst, sollte der Empfänger anschließend den Fingerabdruck des Schlüssels überprüfen.

Mehr dazu unter “Schritt 5: Öffentliche Schlüssel importieren & verifizieren”.


**Schritt 4.2:** über Schlüssel-Server

Schlüssel-Server stellen ein Verzeichnisse dar, über die OpenPGP-Schlüssel veröffentlicht  und abgerufen werden können. Zusätzlich synchronisieren sich die meisten Schlüssel-Server mit anderen Schlüssel-Servern.

Achtung: Jeder kann einen Schlüssel für eine beliebige Email-Adresse auf normalen Schlüssel-Servern veröffentlichen.

Bisher gibt es nur wenige Schlüssel-Server die überprüfen, ob die Person die einen Schlüssel hochlädt auch den zugehörigen privaten Schlüssel besitzt und ob diese auch Zugriff auf das Email-Konto hat. Diese Schlüssel-Server sollten allerdings gegenüber der klassischen Schlüssel-Server bevorzugt werden.

Einer dieser Server ist hkps://keys.mailvelope.com

### Anleitung: Öffentlichen Schlüssel auf Schlüssel-Server veröffentlichen

Wähle im Thunderbird-Menü Enigmail → Schlüssel verwalten aus.
Wähle deinen Schlüssel mit einem Rechtsklick aus und klicke auf “Öffentliche Schlüssel in die Zwischenablage kopieren”.
Rufe im Browser die folgende Adresse auf:  https://keys.mailvelope.com/demo.html

Füge deinen Schlüssel mit Rechtsklick → Einfügen in das Textfeld unter “OpenPGP Key Upload” ein und klicke anschließend auf den Button “Upload”.

Anschließend sollte in Thunderbird eine neue Email mit dem Betreff “Verify Your Key” ankommen. Öffne die Email in dem du sie anklickst und danach das Passwort für deinen OpenPGP-Schlüssel eingibst um die Email zu entschlüsseln.

Öffne anschließend den Link in der Email.
Auf der geöffneten Seite sollte nun “Email address successfully verified!” stehen mit einem zusätzlichen Link, mit dem du deinen Schlüssel teilen kannst.


**Schritt 5:** Öffentliche Schlüssel importieren & verifizieren

Um einen öffentlichen Schlüsel zu importieren kannst du diesen:

  * falls er per email zugesendet wurde: direkt mit einem rechtsklick darauf importieren oder
  * falls der Schlüssel auf andere Weise empfangen wurde(z.B. über schlüssel-Server): Durch das Öffnen von Menü → Enigmail → Schlüsselverwaltung → Schlüssel importieren.

Um einen Schlüssel zu verifizieren rufst du am besten die Person zu der der Schlüssel   gehört an und gleichst mit der Person den Fingerprint des Schlüssels ab. Den Fingerprint   des Schlüssels kannst du dir unter Menü → Enigmail → Schlüsselverwaltung anzeigen lassen. Schlüssel sollten verifiziert werden, um sicher zu stellen das ein Angreifer den Schlüssel  beim Transport nicht ausgetauscht hat.

## Pseudonymiserte Emails: TorBirdy

//TODO:


## OMEMO-verschlüsselt chatten: Conversations & ChatSecure

### Android: Conversations

#### Installation
  * Auf dem Gerät unter *Einstellungen -> Sicherheit -> Unbekannte Herkunft(Installation von Apps aus unbekannten Quellen zulassen)* **aktivieren**
  *  Die F-Droid-App von f-droid.org herunterladen
  * Die F-Droid-App öffnen und dort die App “Conversations” suchen und installieren

#### Account einrichten

Übersicht kostenloser Jabber/XMPP-Anbieter:
  * systemli.org (Registrierung nur über Web-Interface)
  * jabber.ccc.de
  * jabber.de

Conversations starten und die Jabber-ID(ähnelt einer Email-Adresse) und das Passwort eintragen.

Falls du das Konto noch nicht registriert hast zusätzlich den Haken bei **Neues Konto auf Server erstellen** setzen.


#### Kontakte hinzufügen
Um eine verschlüsselte Kommunikation starten zu können solltest du als erstes Kontakte hinzufügen.

Gehe dazu über das Menü oben rechts auf + und anschließend auf das zweite Symbol von rechts.
Gebe anschließend die Jabber-ID des Kontakts ein und klicke auf OK.

#### Verschlüsselte Konversation & Schlüssel-Verifizierung

Mit einem Klick auf den Kontakt in der Kontaktliste kann eine neue Konversation gestartet werden. Wenn das Gesprächsfenster geöffnet wurde sollte man als erstes auf das Schloss- Symbol drücken und anschließend OMEMO auswählen.

Falls das nicht möglich ist muss als erstes OTR ausgewählt werden und nach einer ersten Testnachricht auf OMEMO umgeschaltet werden.

Anschließend sollte der Schlüssel verfiziert werden. Folgende Optionen stehen dafür zur Verfügung:

  * **SMP:** Mit SMP muss eine der beiden Personen eine Frage stellen und die Antwort zu der Frage eingeben. Die andere Person bekommt dann die Frage zugesendet und muss diese beantworten. Die Antwort muss hierbei nicht komplex sein, da die andere Person nie die Klartext-Antwort erhält.

  * **Fingerprints vergleichen:** Alternativ zu SMP können auch die Fingerprints verglichen werden zum Beispiel per Telefon

## Verschlüsselte Container: VeraCrypt

//TODO:

# Weitere Links
**Surveillance Self-Defense | Electronic Frontier Foundation:** https://ssd.eff.org/en
