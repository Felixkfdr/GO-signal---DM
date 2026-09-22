# SV Gustlmännchen

Die Vereinsseite der Hobbyliga-Truppe: Trainingstermine eintragen, abstimmen, wer kann — und
den Strafkatalog vor Augen haben.

Eine einzelne HTML-Datei, kein Build, keine Abhängigkeiten.

## Benutzen

`index.html` im Browser öffnen — das war's.

1. **Anmelden** — einmal mit Namen (Rückennummer optional) eintragen. Wer angemeldet ist, steht im Kader
   und darf abstimmen.
2. **Kalender** — Tag anklicken, Uhrzeit und Ort eintragen, fertig. Wer einen Termin einträgt, steht
   automatisch auf „dabei". Ein Punkt im Kalender zeigt, dass an dem Tag etwas ansteht, die Zahl darin
   die Zusagen; wird der Punkt grün, findet das Training statt.
3. **Abstimmung** — zu jedem Termin *Bin dabei*, *Vielleicht* oder *Kann nicht*. Nochmal auf dieselbe
   Antwort klicken nimmt sie zurück. Kommen genug Zusagen zusammen, springt der Termin auf
   **Training findet statt**.
4. **Strafkatalog** — die übliche Liste, erweiterbar. Zeilen lassen sich über das × löschen.

Die Schwelle („Training findet statt ab _n_ Zusagen") steht oben in der Abstimmung und lässt sich
jederzeit ändern — Standard sind 8.

## Daten

Alles landet im `localStorage` des jeweiligen Browsers, unter dem Schlüssel `svg-hobbyliga-v1`.
Das heißt: **jeder sieht erst einmal nur seine eigenen Eintragungen.** Für eine echte gemeinsame
Abstimmung über mehrere Geräte hinweg bräuchte es einen kleinen Server (oder einen gehosteten
Datendienst), der Kader, Termine und Stimmen hält — die Seite ist so gebaut, dass dafür nur
`load()` und `save()` im `<script>`-Block ausgetauscht werden müssen.

Im privaten Modus mancher Browser ist `localStorage` gesperrt; dann funktioniert alles wie gewohnt,
die Daten sind aber nach dem Schließen des Tabs weg.

## Anpassen

Oben im `<script>`-Block:

| Konstante | Bedeutung |
| --- | --- |
| `DEFAULT_PENALTIES` | Strafkatalog, mit dem eine frische Seite startet |
| `STORE` | Schlüssel im `localStorage` |

Vereinsfarben stecken in den CSS-Variablen `--pitch` und `--pitch-2` ganz oben im `<style>`-Block;
ein Dark-Mode-Satz derselben Variablen steht direkt darunter.

## Sonst noch hier

`go.html` — ein Startsignal für den Browser. Beide ⌘-Tasten gleichzeitig drücken, ein Countdown von 3
läuft, dann erscheint **GO**. Auf Touch-Geräten mit zwei Fingern tippen.

## Lizenz

MIT
