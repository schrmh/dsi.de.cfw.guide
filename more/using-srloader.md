---
title: SRLoader benutzen
layout: single
sidebar:
  nav: "side"
---

nds-bootstrap ist Momentan a im Proof-of-Concept-Stadium und ist bei weitem noch nicht fertig. Erwarte lange Ladezeiten und Kompatibilitätsprobleme. Es wird stark empfohlen, folgende Seite zu lesen und ein Lesezeichen auf sie zu setzen: [Kompatibilitätstabelle](https://docs.google.com/spreadsheets/d/1M7MxYQzVhb4604esdvo57a7crSvbGzFIdotLW0bm0Co/edit#gid=0){:target="_blank"}.
{: .notice--info}

SRLoader ist eine Homebrewanwendung, die Homebrews und Retail-ROMs laufen lassen kann, wofür sie [nds-bootstrap](https://github.com/ahezard/nds-bootstrap){:target="_blank"} nutzt. SRLoader hat zudem verschiedene Emulatoren integriert, wie z.B. “GBA runner“, was das Abspielen von “Gameboy Color“-, NES- und GBA-ROMs ermöglicht.

Mehr über SRLoader erfährst du [hier](https://gbatemp.net/threads/srloader-gui-for-flashcards-also-a-nds-app-for-dsi.472200/){:target="_blank"}.

## Downloads

- The latest release of [SRLoader](https://github.com/Robz8/SRLoader/releases)

## Installation
1. Verbinde die SD-Karte deines Systems mit deinem Computer
2. Kopiere den Content des twlnf `.7z`-Archives in das Root-Verzeichnis deiner SD-Karte
  - Wenn du gefragt wirst, ob du boot.nds ersetzen möchtest, dann stimme zu
3. Kopiere ROMs je nach Typ in entsprechende Ordner
  - Platziere Gameboy-ROMs in `/roms/gb`
  - Platziere NDS-ROMs in `/roms/nds`
  - Platziere NES-ROMs in `/roms/nes`
  - Für GBA-ROMs, erstelle einen Ordner in `roms` mit dem Namen `gba` und platziere sie hier
  - GBA-ROMs benötigen eine Kopie des GBA-BIOS, die `bios.bin` heißt, in dem Root-Verzeichnis deiner SD-Karte. Aktuell können Spielstände von GBA-Spielen nicht gesichert werden.

## Nutzung
1. Öffne SRLoader, indem du einen Homebrew-Eintrittspunkt deiner Wahl nutzt
2. Nun wirst du eine Liste deiner NDS-ROMs sehen
  - Drücke **Y** um Homebrew-Anwendungen ohne nds-bootstrap zu starten
  - Drücke **A** um kommerzielle ROMs und Homebrew-ROMs über nds-bootstrap zu starten (Homebrew mit erweitertem DSi-Header werden nicht durch bootstrap gestartet)
  - Drücke **SELECT**, um eine Spender-ROM zu setzen, wenn die Kompatibilitätsliste danach verlangt
  - Drücke **HOCH** oder **RUNTER** um zwischen NDS-ROMs und DSiWare zu wechseln
  - Drücke **START**, dann navigiere zu “**Start GBARunner2**“, um GBA-ROMs zu starten
  - Drücke **B** um zum DSi-Menü zurückzukehren
