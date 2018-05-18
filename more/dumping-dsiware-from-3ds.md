---
title: DSiWare vom 3DS dumpen
layout: single
sidebar:
  nav: "side"
---

Dieser Guide benötigt einen gehackten 3DS mit [Luma3DS](https://github.com/AuroraWright/Luma3DS){:target="_blank"} und [FBI](https://github.com/Steveice10/FBI){:target="_blank"} installed.
{: .notice--info}

Dieser Guide wird dir erlauben, DSiWare zu kopieren, die du auf deiner DSi-Konsole nutzen kannst. Du wirst einen gehackten 3DS benötigen, der mit Luma3DS läuft. Folge [3ds.hacks.guide](3ds.hacks.guide/de_DE/){:target="_blank"} um deinen 3DS zu hacken.

## TitleID einer DSiWare finden
1. Öffne die Homebrew FBI auf deinem 3DS
2. Scrolle herunter zu "Titles" und drücke **A**
3. Drücke **Select** und dann drücke **A** bei "Show game card" und "Show SD"
4. Drücke **B** und warte dann, bis der Bildschirm aufhört, sich zu bewegen.
5. Scroll zu der DSiWare herunter, die du dumpen möchtest
6. Notiere dir die `Title-ID` der DSiWare, die auf dem oberen Bildschirm angezeigt wird
7. Schalte den 3DS aus

## DSiWare dumpen
1. Schalte deinen 3DS an während du **Start** drückst, um das Chainloader-Menü von Luma3DS zu starten
2. Navigiere zu GodMode9 und drücke **A** um es zu öffnen
3. Navigiere zu `[2:] SYSNAND TWLN/title/00030004`
4. Der Ordner, der das Spiel enthält, welches du kopieren möchtest, ist nach den letzten acht Stellen der Title-ID benannt
5. Drücke **R+A** auf diesem Ordner
6. Wähle "Copy to `0:/gm9/out`"
7. Drücke **A** wenn der Kopiervorgang abgeschlossen ist.
8. Schalte deinen 3DS aus.

Deine gedumpte Kopie sollte sich nun in dem `gm9/out`-Ordner auf der SD-Karte befinden, die in deinem 3DS ist.

Dieser Guide ist noch nicht vollständig. Die nächste Sektion wird dich durch den Installationsprozess von DSiWare auf deinen DSi führen. Bitte schaue zu einem späteren Zeitpunkt nach, um entsprechende Anweisungen zu finden.