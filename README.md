# Luki angeln

Ein kleines Angelspiel direkt im Browser.

## Starten

Öffne [index.html](./index.html) im Browser. Es ist keine Installation und kein Build-Schritt nötig.

## Seltenheiten

Die sechs Seltenheitsstufen sind jetzt:

1. Normal
2. Selten
3. Sehr selten
4. Unmöglich
5. Legendär
6. Mythisch

Legendär liegt zwischen Unmöglich und Mythisch. Unmögliche Fische sind seltener als zuvor; legendäre und mythische Fänge sind noch seltener.

## Fischsammlung

Es gibt jetzt **79 verschiedene Fische**, darunter **16 Neuzugänge**:
- 6 neue Fische im normalen See
- 5 neue Fische in der Aurora-Welt
- 5 neue Fische im Korallenriff

## Minispiel

Der Schwierigkeitsgrad steigt jetzt in sechs Stufen. Unmögliche, legendäre und mythische Fische brauchen mehr Treffer und haben kleinere Trefferzonen. Der Start-Lebenstand steigt ebenfalls mit der Seltenheit:

| Seltenheit | Treffer nötig | Start-Leben |
|---|---:|---:|
| Normal | 1 | 4 |
| Selten | 2 | 5 |
| Sehr selten | 3 | 6 |
| Unmöglich | 5 | 7 |
| Legendär | 6 | 8 |
| Mythisch | 7 | 9 |

Jede zweite Angel-Stufe gibt ein zusätzliches Leben. Mutierte Fische geben ebenfalls ein zusätzliches Leben, benötigen aber einen Treffer mehr.

## Weitere Funktionen

- Überarbeitetes, responsives Interface.
- Seltene Fänge haben aufwendigere Reveal-Animationen.
- Fangkarte zeigt die jeweilige Fangchance und den Verkaufspreis.
- Köderpreise steigen mit Käufen, Fangfortschritt und Ausrüstung.
- Gold-, Diamant- und Rainbow-Index haben sichtbare Sammelziele.
- Verkauf eines Fangs ist gegen Doppelklicks und falsche Inventar-Schlüssel abgesichert.

## Spielstand

Der Spielstand wird lokal im Browser über `localStorage` gespeichert. Er wird nicht automatisch zwischen verschiedenen Browsern oder Geräten synchronisiert.
