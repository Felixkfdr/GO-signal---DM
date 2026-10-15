# GO

Ein Startsignal für den Browser. Beide ⌘-Tasten gleichzeitig drücken, ein Countdown von 3 läuft, dann erscheint **GO**. Nach zwei Sekunden steht wieder `Press to start` da.

Eine einzelne HTML-Datei, kein Build, keine Abhängigkeiten.

## Benutzen

`index.html` im Browser öffnen — das war's.

- **Tastatur:** beide ⌘-Tasten gleichzeitig antippen (halten ist nicht nötig). Beide Shift-, Ctrl- oder Alt-Tasten gehen genauso, falls der Browser ⌘ abfängt.
- **Touch:** mit zwei Fingern tippen.

„Gleichzeitig" heißt: die zweite Taste innerhalb von 300 ms nach der ersten. Eine einzelne Taste löst nichts aus.

## Anpassen

Oben im `<script>`-Block:

| Konstante | Standard | Bedeutung |
| --- | --- | --- |
| `COUNT_FROM` | `3` | Startzahl des Countdowns |
| `GO_MS` | `2000` | wie lange `GO` stehen bleibt (ms) |
| `TAP_WINDOW` | `300` | max. Abstand zwischen den beiden Tasten (ms) |

Die drei Lampen oben richten sich automatisch nach `COUNT_FROM` — bei einem anderen Wert die `<span class="lamp">`-Elemente entsprechend anpassen.

## Lizenz

MIT
