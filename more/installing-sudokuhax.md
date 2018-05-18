---
title: Sudokuhax installieren
layout: single
sidebar:
  nav: "side"
---

Dieser Guids ist im Moment nur für USA-Konsolen geeignet.
{: .notice--info}

Stelle sicher, dass du mindestens 30 Blöcke an freiem Speicher auf dem internen Speicher deiner Konsole hast. Dein Gerät **wird bricken**, wenn nicht genug Blöcke frei sind.
{: .notice--danger}

Sudokuhax ist ein Exploit für die Sudoku-DSiWare, durch den der Homebrew-Launcher bereits nach wenigen Sekunden, nach Öffnen der DSiWare, starten wird.

To use the [magnet](https://en.wikipedia.org/wiki/Magnet_URI_scheme) links on this page, you will need a torrent client like [Deluge](https://dev.deluge-torrent.org/wiki/Download).

## Was du benötigst
- <i class="fa fa-magnet" aria-hidden="true" title="Dies ist ein Magnet-Link. Benutze einen Torrent-Client, um die dahinterliegende Datei herunterladen zu können."></i> -  [sudokuhax](magnet:?xt=urn:btih:fd4dcb2f954f48adb2af96326609f9c3f3ae2a7a&dn=sudokuhax.zip&tr=http%3a%2f%2ftracker.tfile.me%2fannounce&tr=udp%3a%2f%2f9.rarbg.com%3a2710%2fannounce&tr=udp%3a%2f%2fexplodie.org%3a6969%2fannounce&tr=udp%3a%2f%2ftorrent.gresille.org%3a80%2fannounce&tr=udp%3a%2f%2ftracker.yoshi210.com%3a6969%2fannounce&tr=http%3a%2f%2fexplodie.org%3a6969%2fannounce&tr=http%3a%2f%2ftracker1.wasabii.com.tw%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.coppersurfer.tk%3a6969%2fannounce&tr=udp%3a%2f%2fp4p.arenabg.com%3a1337%2fannounce&tr=http%3a%2f%2ftracker.opentrackr.org%3a1337%2fannounce&tr=udp%3a%2f%2ftracker.tiny-vps.com%3a6969%2fannounce&tr=http%3a%2f%2ftorrent.gresille.org%2fannounce&tr=udp%3a%2f%2ftracker.filetracker.pl%3a8089%2fannounce&tr=http%3a%2f%2ftracker.aletorrenty.pl%3a2710%2fannounce&tr=udp%3a%2f%2fzer0day.ch%3a1337%2fannounce&tr=http%3a%2f%2fp4p.arenabg.com%3a1337%2fannounce&tr=http%3a%2f%2ftracker.baravik.org%3a6970%2fannounce&tr=udp%3a%2f%2ftracker.opentrackr.org%3a1337%2fannounce&tr=udp%3a%2f%2ftracker.aletorrenty.pl%3a2710%2fannounce&tr=udp%3a%2f%2ftracker.leechers-paradise.org%3a6969%2fannounce)

## Vorbereitung

1. Verbinde deine SD-Karte mit deinem Computer
2. Kopiere den Content von sudokuhax `.zip` zum Root-Verzeichnis deiner SD-Karte
3. Trenne deine Karte vom PC und stecke sie in deinen DSi

## twlnf starten
1. Öffne die "Flipnote Studio"-App
  - Stelle sicher, dass *Mit Kalender starten*  in den Einstellungen der App deaktiviert ist
2. Selektiere  **Flipnote ansehen > SD Card > Ordner wählen > User > ugopwn**
3. Klicke auf das Note mit der unteren roten Hälfte
4. Wähle “Bearbeiten”
5. Klicke auf Flipnotes Frosch-Icon, das unten links ist
6. Klicke auf das Filmrollen-Icon
7. Selektiere **Kopieren > Zurück > Beenden**
8. Klicke auf das zweite Note
9. Klicke auf Flipnotes Frosch-Icon, das unten links ist
10. Klicke auf das Filmrollen-Icon
11. Klicke auf den einzelnen rechten Pfeil (der neben dem letzten Pfeil-Icon) zweimal
  - Du wirst nun sehen, wie ein neuer Frame erstellt wird
12. Klicke genau 122x auf den Einfügen-Button
13. Wähle “Löschen” und dann “Einfügen”
  - Dies sollte twlnf ausführen

## Sudokuhax installieren
1. Falls in twlnf aufgefordert, drücke **A** um ein NAND-Backup zu erstellen
  - Dies wird ein paar Minuten dauern
  - Bewahre dieses NAND-Backup an einer sicheren Stelle auf, denn es ist ein wichtiges Backup.
2. Drücke **X** um den NAND direkt zu mounten
  - twlnf listet dies nicht als eine Option
3. Öffne den `sudoku/content`-Ordner
4. Navigiere zu `title.tmd`
5. Drücke **A** um die App in den NAND zu installieren
6. Wenn abgeschlossen, drücke **Select** um twlnf zu verlassen
7. Drücke **A** zum Bestätigen
  - Deine Konsole wird sich nun ausschalten

## Sudokuhax starten

1. Schalte deine Konsole an
2. Öffne die neue Geschenkbox, um Sudoku “auszupacken“
3. Öffne die Software
4. Warte, bis die ESRB- und EA-Bildschirme angezeigt wurden
5. Wenn aufgefordert, dann tippe auf den unteren Bildschirm, um den Entrypoint zu laden

Sudokuhax wird nun die Homebrew von deiner SD-Karte laden, die dort `boot.nds` benannt ist.
