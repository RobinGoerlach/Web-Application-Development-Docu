## # HTML-Tabellen: Erstellen von Tabellen mit `<table>`, `<tr>`, `<td>` und `<th>`

Tabellen sind ein nützliches Werkzeug in HTML, um Daten und Informationen strukturiert darzustellen. Sie eignen sich besonders für die Darstellung tabellarischer Informationen wie Kalender, Preislisten, Stundenpläne oder Vergleichstabellen. HTML bietet dafür die Tags `<table>`, `<tr>`, `<td>`, und `<th>`, mit denen die Struktur einer Tabelle definiert wird.
## Grundstruktur einer HTML-Tabelle

Eine HTML-Tabelle wird mit dem `<table>`-Tag erstellt. Eine Tabelle besteht aus Zeilen (`<tr>` für table row) und Zellen (`<td>` für table data), die die Inhalte der Tabelle aufnehmen. Kopfzellen werden mit dem `<th>`-Tag (table header) erstellt und dienen oft als Spalten- oder Zeilenüberschriften.
### Beispiel einer einfachen Tabelle
```html
<table>
<tr>
  <th>Name</th>
  <th>Alter</th>
  <th>Beruf</th>
</tr>
<tr>
  <td>Max</td>
  <td>25</td>
  <td>Entwickler</td>
</tr>
<tr>
  <td>Lisa</td>
  <td>30</td>
  <td>Designer</td>
</tr>
</table>
```
**Ergebnis:**

| Name | Alter | Beruf      |
| ---- | ----- | ---------- |
| Max  | 25    | Entwickler |
| Lisa | 30    | Designer   |
### Erklärung der Tags
- **`<table>`**: Umfasst die gesamte Tabelle.
- **`<tr>`**: Definiert eine Tabellenzeile (table row). Jede Zeile enthält mehrere Zellen.
- **`<th>`**: Erstellt eine Kopfzelle (table header). Der Text in Kopfzellen ist standardmäßig fett und zentriert.
- **`<td>`**: Erstellt eine normale Zelle (table data) innerhalb einer Zeile.
## Aufbau einer Tabelle mit Kopf- und Datenzeilen
Es ist gängige Praxis, die erste Zeile einer Tabelle als Kopfzeile zu verwenden und die weiteren Zeilen als Datenzeilen.
```html
<table>
  <tr>
    <th>Produkt</th>
    <th>Preis</th>
    <th>Menge</th>
  </tr>
  <tr>
    <td>Apfel</td>
    <td>1,20 €</td>
    <td>5</td>
  </tr>
  <tr>
    <td>Banane</td>
    <td>0,80 €</td>
    <td>8</td>
  </tr>
</table>
```
**Ergebnis:**

| Produkt | Preis  | Menge |
| ------- | ------ | ----- |
| Apfel   | 1,20 € | 5     |
| Banane  | 0,80 € | 8     |
## Erweiterte Tabellenstruktur mit `<thead>`, `<tbody>` und `<tfoot>`
Für komplexere Tabellen bietet HTML die Tags `<thead>`, `<tbody>` und `<tfoot>` an, um die Struktur der Tabelle zu verbessern:
- **`<thead>`**: Umfasst die Kopfzeilen der Tabelle.
- **`<tbody>`**: Umfasst den Hauptinhalt der Tabelle.
- **`<tfoot>`**: Umfasst die Fußzeile der Tabelle (z.B. Summen, Gesamtangaben).
### Beispiel mit `<thead>`, `<tbody>` und `<tfoot>`
```html
<table>
  <thead>
    <tr>
      <th>Artikel</th>
      <th>Stückpreis</th>
      <th>Anzahl</th>
      <th>Gesamt</th>
    </tr>
  </thead>
  <tbody>
    <tr>
       <td>Apfel</td>
       <td>1,20 €</td>
       <td>5</td>
       <td>6,00 €</td>
    </tr>
    <tr>
       <td>Banane</td>
       <td>0,80 €</td>
       <td>8</td>
       <td>6,40 €</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
       <td colspan="3">Gesamt</td>
       <td>12,40 €</td>
    </tr>
  </tfoot>
</table>
```
**Ergebnis:**

| Artikel    | Stückpreis | Anzahl | Gesamt  |
| ---------- | ---------- | ------ | ------- |
| Apfel      | 1,20 €     | 5      | 6,00 €  |
| Banane     | 0,80 €     | 8      | 6,40 €  |
| **Gesamt** |            |        | 12,40 € |
### Erklärung der zusätzlichen Tags
- **`<thead>`**: Enthält die Kopfzeile der Tabelle, üblicherweise die Titel für jede Spalte.
- **`<tbody>`**: Enthält die Datenzeilen der Tabelle.
- **`<tfoot>`**: Wird oft für die Zusammenfassung oder den Gesamtbetrag verwendet und befindet sich am unteren Rand der Tabelle.
- **`colspan`**: Ein Attribut, das die Anzahl der zu überbrückenden Spalten angibt. Im Beispiel erstreckt sich die Zelle in der Fußzeile über drei Spalten.
## Tabellenstyling mit CSS
Tabellen lassen sich mit CSS ansprechend gestalten, um die Lesbarkeit und das Layout zu verbessern. Hier sind einige grundlegende CSS-Eigenschaften, die für Tabellen hilfreich sind:
```css
table {
  width: 100%;
  border-collapse: collapse; /* Entfernt die Abstände zwischen Zellen */
}
th, td {
  border: 1px solid #ddd;
  padding: 8px;
  text-align: left;
}
th {
  background-color: #f4f4f4;
  font-weight: bold;
}
tr:nth-child(even) {
  background-color: #f9f9f9; /* Streifenmuster für die Lesbarkeit */
}
```
### Erklärung des CSS
- **`border-collapse: collapse;`**: Entfernt die Abstände zwischen den Zellen und sorgt für ein kompaktes Design.
- **`border`**: Definiert einen Rand um jede Zelle.
- **`padding`**: Fügt Innenabstand in jeder Zelle hinzu.
- **`text-align: left;`**: Richtet den Inhalt der Zellen linksbündig aus.
- **`nth-child(even)`**: Hebt jede zweite Zeile hervor und schafft ein Streifenmuster, das die Lesbarkeit verbessert.
### Beispiel für eine gestylte Tabelle
```html
<table>
  <thead>
    <tr>
       <th>Artikel</th>
       <th>Preis</th>
       <th>Menge</th>
    </tr>
  </thead>
  <tbody>
    <tr>
       <td>Apfel</td>
       <td>1,20 €</td>
       <td>5</td>
    </tr>
    <tr>
      <td>Banane</td>
      <td>0,80 €</td>
      <td>8</td>
    </tr>
  </tbody>
</table>
```
Mit den oben genannten CSS-Regeln ist diese Tabelle gut lesbar und optisch ansprechend.
## Zusammenfassung: Wann du Tabellen verwenden solltest
Tabellen sind ideal für die Darstellung tabellarischer Daten und Informationen. Sie sind jedoch ungeeignet für das allgemeine Layout von Inhalten, da Tabellen nur für strukturierte, miteinander in Beziehung stehende Daten konzipiert sind.
**Verwende Tabellen, wenn:**
- Du numerische oder strukturierte Daten anzeigst, die eine logische Beziehung haben (z.B. Preise, Berichte).
- Die Daten durch Überschriften in Spalten oder Zeilen logisch gruppiert werden können.
**Vermeide Tabellen für das Layout von Webseiten**: CSS ist für das Layout und die Positionierung von Inhalten viel besser geeignet und flexibler.

---

Dieser Artikel bietet eine fundierte Einführung in die Erstellung und Gestaltung von Tabellen in HTML. Mit diesen Grundlagen kannst du tabellarische Daten klar und strukturiert darstellen und deine Tabellen ansprechend gestalten.