---
title: Setup komplettieren
layout: single
sidebar:
  nav: "side"
---

Jetzt werden wir SRLoader ins Systemmenü installieren, indem wir es auf die SD-Karte kopieren.

SRLoader ist eine Homebrewanwendung, die Homebrews und Retail-ROMs laufen lassen kann, und die auch verschiedene Emulatoren mitbringt.

## Downloads

- Die letzte veröffentlichte Version von [SRLoader](https://github.com/Robz8/SRLoader/releases){:target="_blank"}

## Anweisungen

1. Verbinde deine SD-Karte, die den SD-NAND (<2GB) beinhaltet, mit deinem Computer
2. Kopiere *den Inhalt von* `CFW - SDNAND root` des SRLoader `.7z-Archives zum Rootverzeichnis deiner als SD-NAND genutzen (<2GB) SD-Karte.
3. Kopiere die  `_nds`- und `roms`-Ordner des SRLoader `.7z`-Archives zum Root-Verzeichnis deiner SD-Karte
4. Trenne die SD-Karte vom PC und stecke sie in den DSi
5. Schalte deine Konsole an
6. Öffne die neue Geschenkbox, indem du sie antippst
    - SRLoader sollte nun auftauchen

SRLoader sollte nun auf deinem System-Menü sein, so wie es jede andere DSiWare sein sollte. Mit SRLoader kannst du Homebrew-Anwendungen, ROMs von Spielen und verschiedene mitgelieferte Emulatoren ausführen.

## Nutzung

1. Kopiere ROMs je nach Typ in entsprechende Ordner
  - Platziere Gameboy-ROMs in `/roms/gb`
  - Platziere NDS-ROMs in `/roms/nds`
  - Platziere NES-ROMs in `/roms/nes`
  - Für GBA-ROMs, erstelle einen Ordner in `roms` mit dem Namen `gba` und platziere sie hier
  - GBA-ROMs benötigen eine Kopie des GBA-BIOS, die `bios.bin` heißt, in dem Root-Verzeichnis deiner SD-Karte. Aktuell können Spielstände von GBA-Spielen nicht gesichert werden.
2. Öffne SRLoader, indem du einen Homebrew-Eintrittspunkt deiner Wahl nutzt
3. Nun wirst du eine Liste deiner NDS-ROMs sehen
  - Drücke **Y** um Homebrew-Anwendungen ohne nds-bootstrap zu starten
  - Drücke **A** um kommerzielle ROMs und Homebrew-ROMs über nds-bootstrap zu starten (Homebrew mit erweitertem DSi-Header werden nicht durch bootstrap gestartet)
  - Drücke **SELECT**, um eine Spender-ROM zu setzen, wenn die Kompatibilitätsliste danach verlangt
  - Drücke **HOCH** oder **RUNTER** um zwischen NDS-ROMs und DSiWare zu wechseln
  - Drücke **START**, dann navigiere zu “**Start GBARunner2**“, um GBA-ROMs zu starten
  - Drücke **B** um zum DSi-Menü zurückzukehren
