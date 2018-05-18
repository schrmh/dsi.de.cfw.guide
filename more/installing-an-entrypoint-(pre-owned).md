---
title: Installieren eines Entrypoints (mit erworbenenen Titeln)
layout: single
sidebar:
  nav: "side"
---

Dieser Guids ist im Moment nur für USA-Konsolen geeignet.
{: .notice--info}

Jetzt werden wir vorbereitete Skripte benutzen, um die Installation von Homebrew-Entrypoints zu vereinfachen. Diese Einstiegspunkte werden uns erlauben, Homebrew innerhalb von Sekunden nach Start der Ziel-Anwendungen zu laden.

Die Benutzung von 4swordshax wird lediglich erlauben, Emulatoren und Homebrew-Anwendungen auszuführen. Falls du auch kommerzielle ROMs mittels SRLoader starten möchtest, dann empfehlen wir dir die Installation von [sudokuhax](/guide/installing-sudokuhax) anstelle von 4swordshax.

## Was du benötigst

* Das [twlnf-Einstiegspunkt-Installations-Paket](/assets/files/twlnf-entrypoint-pack.zip)

## Vorbereitung

1. Verbinde deine SD-Karte mit deinem Computer
2. Kopiere den Content des “twlnf entrypoint installation“ `.zip`-Archives in das Root-Verzeichnis deiner SD-Karte
3. Trenne deine SD-Karte und stecke sie in deinen DSi

## twlnf ausführen

1. Öffne die “Flipnote Studio“-App
  - Stelle sicher, dass *Mit Kalender starten*  in den Einstellungen der App deaktiviert ist
2. Selektiere  **Flipnote ansehen > SD Card > Ordner wählen > User > ugopwn**
3. Klicke auf das Note mit der unteren roten Hälfte
4. Wähle “Bearbeiten”
5. Klicke auf Flipnotes Frosch-Icon, das unten links ist
6. Klicke auf das Filmrollen-Icon
7. Selektiere **Kopieren > Zurück > Beenden**
8. Klicke auf Flipnotes Frosch-Icon, das unten links ist
9. Klicke auf das Filmrollen-Icon
10. Klicke auf den einzelnen rechten Pfeil (der neben dem letzten Pfeil-Icon) zweimal
  - Du wirst nun sehen, wie ein neuer Frame erstellt wird
11. Klicke genau 122x auf den Einfügen-Button
12. Wähle “Löschen” und dann “Einfügen”
  - Dies sollte twlnf ausführen

## Deinen Einstiegspunkt installieren

1. Falls durch twlnf aufgefordert, drücke **A** um ein NAND-Backup anzulegen
  - Dies wird eine Weile dauernd
  - Bewahre dieses NAND-Backup an einem sicheren Ort auf, denn es ist ein sehr wichtiges Backup
2. Drücke **X** um den NAND direkt zu mounten

  - twlnf listet das nicht als Option

3. Navigiere zu dem zu deiner DSiWare passendem .nfs-Skript
  - Fieldrunners - `install_fieldrunhax_usa.nfs`
  - Legends of Exidia - `install_exidiahax_usa.nfs`
  - Guitar Rock Tour - `install_grtpwn_usa.nfs`
  -  The Legend of Zelda: Four Swords Anniversary - `install_4swordshax_usa.nfs`
4. Drücke **A** um das Skript auszuführen
  - Wenn der Probedurchgang fehlschlägt, dann hast du die DSiWare nicht installiert
5. Drücke **A**, um die App in den NAND zu installieren
6. Wenn abgeschlossen, drücke **Select** um twlnf zu verlassen
7. Drücke **A** zum Bestätigen
  - Deine Konsole wird sich nun ausschalten

## Deinen Entrypoint nutzen

1. Schalte deine Konsole an
2. Öffne die ausgenutzte App
3. Folge den zu der App passenden Schritten:
  - Fieldrunners - Warte, bis das Spiel geladen ist und drücke auf **Scores** im Hauptmenü
  - Legends of Exidia - Nach den zwei Startbildschirmen wählst du den ersten Speicherpunkt und drückst auf **Continue**
  - Guitar Rock Tour - Scrolle herunter und drücke auf **High Scores** > **Drums** > **Easy**
  -  The Legend of Zelda: Four Swords Anniversary - Starte einfach das Spiel, denn 4swordshax benötigt keine Benutzerinteraktion

Dein Einstiegspunkt wird nun die Homebrew von deiner SD-Karte laden, die dort `boot.nds` benannt ist.