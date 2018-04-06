# Privacy Guide

- [Präsentation](#pr-sentation)
- [Master-Passwort](#master-passwort)
  * [Master-Passwort mit Würfeln erstellen](#master-passwort-mit-w-rfeln-erstellen)
- [Software](#software)
  * [System-Verschlüsselung](#system-verschl-sselung)
  * [Passwort-Manager: KeepassXC](#passwort-manager--keepassxc)
  * [Anonym Surfen: Tor-Browser](#anonym-surfen--tor-browser)
  * [OpenPGP verschlüsselte Emails: Thunderbird & Enigmail](#openpgp-verschl-sselte-emails--thunderbird---enigmail)
    + [Anleitung: Öffentlichen Schlüssel auf Schlüssel-Server veröffentlichen](#anleitung---ffentlichen-schl-ssel-auf-schl-ssel-server-ver-ffentlichen)
  * [Pseudonymiserte Emails: TorBirdy](#pseudonymiserte-emails--torbirdy)
  * [OMEMO-verschlüsselt chatten: Conversations & ChatSecure](#omemo-verschl-sselt-chatten--conversations---chatsecure)
    + [Android: Conversations](#android--conversations)
      - [Installation](#installation)
      - [Account einrichten](#account-einrichten)
      - [Kontakte hinzufügen](#kontakte-hinzuf-gen)
      - [Verschlüsselte Konversation & Schlüssel-Verifizierung](#verschl-sselte-konversation---schl-ssel-verifizierung)
    + [iOS: ChatSecure](#ios--chatsecure)
  * [Verschlüsselte Container: VeraCrypt](#verschl-sselte-container--veracrypt)
- [Weitere Links](#weitere-links)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>



# Präsentation

[gitpitch.com/code-a/privacy-guide](https://gitpitch.com/code-a/privacy-guide)


# Master-Passwort

## Master-Passwort mit Würfeln erstellen

Benötigtes Material:

  * 5 Würfel
  * Folgende Wortliste: https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt

**Generierung des Passworts:**

  * Die Würfel nehmen und alle 5 Würfel gleichzeitig würfeln
  * Die gewürfelten Zahlen in einer Reihe aufschreiben z.B. 4, 1, 4, 3, 5
  * Weitere 5 Mal mit den 5 Würfeln würfeln und die Zahlen bei jedem durchgang in einer neuen Zeile aufschreiben
  * Die Wortliste öffnen und zu jeder 5 stelligen Zahl das zugehörige Wort aufschreiben
  * Ihr solltet anschließend 6 Wörter aufgeschrieben haben, so dass ihr ein langes Grundpasswort ähnlich dem Folgenden habt:
    * panoramic nectar precut smith banana handclap
  * Dieses Passwort hat bereits eine Komplexität von etwa 72 Bit
  * Anschließend die Komplexität durch das Einstreuen von Zahlen und Sonderzeichen zwischen den Wörtern erhöhen, z.B.
    * 1panoramic7nectar!precut/smith#banana_handclap
  * Als letzten Schritt muss man sich das Passwort noch merken :(... Methoden:
    * Eselsbrücke
    * Passwort pauken bis es im Kopf ist
    * ...

*Quelle: https://www.eff.org/dice*

# Software
## System-Verschlüsselung
Die System-Verschlüsselung sollte direkt bei der Installation des Betriebssystems aktiviert werden.

Die meisten GNU/Linux-Distributionen unterstützen das Einrichten der System-Verschlüsselung/Full disk encryption bei der Installation. Hierzu zählen unter Anderem:

  * Debian
  * Ubuntu (enthält proprietäre Bestandteile)
  * Mint (enthält proprietäre Bestandteile)
  * Manjaro

**Von der Verwendung von proprietären Betriebssystemen und System-Verschlüsselungen ist dringend abzuraten!**

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

**Schritt 1:** Herunterladen und Installation

Lade dir den tor-Browser von der folgenden Seite herunter und installiere ihn anschließend:

https://www.torproject.org/projects/torbrowser.html


**Schritt 2:** Tor-Browser starten

Starte den Tor-Browser anschließend. Beim Starten wird es einen kurzen moment dauern bis eine Verbindung zum Tor-Netzwerk aufgebaut ist.
Du solltest mit einer Seite begrüßt werden, die dir mitteilt das du mit dem Tor-Netzwerk verbunden bist.

Wenn das der Fall ist kannst du anschließend anonym mit dem Tor-Browser surfen, jedoch mit den folgenden Einschränkungen:
  * Javascript ist deaktiviert, daher kann es sein das manche Seiten nicht richtig funktionieren
  * Die Verbindung ist langsam
  * Du solltest dich nicht in Accounts einloggen, die persönliche Informationen über dich preisgeben, da deine Anonymität dadurch stark gefährdet wird.



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

**Schritt 1:** TorBirdy installieren

TorBirdy von folgender Adresse herunterladen: https://addons.mozilla.org/de/thunderbird/addon/torbirdy/

Anschließend Thunderbird starten und über das "Katalog-Symbol" in der oberen rechten Ecke den Punkt "Add-ons" anklicken.

Danach in dem neu geöffneten Tab im Menü "Erweiterungen/Extensions" auswählen.
Mit einem Klick auf das "Zahnrad-Symbol"->"Add-on aus Datei installieren/Install Add-on from file" die heruntergeladene Datei auswählen und installieren.

**Schritt 2:** TorBirdy nutzen

Sobald TorBirdy aktiviert ist können die Emails nur noch über das Tor-Netz abgerufen werden. Daher ist es notwendig Tor/Tor-Browser während der Nutzung von Thunderbird laufen zu lassen.

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

### iOS: ChatSecure

//TODO:


## Verschlüsselte Container: VeraCrypt

**Schritt 1:** Installation von VeraCrypt

Lade dir VeraCrypt von der folgenden Seite herunter und installiere es:  https://sourceforge.net/projects/veracrypt/


**Schritt 2:** Container/Volume anlegen

Öffne VeraCrypt und klicke auf den Button Neues Volume erstellen. Wähle anschließend Einen verschlüsselten Datei-Container erstellen aus.
Im nächsten Fenster Standard VeraCrypt Volume auswählen und anschließend den Speicherort angeben. Bei Verschlüsselungsoptionen können die Voreinstellungen verwendet werden.
Bei der Eingabe der Größe des Volume sollte beachtet werden, dass diese später nicht mehr geändert werden kann. Daher sollte man hier zur Sicherheit eher einen größeren Wert eintragen.

Das Passwort für das Volume sollte möglichst lang und komplex sein, weshalb hierfür ein Passwort-Manager z.B. Keepass zu empfehlen ist.

Bei Formatierungsoptionen können ebenfalls die Voreinstellungen übernommen werden. Im nächsten Schritt muss der Mauszeiger im Fenster über einen längeren Zeitraum zufällig bewegt werden bis der obere Balken vollständig gefüllt ist.

Klicke anschließend auf den Formatieren Button um die Erstellung abzuschließen.
Nach der erstellung können entweder weitere Container/Volumes erstellt werden oder der Assistent beendet werden.

**Schritt 3:** Container/Volume einbinden

Um den verschlüsselten Container/Volume nutzen zu können muss dieser eingebunden werden. Wähle hierfür in der Liste einen Slot aus und wähle im unteren Bereich mit einem Klick auf Datei das zuvor erstellte Volume aus.
Klicke auf den Button Einbinden und gebe anschließend das Passwort für das Volume ein. Danach sollte das Volume automatisch als Laufwerk in der Dateiverwaltung erscheinen und kann verwendet werden um dort Dateien und Verzeichnisse abzulegen oder zu bearbeiten.

Wenn du mit der Arbeit an den Dateien im Volume fertig bist schließe diesen wieder mit dem Button Aushängen.

# Weitere Links
**Surveillance Self-Defense | Electronic Frontier Foundation:** https://ssd.eff.org/en
