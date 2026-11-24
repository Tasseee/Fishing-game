# Luki angeln

Ein kleines Angelspiel direkt im Browser.

## Starten

Öffne [index.html](./index.html) im Browser. Es ist keine Installation und kein Build-Schritt nötig.

## Seltenheiten und Fische

Es gibt sechs Seltenheitsstufen: Normal, Selten, Sehr selten, Unmöglich, Legendär und Mythisch. Legendär liegt zwischen Unmöglich und Mythisch. Die Sammlung enthält 79 verschiedene Fische über den normalen See, die Aurora-Welt und das Korallenriff.

## Minispiel beim Angeln

Jede Seltenheit startet mit genau **3 Leben**. Die benötigten Treffer und die Größe beziehungsweise Geschwindigkeit der Zielzone steigen weiter mit der Seltenheit.

## Mutations-Wahrscheinlichkeiten

Die Fangkarte zeigt die Seltenheitschance, die Wahrscheinlichkeit der tatsächlich gezogenen Mutation (oder „keine Mutation“) und die kombinierte Gesamtchance aus beidem.

## Schatzkiste

Bei jedem erfolgreichen Fang wird eine feste **1%-Chance** auf eine Schatzkiste geprüft. Glücks-Upgrades verändern diese Chance nicht. Beim Öffnen gibt es zufällig entweder:
- Münzen in Höhe von 25% des aktuellen Geldbestands (mindestens 50 Münzen),
- 25 Glücksköder,
- oder 10 zufällige Upgrade-Stufen, soweit noch Stufen verfügbar sind.

Die Kiste hat eine eigene Öffnungsanimation.

## Piratenschiff

Ein Piratenschiff taucht in zufälligen Abständen zwischen **10 Sekunden und 5 Minuten** auf. Im Kampf müssen 7 kleiner werdende Zielscheiben angeklickt werden. Es gibt 30 Sekunden Zeit und höchstens 3 verfehlte Ziele.

- Sieg: Beute in Höhe von **7% aller seit Beginn gezählten verdienten Münzen**.
- Niederlage: Der aktuelle Münzbestand geht verloren.

Das Spiel speichert die gesamten verdienten Münzen separat, damit Ausgaben und zwischenzeitliche Verluste den späteren Piratenbonus nicht verringern. Bei älteren Spielständen wird der aktuelle Münzbestand als bisheriger Mindestwert übernommen.

## Weitere Funktionen

- Responsives Interface und animierte Fangkarten.
- Gold-, Diamant- und Rainbow-Mutationen.
- Köderpreise steigen mit Käufen, Fangfortschritt und Ausrüstung.
- Der Spielstand wird lokal im Browser über `localStorage` gespeichert und nicht automatisch zwischen Geräten synchronisiert.
