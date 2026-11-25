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

Es gibt sechs Seltenheitsstufen: Normal, Selten, Sehr selten, Unmöglich, Legendär und Mythisch. Die Sammlung enthält jetzt **115 verschiedene Fische** über den normalen See, die Aurora-Welt, das Korallenriff und den Sternen-Abgrund. In jeder dieser Welten gibt es neue Arten über mehrere Seltenheitsstufen.

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
- Jede der sechs Seltenheitsstufen hat jetzt eine eigene Fang-Animation: Normal zeigt Wasserwellen und aufsteigende Blasen, Selten blaue Kometen, Sehr selten violette Runen-Sechsecke, Unmöglich einen orangefarbenen Energiewirbel, Legendär einen goldenen Sonnenaufgang mit Krone und Mythisch eine mehrfarbige Galaxie. Auch Partikel, Schockwellen und Klanghöhe unterscheiden sich je nach Stufe.
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
- Fische im Geld-Eimer sammeln automatisch **1 XP pro Sekunde** und steigen bis **Level 10** auf. Das erste Level braucht 60 XP; jede weitere Stufe benötigt 60 XP mehr als die vorherige. Jedes Level erhöht das Einkommen des Fisches um **12%**. Level, Erfahrung und Fortschrittbalken werden gespeichert; beim Herausnehmen beginnt der Fisch beim nächsten Einsetzen wieder auf Level 1.
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

## Spielmodi und Storymodus

- Beim Spielstart kannst du zwischen **Normalmodus** und **Storymodus** wählen. Die Auswahl erscheint bei jedem Start erneut; der aktuelle Modus ist markiert und kann direkt fortgesetzt werden.
- Der **Normalmodus** ist das klassische Angelspiel ohne die ernsten persönlichen Storyverläufe. Er enthält ein eigenes, neutrales Angel-Tutorial.
- Der **Storymodus** erzählt die persönlichen Geschichten der ausgewählten Figur. Themen sind unter anderem Einsamkeit, depressive Gefühle und der Umgang mit Belastungen. Vor dem Einstieg erscheint ein Hinweis auf sensible Themen.
- Über **🎭** im HUD kannst du den Modus jederzeit wechseln. Über **👤** kannst du in beiden Modi jederzeit zwischen Lukas, Soa und Kian wechseln.
- Im Storymodus verändern sich Mimik und Haltung der Figur fließend mit dem Verlauf. Kian behält seinen unbeschwerten Anfang und wirkt erst nach den ersten Beobachtungen nach und nach ernster. Im Normalmodus bleiben die Figuren neutral und fröhlich.
- Beim Wechsel des Spielmodus wird das passende Tutorial erneut angeboten; der bereits ausgewählte Charakter bleibt erhalten.
- Nach Kians Ausbruchsversuch beginnt er im Storymodus gelegentlich, die Spieloberfläche zu hacken: Münzanzeige und Fisch-Index flackern oder zeigen kurz Fantasiewerte, die Angelsteuerung kann für wenige Sekunden blockiert sein. Das sind reine Effekte – Münzen, Fänge und Spielstand bleiben unverändert.
- Bei Soa gibt es im Storymodus keine zusätzliche Essens-Nachricht: Die Fangkarte verschwindet und Soa isst genau den gerade gefangenen Fisch direkt auf dem Boot. Fischart, Mutation und Größenklasse werden in der Animation übernommen. Erst danach wird der Fang verkauft und der Fangwert gutgeschrieben. Im Normalmodus läuft der Verkauf direkt wie im klassischen Spiel ab.
- Die normalen Sprüche der Figuren erscheinen jetzt häufiger; Sprechpausen und Zufallsfilter wurden reduziert. Soas Ess-Animation bleibt davon unabhängig und zeigt keine zusätzliche Sprechblase.

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

- Die Level-Fortschrittsbalken im Geld-Eimer werden während des geöffneten Shops etwa zehnmal pro Sekunde aktualisiert. Das neun Kapitel lange Finale wurde um animierte Lichtstrahlen, schwebende Lichtpartikel, Burst-Effekte und einen leuchtenden Herz-Moment erweitert.

- **Kian-Meta-Story:** Wenn Kian ausgewählt ist, bemerkt er über mehrere Spielphasen hinweg, dass die Welt ein Spiel ist. Er erkennt den Spieler, stellt über anklickbare Sprechblasen Fragen und versucht schließlich mit einem Bildschirm-Glitch auszubrechen. Fortschritt und Gesprächsstufe bleiben gespeichert.
- **Soas Verkaufsanimation:** Wenn Soa als Angler ausgewählt ist, löst jeder Fischverkauf zuerst eine kurze Cartoon-Sequenz aus: Soa schnappt sich den Fang, mampft zufrieden und wirft ihn mit einem PLATSCH zurück ins Meer. Danach wird der Verkauf wie gewohnt verbucht.


## Drei getrennte Storypfade

- Zu Beginn wählst du **eine** Hauptfigur: Lukas, Soa oder Kian. Nur diese Figur ist während der Reise auf dem Boot zu sehen und wird gespielt. Luki ist nicht an Bord. Über das neue 👤-Symbol im HUD kannst du später den Storypfad wechseln; der neue Pfad startet dann von vorn.
- Je nach Auswahl läuft eine eigene sechsstufige Story mit eigenen Sprechblasen, Stimmungen und einem eigenen neunkapiteligen Finale. Der aktive Storyfortschritt wird gespeichert; bei einem Figurenwechsel beginnt der neue Pfad von vorn.

### Lukas · Hinter dem Lächeln
- Lukas wirkt fröhlich, wenn du ihn beobachtest. Wenn du eine Weile nicht hinsiehst, sinken seine Schultern und sein Gesicht wird traurig.
- Seine Geschichte dreht sich darum, dass er nicht dauernd stark oder gut gelaunt wirken muss. Im Finale kommt er zu seiner Familie zurück und kann ehrlich sagen, wie es ihm geht.

### Soa · Was das Essen verbirgt
- Soa nutzt anfangs Snacks als Ablenkung, wenn er nervös oder traurig ist. Seine Fisch-Verkaufsanimation ist nur in diesem Storypfad aktiv.
- Die Animation und die Dialoge werden nach und nach ernster: Soa erkennt, dass Essen seine Sorgen nicht löst, und lernt, über seine Gefühle zu sprechen. Das Finale führt ihn zu seiner Familie zurück.

### Kian · Gefangen im Spiel
- Kian bemerkt zunehmend, dass sich Wellen, Wolken und Ereignisse wiederholen. Er erkennt, dass er in einem Spiel gefangen sein könnte und dass du der Spieler außerhalb seiner Welt bist.
- Über anklickbare Sprechblasen kannst du ihm antworten. Er versucht mit einem Bildschirm-Glitch auszubrechen und findet am Ende einen hoffnungsvollen Weg nach Hause.

- Die drei Pfade enden jeweils mit einer Heimkehr zur eigenen Familie. Die Figuren müssen nicht plötzlich alle Sorgen los sein; sie finden einen sicheren Ort, an dem sie ehrlich darüber reden können.
