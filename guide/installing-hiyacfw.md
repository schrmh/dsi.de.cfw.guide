---
title: HiyaCFW installieren
layout: single
sidebar:
  nav: "side"
---

Falls du keine USA-Konsole hast, dann musst du bereits einen DSiWare-Exploit installiert haben, um fortfahren zu können.
{: .notice--info}

Du hast [Unlaunch](/guide/installing-unlaunch/) installiert zu haben, bevor du fortfährst.
{: .notice--info}

Lade kein System-Update herunter, nach dem Installieren von HiyaCFW. Dies würde von HiyaCFW erstellte SD-Patches entfernen.
{: .notice--danger}

HiyaCFW ist eine “Custom firmware“ für den “Nintendo DSi“, die nach dem Installieren Folgendes ermöglicht:
- Booten des Systems von einer SD-Karte
- Installieren von Homebrew-Anwendungen zum “Home Menu“
- Starten von bei neueren System-Versionen blockierter Flashkarten

## Anforderungen
- Die neuste Version von [Python 3](https://www.python.org/downloads/){:target="_blank"}
  - Du solltest bereits Folgendes durch die vorherige Sektion haben:
- Eine SD-Karte, die 2GB oder kleiner ist, oder eine größere SD-Karte, die eine Partition hat, die 2GB oder kleiner ist
- Die letzte veröffentliche Version von [twlnf](https://github.com/Jimmy-Z/twlnf/releases){:target="_blank"}
- Die letzte veröffentliche Version von [HiyaCFW](https://github.com/Robz8/hiyaCFW/releases){:target="_blank"}
- Die letzte veröffentliche Version von [ugopwn](/assets/files/ugopwn.zip)
- [NUSDownloader](/assets/files/NUSDownloader.zip)
- Ein Backup des NAND deines Gerätes, inklusive dem NO$GBA-Footer
  - twlnf wird diesen Footer automatisch erstellen, wenn es ein Backup anlegt
  - Du solltest dieses Backup bereits haben, wenn du den Anweisungen der vorherigen Sektion gefolgt bist
- [Hilf-Skripts für die HiyaCFW-Installation](/assets/files/hiyacfw_helper.zip)

## Vorbereitungen
1. Verbinde die <2GB-SD-Karte mit deinem PC
2. Kopiere *den Inhalt* des NUSDownloader `.zip`-Archives zu einem Ordner auf deinem Computer
3. Kopiere *den Inhalt* des HiyaCFW `.7z`-Archives zu einem Ordner auf deinem Computer
4. Kopiere *den Inhalt* des HiyaCFW helper `.7z` zu dem `for PC`-Ordner in deinem HiyaCFW-Ordner
5. Kopiere *den Inhalt* des ugopwn `.zip`-Archives zu dem Root-Verzeicnis deiner <2GB-SD-Karte
6. Kopiere *den Inhalt** des twlnf `.7z`-Archives zu dem Root-Verzeicnis deiner <2GB-SD-Karte, und ändere den Namen der `twlnf.nds` zu `boot.nds`
7. Kopiere `console_id.txt` vom Root-Verzeichnis deiner normalen SD-Karte zu dem Root-Verzeichnis deiner <2GB-SD-Karte
  - Natürlich brauchst du das nur tun, falls deine <2GB-SD-Karte nicht auch deine normale SD-Karte ist
8. Kopiere `nand.bin` und `nand.bin.sha` vom Root-Verzeichnis deiner normalen SD-Karte zu dem Root-Verzeichnis deiner <2GB-SD-Karte
9. Öffne NUSDownloader auf deinem Computer
  - Dies kann durch [Mono](http://www.mono-project.com/) auf Mac/Linux/*nix-System erreicht werden
10. Aktiviere das “Create Decrypted Contents (*.app)”- und deaktiviere das “Keep Enc. Contents”-Kontrollkästchen
11. Selektiere **Database > System (DSi) > System Menu (Launcher) > [Your Region] > v512 > Start NUS Download!**
12. Beende den NUS-Downloader
13. Navigiere zu **titles > 00030017484e41XX > 512** in deinem “NUS Downloader“-Verzeichnis
14. Kopiere `00000002.app` von dem `512`-Ordner zu HiyaCFWs `for PC`-Ordner
15. Kopiere dein valides NAND-Backup (`nand.bin`) Kopiere dein valides NAND-Backup `for PC`-Ordner

## Anweisungen
1. Stecke deine <2GB-SD-Karte in deinen DSi
2. Schalte deine Konsole an
3. Öffne die “Flipnote Studio“-App
  - Stelle sicher, dass *Mit Kalender starten*  in den Einstellungen der App deaktiviert ist
  - Falls du bereits einen anderen DSiWare-Exploit installiert hast, öffne diesen und springe direkt zu Schritt 16
4. Selektiere  **Flipnote ansehen > SD Card > Ordner wählen > User > ugopwn**
5. Klicke auf das Note mit der unteren roten Hälfte
6. Wähle “Bearbeiten”
7. Klicke auf Flipnotes Frosch-Icon, das unten links ist
8. Klicke auf das Filmrollen-Icon
9. Selektiere **Kopieren > Zurück > Beenden**
10. Klicke auf das zweite Note
11. Klicke auf Flipnotes Frosch-Icon, das unten links ist
12. Klicke auf das Filmrollen-Icon
13. Klicke auf den einzelnen rechten Pfeil (der neben dem letzten Pfeil-Icon) zweimal
  - Du wirst nun sehen, wie ein neuer Frame erstellt wird
14. Klicke genau 122x auf den Einfügen-Button
15. Wähle “Löschen” und dann “Einfügen”
  - Dies sollte twlnf ausführen
16. Drücke **X** um den System-NAND direkt zu mounten
17. Drücke **START** um das Menü von twlnf zu öffnen
18. Drücke **R** um den Inhalt des NAND zu der SD-Karte zu kopieren
  - Dies wird einige Minuten dauern
  - Während dieses Prozesses sollte dein System stets mit einem Netzteil aufgeladen werden, um ein plötzliches Ausgehen zu verhindern
  - Wenn `walk returned 0` auftaucht, dann ist der Prozess abgeschlossen
19. Nach Fertigstellung, drücke **Select** um twlnf zu verlassen
20. Drücke **A** zum Bestätigen
  - Deine Konsole wird sich ausschalten
21. Verbinde deine <2GB-SD-Karte mit deinem Computer
22. Verschiebe alle Dateien des `dump`-Verzeichnisses zum Root-Verzeichnis der SD-Karte
  - Dies bereitet den “SD-NAND” vor, von welchem HiyaCFW booten wird
23. Navigiere zu HiyaCFWs `for PC`-Ordner
24. Starte `hiyacfw_helper.py` um Modifikationen vorzubereiten
  - Dieses Skript benötigt [WINE](https://www.winehq.org/){:target="_blank"} auf Mac/Linux/*nix-Systemen
25. Öffne den neuen `Modified Files`-Ordner
26. Kopiere `bootloader.nds` zum Root-Verzeichnis deiner <2GB-SD-Karte
27. Kopiere 00000002.app zu dem **title > 00030017 > 484e41XX > content**-Ordner auf deiner <2GB-SD-Karte
28. Kopiere *den Inhalt* des HiyaCFWs `for 2GB (or lower) SD card (SDNAND)`-Ordner zu dem Root-Verzeichnis der <2GB-SD-Karte
29. Trenne deine <2GB-SD-Karte, und führe sie in deinen DSi ein
30. Schalte deine Konsole ei
  - Der Startbildschirm von HiyaCFW sollte erscheinen

Dein System sollte jetzt von der SD-Karte anstatt vom internen NAND booten.

[Setup komplettieren](/guide/finalizing-setup){: .btn .btn--light-outline}
{: style="text-align: center;"}
