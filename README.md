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

Es gibt sechs Seltenheitsstufen: Normal, Selten, Sehr selten, Unmöglich, Legendär und Mythisch. Die Sammlung enthält 79 verschiedene Fische über den normalen See, die Aurora-Welt und das Korallenriff.

Jede Seltenheit startet im Angel-Minispiel mit genau **3 Leben**.

Bei jedem erfolgreichen Fang gibt es eine feste **1%-Chance** auf eine Schatzkiste. Glücks-Upgrades verändern diese Chance nicht. Eine Kiste enthält zufällig 25% des aktuellen Geldbestands (mindestens 50 Münzen), 25 Glücksköder oder 10 zufällige Upgrade-Stufen, soweit noch verfügbar.

Ein Piratenschiff taucht in zufälligen Abständen zwischen **10 Sekunden und 5 Minuten** auf. Im Kampf müssen 7 schrumpfende Zielscheiben in 30 Sekunden getroffen werden; höchstens 3 Fehlschüsse sind erlaubt. Ein Sieg zahlt 7% aller bisher verdienten Münzen aus. Bei einer Niederlage geht der aktuelle Münzbestand verloren.

Die Fangkarte zeigt Seltenheitschance, Mutationschance und die kombinierte Fangchance inklusive Mutation an.

## Spielstand

Der Spielstand wird lokal im Browser über `localStorage` gespeichert und nicht automatisch zwischen Geräten synchronisiert.

## Admin-Menü, Tageszeit und Wetter

- Sieben schnelle Klicks auf die Münzanzeige öffnen das geheime Admin-Menü.
- Im Admin-Menü lassen sich der Münzbestand und der Glückswert einstellen. Der Glückswert beeinflusst seltene Fische und Mutationen ab dem nächsten Wurf.
- Eine Schatztruhe kann für den nächsten erfolgreichen Fang vorgemerkt werden.
- Ein Piratenüberfall kann direkt gestartet werden.
- Im Spiel wechseln Tag und Nacht automatisch in einem Zyklus von ungefähr drei Minuten.
- Gelegentlich setzt Regen ein. Währenddessen werden die Wellen höher und das Boot schaukelt stärker.
