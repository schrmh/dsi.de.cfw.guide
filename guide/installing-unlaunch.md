---
title: Unlaunch installieren
layout: single
sidebar:
  nav: "side"
---

Falls du keine USA-Konsole hast, dann musst du bereits einen DSiWare-Exploit installiert haben, um fortfahren zu können.
{: .notice--info}

Unlaunch befindet sich momentan im Beta-Stadium. Bitte fahre nur mit äußerster Vorsicht fort.
{: .notice--info}

Unlaunch ist ein DSi-Bootcode-Exploit, der es dir erlauben wird, HiyaCFW, eine angepasste Firmware auf deinem DSi zu installieren.

## Downloads
- Die letzte veröffentlichte Version von [Unlaunch](http://problemkaputt.de/unlaunch.zip)
- Die letzte veröffentlichte Version von [HBMenu](https://github.com/devkitPro/nds-hb-menu/releases/){:target="_blank"}
- Die letzte veröffentlichte Version von [ugopwn](/assets/files/ugopwn.zip)
  - Nur für Konsolen der USA-Region
- Die letzte veröffentlichte Version von [twlnf](https://github.com/Jimmy-Z/twlnf/releases){:target="_blank"}
- Die letzte veröffentlichte Version von [Python 3](https://www.python.org/downloads/){:target="_blank"}
- Die letzte veröffentlichte Version von [DSi SRL Extractor](/assets/files/dsi_srl_extract.zip)

## Deine SD-Karte vorbereiten

1. Installiere Python 3 auf deinem Computer
2. Öffne die Systemeinstellungen-App
3. Selektiere **Datenverwaltung > Systemspeicher > Flipnote Studio > Kopieren > Ja**
	- Falls die Datenverwaltung nicht auftaucht, öffne den DSi-Shop, schließe ihn, und versuche es dann erneut
4. Nach Fertigstellung, schalte dein Gerät aus
5. Nehme deine SD-Karte aus deiner Konsole und verbinde diese mit deinem Computer
6. Kopiere den Inhalt des ugopwn `.zip`-Archives zum Rootverzeichnis deiner SD-Karte
  - Nur für USA-Konsolen
7. Kopiere den Inhalt des `.7z`-Archives zum Rootverzeichnis der SD-Karte und benenne `twlnf.nds` in `boot.nds` um
8. Kopiere den Inhalt des  “DSi SRL Extractor“ `.zip`-Archives in einen Ordner auf deinem Desktop
9. Öffne das SD-Speicherkartenlaufwerk auf deinem Computer
10. Navigiere zu  /Private/DS/Title/
11. Kopiere die `.bin`-Datei zu  deinem “DSi SRL Extractor“-Ordner
12. Starte die console_id `.py`-Datei, die sich in dem Ordner befindet
  - Dieses Skript benötigt [WINE](https://www.winehq.org/){:target="_blank"} auf Mac/Linux/*nix-Systemen
13. Wenn aufgefordert, drücke die Enter-Taste
14. Kopiere die neue console_id `.txt`-Datei in der Rootverzeichnis der SD-Karte
15. Werfe deine SD-Karte aus und stecke sie zurück in deinen DSi

## Ein NAND-Backup erstellen

1. Öffne die “Flipnote Studio“-App
  - Stelle sicher, dass *Mit Kalender starten*  in den Einstellungen der App deaktiviert ist
  - Falls du bereits einen anderen DSiWare-Exploit installiert hast, öffne diesen und springe direkt zu Schritt 14
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
14. Wenn aufgefordert, drücke **A** um ein NAND-Backup zu erstellen
  - Dies wird einige Minuten dauern
  - Bewahre dieses NAND-Backup an einer sicheren Stelle auf, denn es ist ein wichtiges Backup, das später bei der Installation von HiyaCFW benötigt wird
15. Drücke **B** um twlnf zu verlassen
  - Deine Konsole wird sich ausschalten

## Installation

1. Verbinde deines Systems SD-Karte mit deinem Computer
2. Kopiere `BOOT.NDS` von dem `hbmenu`-Ordner des HBMenu `.tar.bz2`-Archives zu dem Rootverzeichnis deiner SD-Karte
  - twlnf ist aktuell deine `boot.nds`; für jetzt, benenne die Datei in `boot.bak` oder `twlnf.nds` um
3. Kopiere `UNLAUNCH.DSI` von dem Unlaunch `.zip`-Archiv zu dem Rootverzeichnis deiner SD-Karte
4. Benne `UNLAUNCH.DSI` in `unlaunch.nds` um
5. Trenne deine SD-Karte und stecke sie in deinen DSi
6. Schalte deinen DSi ein und wiederhole Schritt 1 bis 13 in **Ein NAND-Backup erstellen**
  - HBMenu sollte auftauchen
7. Navigiere zu `unlaunch.nds` und drücke **A**
  - Das Installationsprogramm von Unlaunch sollte auftauchen
8. Navigiere zu `INSTALL NOW` und drücke **A**
  - Wenn Unlaunch bei `LOADING FAT` einfriert, dann lese bitte unsere [FAQ](/help/faq)
9. Wenn abgeschlossen, navigiere zu `POWER DOWN` und drücke **A**
  - Dein System wird sich ausschalten
10. Schalte dein System an, um die korrekte Installation von Unlaunch zu verifizieren
  - Du solltest kurz Unlaunchs Bootscreen sehen, und der DSi sollte in eine Version des DSi-Menüs booten, die keine Soundausgabe bietet

Mit einer Installation von Unlaunch hat dein System jetzt einen primitiven Brick-Schutz, bis die TMD-Datei des Launchers zerstört wird. Unlaunch hat Schutzvorkehrungen, die das verhindern sollten und HiyaCFW nutzt deine SD-Karte als den NAND des DSi, was dein System theoretisch unbrickbar macht.

[HiyaCFW installieren](/guide/installing-hiyacfw){: .btn .btn--light-outline}
{: style="text-align: center;"}
