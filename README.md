# Luki angeln

Ein kleines Angelspiel direkt im Browser.

## Starten

Öffne [index.html](./index.html) im Browser. Es ist keine Installation und kein Build-Schritt nötig.

## Optik-Update

Die gesamte Spieloberfläche wurde visuell überarbeitet:
- Der Angler hat jetzt eine gezeichnete Figur mit Gesicht, Mütze, Jacke und Armen.
- Das Boot hat einen detaillierteren Holzkörper, Planken, Sitz, Laterne, Flagge und eine ausgearbeitete Angel.
- Die Fische haben neue Körperformen, Flossen, Muster, Schuppen-Highlights, Augen und Mutations-Leuchteffekte.
- Die Seen haben Wolken, Insel-Silhouetten, Lichtstrahlen, Wasserreflexe und Unterwasser-Partikel.
- Der Fischfang zeigt eine eigene Timing-Konsole mit leuchtender Trefferzone, Fortschrittsmarkern und drei Leben.
- Der Piratenkampf zeigt ein gezeichnetes Schiff mit Segeln, Totenkopfflagge, Mond, Meer und animiertem Ziel-Fadenkreuz.
- Shop, Index, Fangkarte und Schatzkiste haben neue Glas-, Metall- und Licht-Effekte, stärkere Karten und überarbeitete Buttons.
- Die Schatzkiste hat zusätzliche Leucht- und Öffnungseffekte.

## Spielsysteme

Es gibt sechs Seltenheitsstufen: Normal, Selten, Sehr selten, Unmöglich, Legendär und Mythisch. Die Sammlung enthält 91 verschiedene Fische über den normalen See, die Aurora-Welt und das Korallenriff.

Jede Seltenheit startet im Angel-Minispiel mit genau **3 Leben**.

Bei jedem erfolgreichen Fang gibt es eine feste **5%-Chance** auf eine Schatzkiste. Während des Events „Schatzflut“ steigt die Chance auf 8%. Glücks-Upgrades verändern diese Chance nicht. Eine Kiste enthält zufällig 25% des aktuellen Geldbestands (mindestens 50 Münzen), 25 Glücksköder oder 10 zufällige Upgrade-Stufen, soweit noch verfügbar.

Ein Piratenschiff taucht in zufälligen Abständen zwischen **10 Sekunden und 5 Minuten** auf. Im Kampf müssen 7 schrumpfende Zielscheiben in 30 Sekunden getroffen werden; höchstens 3 Fehlschüsse sind erlaubt. Ein Sieg zahlt 7% aller bisher verdienten Münzen aus. Bei einer Niederlage geht der aktuelle Münzbestand verloren.

Die Fangkarte zeigt Seltenheitschance, Mutationschance und die kombinierte Fangchance inklusive Mutation an.

## Quests

- Es gibt insgesamt **30 Aufgaben** in zehn Abschnitten. Du hast immer 3 aktive Quests gleichzeitig; erst wenn alle drei eingelöst wurden, erscheinen die nächsten drei.
- Aufgaben reichen vom Fischefangen und Verkaufen bis zu seltenen Fischen, Mutationen und gigantischen Fängen.
- Fertige Aufgaben kannst du über **📜 Quests** unten links einlösen. Münzen werden direkt gutgeschrieben.
- Fischbelohnungen zeigen einen Zufalls-Spin mit auslaufender Drehgeschwindigkeit, Lichtstrahlen, leuchtenden Ringen und einer großen Gewinn-Enthüllung. Mit jeder schwierigeren Quest steigen die Chancen auf seltene, legendäre und mythische Fische. Der gewonnene Fisch landet nach dem Spin im Fangbestand.
- Nach einem Fang spricht der Angler in einer Sprechblase: „Ich warte hier, bis ich nochmal geworfen habe!“ Die Blase bleibt bis zum nächsten Wurf sichtbar.
- Nach allen 30 Aufgaben gibt es einen zusätzlichen Münzbonus. Beim Rebirth beginnt die Quest-Reihe wieder von vorn.
- Quest-Abschnitt, Fortschritt und eingelöste Belohnungen werden lokal mit dem restlichen Spielstand gespeichert.
- Der Angler kommentiert jetzt häufiger besondere Größen und Seltenheiten, Mutationen, Events sowie Regen und Wetterwechsel.
- Der normale Fangmoment hat jetzt eine mehrstufige Reveal-Sequenz mit dunkler werdendem Hintergrund, magischen Energie-Ringen, rotierenden Lichtstrahlen, Partikel-Sog und einer großen Schockwelle beim Auftauchen des Fisches.
- Die Fang-Animation wurde für flüssigere Darstellung optimiert: Die Effekt-Ebene rendert mit geringerer interner Auflösung, Partikelmengen und zusätzliche Funken sind begrenzt und Leuchteffekte werden nur noch bei ausgewählten Partikeln berechnet.
- Der Angler hat eine Sprechpause und kommentiert Fänge, Wetter und Events deutlich seltener. Auch die Sprechblase nach dem Fang erscheint nur gelegentlich.
- Die Fangkarte bekommt einen kräftigen Auftritt mit schwebendem Fisch, animiertem Seltenheits-Badge und nacheinander eingeblendeten Fangdetails. Je seltener der Fang und je höher die Mutation, desto länger und spektakulärer wird die Enthüllung.

## Spielstand

Der Spielstand wird lokal im Browser über `localStorage` gespeichert und nicht automatisch zwischen Geräten synchronisiert.

## Admin-Menü, Tageszeit und Wetter

- Sieben schnelle Klicks auf die Münzanzeige öffnen das geheime Admin-Menü.
- Im Admin-Menü lassen sich der Münzbestand und der Glückswert einstellen. Der Glückswert beeinflusst seltene Fische und Mutationen ab dem nächsten Wurf.
- Eine Schatztruhe kann für den nächsten erfolgreichen Fang vorgemerkt werden.
- Ein Piratenüberfall kann direkt gestartet werden.
- Im Spiel wechseln Tag und Nacht automatisch in einem Zyklus von ungefähr drei Minuten.
- Gelegentlich setzt Regen ein. Währenddessen werden die Wellen höher und das Boot schaukelt stärker.

## Geld-Eimer

- Im Laden gibt es einen Geld-Eimer mit maximal **5 Fischen**.
- Gefangene Fische können aus dem Fangbestand in freie Eimerplätze gesetzt und später wieder herausgenommen werden.
- Jeder eingesetzte Fisch bringt automatisch Münzen pro Sekunde. Je höher seine Seltenheit, desto höher das Einkommen; Gold-, Diamant- und Rainbow-Mutationen erhöhen es zusätzlich.
- Das Einkommen läuft auch weiter, wenn ein Menü geöffnet ist, und der Eimer-Spielstand wird lokal gespeichert.
- Grundverdienst pro Sekunde: Normal 0,10; Selten 0,25; Sehr selten 0,70; Unmöglich 2; Legendär 6; Mythisch 18 Münzen. Mutations-Multiplikatoren: normal x1, Gold x1,5, Diamant x2,5, Rainbow x4.

## Behalten und Start-Tutorial

- Mit **Behalten** wird ein Fisch automatisch in einen freien Platz des Geld-Eimers verschoben.
- Der Geld-Eimer fasst maximal **5 Fische**. Ist er voll, bleibt der neue Fisch im normalen Fangbestand und kann später im Laden eingesetzt oder verkauft werden.
- Beim ersten Öffnen des Spiels erscheint ein Tutorial mit den Angel-, Fang-, Eimer-, Shop-, Index- und Event-Grundlagen.
- Über die **?**-Schaltfläche im HUD kann das Tutorial jederzeit erneut geöffnet werden.

## Fisch-Index und Welt-Events

- Der Fisch-Index wurde neu aufgebaut: eigener Scrollbereich, Sammlungs-Fortschritt, Mutations-Tabs, Fischsuche und Seltenheitsfilter.
- In zufälligen Zeitabständen startet ein zeitlich begrenztes Welt-Event. Das aktive Event wird oben im Spiel mit Symbol und Countdown angezeigt.
- **Mutations-Regen:** Jeder während des Events gefangene Fisch erhält mindestens eine Gold-Mutation.
- **2× Glück:** Die Glückswirkung beim Fangen wird verdoppelt.
- **Goldrausch:** Das Einkommen aus dem Geld-Eimer und die Verkaufspreise sind verdoppelt.
- **Schnellbiss:** Fische beißen doppelt so schnell an.
- Die Events laufen zusätzlich zum normalen Wetter, Tag-Nacht-Wechsel, Schatzkisten und Piratenüberfällen.

## Charakterauswahl

- Beim ersten Start wählst du deinen Angler: **Lukas**, **Soa** oder **Kian**.
- Jede Figur hat eigene Farben, Frisur und Kleidung im Spiel.
- Die Auswahl wird im lokalen Spielstand gespeichert und bleibt bei späteren Besuchen erhalten.

## Schatzkiste und Hauptpreis

Die kostenlose Schatzkiste zeigt ihre Gewinnchancen an und rollt die Belohnung in einer horizontalen Leiste aus. Die sieben möglichen Belohnungen sind:

| Belohnung | Wahrscheinlichkeit |
|---|---:|
| Münzregen (+25% deines Geldes) | 24% |
| 25 Glücksköder | 20% |
| 10 zufällige Upgrade-Stufen | 22% |
| Seltener Fisch | 15% |
| Mutations-Fisch | 12% |
| Schatzkarte (+12.500 Münzen) | 5% |
| **Hauptpreis: Perlen-Dreizack** | **2%** |

Der Perlen-Dreizack bleibt dauerhaft im Spielstand, gibt einen kleinen Glücksbonus und lässt die Angel türkis leuchten. Ein weiterer Treffer auf den bereits gewonnenen Hauptpreis wird in 200.000 Münzen umgewandelt.

## Finale und Rebirth

- Das Finale startet, sobald der komplette Fisch-Index entdeckt wurde und mindestens **100.000 Münzen** im aktuellen Bestand liegen.
- In einer kurzen Abschluss-Szene erreicht Lukas das Festland, fährt nach Hause und umarmt seine Familie. Danach kann man normal weiterspielen oder rebirthen.
- Ein Rebirth setzt Sammlung, Fänge, Welten, Ausrüstung, Geld-Eimer und Münzbestand zurück. Der Rebirth-Zähler bleibt erhalten.
- Jeder Rebirth verdoppelt dauerhaft alle Münz-Einnahmen: beim ersten Rebirth **2×**, beim zweiten **4×**, danach **8×** usw. Der Bonus gilt für Verkäufe, Belohnungen und den Geld-Eimer.
- Beim Angeln gleiten Pose und Köder nach dem Auswurf weiter; Schnur und Köder bewegen sich unter Wasser mit der Strömung.


## Neue Inhalte

- Im Admin-Menü können der komplette Fisch-Index inklusive Gold-, Diamant- und Rainbow-Varianten sowie alle Welten freigeschaltet und der Perlen-Dreizack vergeben werden.
- Der neue **Sternen-Abgrund** kostet 75.000 Münzen, bietet **3× Glück**, eine eigene Kristall-Unterwasserwelt und 12 exklusive Fische über alle Seltenheitsstufen.
- Das Finale wurde auf neun Kapitel erweitert: Lukas erreicht die Küste, fährt nach Hause und erlebt eine längere Wiedersehensszene mit Umarmung und kurzen Gesprächen mit seiner Familie.


## Fischgrößen und Film-Finale

- Jeder Fang erhält eine zufällige Größe: **Small**, **Normal**, **Big** oder selten **Gigantic**. Das angezeigte Gewicht wird aus der Fischart und der Größenklasse berechnet.
- Die Größenklasse verändert den Verkaufswert und den passiven Geld-Eimer-Ertrag: Small ×0,65, Normal ×1, Big ×1,75 und Gigantic ×3,5.
- Alte gespeicherte Fänge ohne Größenangabe bleiben als Normal-Fische nutzbar.
- Das Finale läuft jetzt automatisch als Vollbild-Animationsfilm mit gezeichneten Figuren, Boot, Heimfahrt, Familien-Wiedersehen, Dialogen und Szenenübergängen. Die Szenen können weiterhin zurück- oder übersprungen werden.
- Bei besonders großen oder sehr seltenen Fängen kommentiert die Spielfigur gelegentlich den Fang – nicht bei jedem Fisch.


- Fische im Geld-Eimer können über **Umbenennen** einen eigenen Namen erhalten. Der Name wird gespeichert und bleibt auch beim Herausnehmen des Fisches erhalten.
