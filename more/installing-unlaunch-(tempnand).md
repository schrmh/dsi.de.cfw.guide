---
title: Unlaunch installieren (TempNAND)
layout: single
toc: true
sidebar:
  nav: "side"
---

Wenn du nicht bereits einen DSiWare-Exploit installiert hast, brauchst du entweder eine Konsole der USA-Region, auf der “Flipnote Studio“ installiert ist, oder eine Hardware-Modifikation, mit der sich DSiWare installieren lässt.
{: .notice--info}

Diese Methode tut den NAND **ziemlich beeinflussen** und sollte daher nur als **allerletzte Möglichkeit** in Betracht gezogen werden.
{: .notice--danger}

## Voraussetzungen

- Die letzte veröffentlichte Version von [Unlaunch](http://problemkaputt.de/unlaunch.zip)
- Die letzte veröffentlichte Version von [ugopwn](/assets/files/ugopwn.zip)
  - Nur für USA-Konsolen
- Die letzte veröffentlichte Version von [fwTool](/assets/files/fwTool_1.6.zip)
- Die letzte veröffentlichte Version von [TempNAND](https://github.com/ThisIsDaAccount/TempNand/releases/latest){:target="_blank"}
- Die letzte veröffentlichte Version von [Java](https://java.com/en/download/){:target="_blank"}
- Die letzte veröffentlichte Version von [Python 3](https://www.python.org/downloads/){:target="_blank"}
- Die letzte veröffentlichte Version von [DSi SRL Extractor](/assets/files/dsi_srl_extract.zip)
- Die letzte veröffentlichte Version von [No$GBA](http://problemkaputt.de/gba.htm){:target="_blank"}
- Eine zufällige `.nds`-ROM-Datei

## SD-Karte vorbereiten

1. Kopiere den Content des `.zip`-Archives in das Rootverzeichnis deiner SD-Karte
2. Bennene die fwTool `.nds` in `boot.nds` um
3. Kopiere den Content des `.zip`-Archives in das Rootverzeichnis deiner SD-Karte
  - Nur für USA-Konsolen

## Key-Dateien dumpen

1. Öffne die Systemeinstellungen-App
2. Selektiere **Datenverwaltung > Systemspeicher > Flipnote Studio > Kopieren > Ja**
	- Falls die Datenverwaltung nicht auftaucht, öffne den DSi-Shop, schließe ihn, und versuche es dann erneut
3. Gehe zurück in das DSi-Menü
4. Öffne die “Flipnote Studio“-App
  - Stelle sicher, dass *Mit Kalender starten*  in den Einstellungen der App deaktiviert ist
  - Falls du bereits einen anderen DSiWare-Exploit installiert hast, öffne diesen und springe direkt zu Schritt 17
5. Selektiere  **Flipnote ansehen > SD Card > Ordner wählen > User > ugopwn**
6. Klicke auf das Note mit der unteren roten Hälfte
7. Wähle “Bearbeiten”
8. Klicke auf Flipnotes Frosch-Icon, das unten links ist
9. Klicke auf das Filmrollen-Icon
10. Selektiere **Kopieren > Zurück > Beenden**
11. Klicke auf das zweite Note
12. Klicke auf Flipnotes Frosch-Icon, das unten links ist
13. Klicke auf das Filmrollen-Icon
14. Klicke auf den einzelnen rechten Pfeil (der neben dem letzten Pfeil-Icon) zweimal
  - Du wirst nun sehen, wie ein neuer Frame erstellt wird
15. Klicke genau 122x auf den Einfügen-Button
16. Wähle “Löschen” und dann “Einfügen”
  - Dies sollte twlnf ausführen
14. Wähle die Optionen `Dump CID` und `Dump BIOS`
15. Wähle `Dump  nand_dsi.bin`
  - Dies wird ein paar Minuten beanspruchen
15. Wenn beendet, schalte dein Gerät aus

## Vorbereitungen für TempNAND und No$GBA

1. Downloade und extrahiere das No$GBA `.zip`-Archiv in einen Ordner auf deinem Desktop
2. Verbinde deine SD-Karte mit deinem Computer
3. Öffne den Ordner auf deiner SD-Karte, der scheinbar nach zufälligen Nummern benannt ist
4. Kopiere das DSi-BIOS in den NO$GBA-Ordner
4. Kopiere `nand_dsi.bin` an einen sicheren Ort auf deinem Computer
5. Benenne `nand_dsi.bin` in `clean_nand_dsi.bin` um
6. Kopiere `CID.bin` an einen sicheren Ort auf deinem Computer
7. Kopiere den Inhalt des Unlaunch `.zip`-Archives in einen Ordner auf deinem Desktop
8. Kopiere den Inhalt des “DSi SRL Extractor `.zip`“-Archives in einen Ordner auf deinem Desktop
9. Navigate zu /Private/DS/Title/ auf deiner SD-Karte
10. Kopiere die `.bin`-Datei zu deinem “DSi SRL Extractor“-Ordner
11. Starte die `console_id.py`-Datei, die sich in diesem Ordner befindet
  - Dieses Skript benötigt [WINE](https://www.winehq.org/){:target="_blank"} auf Mac/Linux/*nix-Systemen
12. Wenn aufgefordert, drücke die Eingabetaste
13. Kopiere die neue `console_id.txt`-Datei zu einem sicheren Ort auf deinem Computer

## TempNAND benutzen

1. Downloade und extrahiere das TempNAND `.zip`-Archiv
2. Starte die TempNAND `.jar`-Datei
  - Stelle sicher, dass du Java installiert hast
3. Navigiere zum Setup-Tab
4. Selektiere **Console ID > get Console ID from file**
5. Selektiere die vorher erstellte `console_id.txt`-Datei
6. Selektiere **CID > get CID from file**
7. Selektiere die vorher erwähnte `CID.bin`-Datei
8. Selektiere **File > Open Encrypted NAND**
9. Selektiere die vorher erwähnte `clean_nand_dsi.bin`-Datei
  - Dies braucht vielleicht ein paar Sekunden
  - Falls es so aussieht, als ob der Prozess eingefroren ist, dann warte lieber ein bisschen
10. Selektiere "Install Unlaunch"
11. Selektiere `unlaunch.dsi`, die du zuvor von Unlaunch `.zip` extrahiert hast
12. Selektiere **File > Save As**
13. Sichere eine Kopie deines NAND-Backups für spätere Zwecke
14. Benenne es in `unlaunch_nand_dsi.bin` um
15. Selektiere **File > Save for No$GBA**
16. Speichere eine Datei in den NO$GBA-Ordner
17. Benenne das No$GBA-NAND-Backup in `DSI-1.mmc`um

## NAND testen

1. Öffne No$GBA
2. Selektiere **Options > Emulation Setup**
3. Setze "Reset/Startup Entrypoint" zu "GBA/NDS BIOS (Nintendo Logo)"
4. Setze "NDS Mode Colors" zu "DSi (retail/16MB)"
5. Selektiere **Save Now > OK**
6. Selektiere **File >> Cartridge Menu (FileName)**
7. Öffne die `.nds`-Datei

Dein NAND sollte nun von No$GBA emuliert werden. Falls es nicht funktioniert, ist das NAND-Backup wahrscheinlich fehlerhaft und es sollte nicht auf deinen DSi geflasht werden.
Wenn das Backup ohne Probleme in No$GBA läuft, dann kannst du zur nächsten Sektion des Guides gehen.

## NAND wieder einspielen

1. Kopiere die `unlaunch_nand_dsi.bin`-Datei zurück in den Ordner auf deiner SD-Karte, der durch fwTool erstellt wurde
2.Lösche die `nand_dsi.bin`-Datei von deiner SD-Karte
  - Stelle sicher, dass du immer noch das originale Backup auf deinem Computer hast!
3. Benenne `unlaunch_nand_dsi.bin` in `nand_dsi.bin` um
4. Öffne die “Flipnote Studio“-App
  - Stelle sicher, dass *Mit Kalender starten*  in den Einstellungen der App deaktiviert ist
  - Falls du bereits einen anderen DSiWare-Exploit installiert hast, öffne diesen und springe direkt zu Schritt 14
5. Selektiere  **Flipnote ansehen > SD Card > Ordner wählen > User > ugopwn**
6. Klicke auf das Note mit der unteren roten Hälfte
7. Wähle “Bearbeiten”
8. Klicke auf Flipnotes Frosch-Icon, das unten links ist
9. Klicke auf das Filmrollen-Icon
10. Selektiere **Kopieren > Zurück > Beenden**
11. Klicke auf das zweite Note
12. Klicke auf Flipnotes Frosch-Icon, das unten links ist
13. Klicke auf das Filmrollen-Icon
14. Klicke auf den einzelnen rechten Pfeil (der neben dem letzten Pfeil-Icon) zweimal
  - Du wirst nun sehen, wie ein neuer Frame erstellt wird
15. Klicke genau 122x auf den Einfügen-Button
16. Wähle “Löschen” und dann “Einfügen”
  - Dies sollte twlnf ausführen

17. Wähle "Restore `nand_dsi.bin`"
  - Dies wird ein paar Minuten dauern
18. Nachdem der Prozess beendet ist, schalte deine Konsole aus

Mit einer Installation von Unlaunch hat dein System jetzt einen primitiven Brick-Schutz, bis die TMD-Datei des Launchers zerstört wird. Unlaunch hat Schutzvorkehrungen, die das verhindern sollten und HiyaCFW nutzt deine SD-Karte als den NAND des DSi, was dein System theoretisch unbrickbar macht.

[HiyaCFW installieren](/guide/installing-hiyacfw){: .btn .btn--light-outline}
{: style="text-align: center;"}
