# Kanji Karten für alle Jouyou-Kanji zum Lernen mit Anki

## Alle Kanji (kanji_neu_cleaned_2136_joyou.txt)

Format: `Japanische Schulklasse|Kanji|kun-yomi|on-yomi|dt. Bedeutung`

mit

* `Japanische Schulklasse`: Klasse 1 bis 10. Die Reihenfolge der Kanji in der weiterführenden Schule (ab Klasse 6) ist nicht eindeutig festgelegt. Die Einteilung hier orientiert sich u.a. am Kanji Kentei.
* `kun-yomi`: getrennt durch `,`, Start von Okurigana mit `。`
* `on-yomi`: wie kun-yomi
* `dt. Bedeutung`: getrennt durch `,`

## Lernkarten für Anki

Kurze Sätze zum Lernen in beide Richtungen (Lesung -> Kanji und Kanji -> Lesung)

* Front und Back getrennt durch `TAB`
* Das zu lernende Kanji steht zwischen `「` und `」`

Für sämtliche anderen in dem Beispiel vorkommenden Kanji (auch solche die in der Klasse schon gelernt sein sollten) stehen Furigana.

Format: `SPACE Kanji [ Furigana ]`. Vor dem Kanji muss ein SPACE stehen, damit Anki den Anfang der zu setzenden Furigana erkennt.

## Import in Anki

a) Direktimport des Decks (tbd)
b) Neues Deck anlegen und "File -> Import"

Vorher: Neuen Kartentyp mit Furigana und Front->Back + Back->Front anlegen.

* Browse Cards, Recktsklick auf Notes, Manage Note Types
* Button Fields: Front + Back: Font auf MS Mincho setzen (sonst werden evtl. chin. Zeichen angezeigt statt jap.)
* Button Cards: Zwei Typen anlegen (wenn nicht schon existiert):
  * Type 1: Card 1: Front -> Back
  * Type 2: Card 2: Back -> Front

### Type 1 Template:

#### Front Template
```
{{furigana:Front}}
```
### Back Template
```
{{FrontSide}}

<hr id=answer>

{{furigana:Back}}
```

### Styling

Damit keine chin. Zeichen angezeigt werden:

```
.card {
 font-family:"ヒラギノ角ゴ Pro W3", "Hiragino Kaku Gothic Pro",Osaka, "メイリオ", Meiryo, "ＭＳ Ｐゴシック", "MS PGothic", sans-serif;
 text-align: center;
 color: black;
 background-color: white;
}
```

### Type 2 Template:

#### Front Template
```
{{furigana:Back}}
```
### Back Template
```
{{FrontSide}}

<hr id=answer>

{{furigana:Front}}
```

### Styling

Damit keine chin. Zeichen angezeigt werden:

```
.card {
 font-family:"ヒラギノ角ゴ Pro W3", "Hiragino Kaku Gothic Pro",Osaka, "メイリオ", Meiryo, "ＭＳ Ｐゴシック", "MS PGothic", sans-serif;
 text-align: center;
 color: black;
 background-color: white;
}
```

