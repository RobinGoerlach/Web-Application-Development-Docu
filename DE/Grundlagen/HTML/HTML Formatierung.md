HTML bietet eine Vielzahl von Tags, die zur Strukturierung und Formatierung von Text verwendet werden können. Diese Tags ermöglichen es, Inhalte auf einer Webseite hierarchisch zu ordnen und bestimmte Teile des Textes hervorzuheben. Die richtigen Tags zu verwenden, verbessert die Lesbarkeit und Struktur deiner Inhalte und ist wichtig für die Barrierefreiheit und Suchmaschinenoptimierung.
## Strukturierende und Formatierende HTML-Tags

### 1. **Absätze (`<p>`)**
Das `<p>`-Tag wird verwendet, um Absätze in HTML zu definieren. Es handelt sich dabei um ein Block-Element, das standardmäßig eine Leerzeile vor und nach dem Absatz einfügt, um den Text visuell zu trennen.
```html
<p>Dies ist ein Absatz mit einem Beispieltext.</p>
<p>Hier ist ein weiterer Absatz, der Inhalte voneinander trennt.</p>
```
### 2. **Überschriften (`<h1>` bis `<h6>`)**
Überschriften geben dem Dokument eine logische Struktur und machen die Hierarchie des Inhalts klar. HTML bietet sechs Überschriftsebenen, wobei `<h1>` die wichtigste und `<h6>` die unwichtigste Überschrift darstellt.
```html
<h1>Hauptüberschrift</h1>
<h2>Unterüberschrift</h2>
<h3>Abschnittsüberschrift</h3>
<h4>Weitere Untergliederung</h4>
<h5>Kleinere Untergliederung</h5>
<h6>Kleinste Überschrift</h6>
```
### Best Practices für Überschriften:
- Verwende nur ein `<h1>` pro Seite, da es die Hauptüberschrift darstellt.
- Nutze die Hierarchie sinnvoll, um Inhalte logisch zu strukturieren.
- Überschriften helfen auch Suchmaschinen, den Seiteninhalt besser zu verstehen, was die SEO verbessert.
### 3. **Fett und Kursiv: Hervorhebung mit `<strong>` und `<em>`**
HTML bietet zwei Tags, um Text hervorzuheben:
- **`<strong>`**: Zeigt den Text in Fettschrift an und hebt ihn semantisch hervor, um die Wichtigkeit zu betonen.
- **`<em>`**: Stellt den Text kursiv dar und betont ihn ebenfalls, allerdings weniger stark als `strong`.
Beide Tags haben nicht nur eine optische Funktion, sondern vermitteln auch Bedeutung für Suchmaschinen und Screenreader.
```html
<p>Dies ist ein <strong>wichtiger</strong> Text.</p>
<p>Hier wird etwas <em>betont</em>.</p>
```
### 4. **Zeilenumbruch (`<br>`)**
Das `<br>`-Tag erzeugt einen einfachen Zeilenumbruch innerhalb eines Textblocks. Es ist ein sogenanntes leeres Tag, das keinen Schließtag benötigt.
```html
<p>Dies ist der erste Satz.<br>Und das ist der nächste Satz in einer neuen Zeile.</p>
```
Verwende `<br>` sparsam, wenn ein logischer Absatzwechsel gewünscht ist, nutze stattdessen das `<p>`-Tag.
### 5. **Horizontale Linie (`<hr>`)**
Das `<hr>`-Tag fügt eine horizontale Linie ein, die als Trennlinie zwischen Abschnitten verwendet wird. Es ist ebenfalls ein leeres Tag und erfordert keinen Schließtag. Die Linie kann als visuelle Abgrenzung zwischen thematischen Abschnitten dienen.
```html
<p>Abschnitt eins des Inhalts</p> <hr> <p>Abschnitt zwei des Inhalts</p>
```
### 6. **Inline-Textformatierung**
Zusätzlich zu `<strong>` und `<em>` gibt es weitere HTML-Tags, die spezifische Inline-Formatierungen bieten.
- **`<b>` und `<i>`**: `<b>` zeigt Text fett, und `<i>` kursiv an, jedoch ohne die semantische Betonung wie `strong` und `em`. Diese Tags sollten vor allem für dekorative Zwecke genutzt werden, wenn keine besondere Bedeutung vermittelt wird.
```html
<p>Ein <b>fetter</b> Text ohne starke Bedeutung.</p>
<p>Ein <i>kursiver</i> Text ohne besondere Betonung.</p>
```
- **`<mark>`**: Hebt Text hervor, meist durch eine Hintergrundfarbe. Es zeigt an, dass der markierte Text besonders wichtig ist.
```html
<p>Dies ist ein <mark>hervorgehobener</mark> Text.</p>
```
- **`<small>`**: Zeigt Text in kleinerer Schriftgröße an, oft für rechtliche Hinweise oder erklärende Texte verwendet.
```html
<p>Copyright <small>2024 Meine Webseite</small></p>
```
### 7. **Zusätzliche Tags für die Textstruktur**
Diese Tags bieten weitere Möglichkeiten zur Textstrukturierung:
- **`<blockquote>`**: Wird verwendet, um längere Zitate hervorzuheben. Es wird häufig eingerückt dargestellt.
```html
<blockquote>
„Das Leben ist das, was passiert, während du andere Pläne machst.“ - John Lennon 
</blockquote>
```
- **`<q>`**: Wird für kurze Zitate innerhalb eines Textabsatzes genutzt. Meist wird es in Anführungszeichen angezeigt.
```html
<p>Er sagte: <q>Wir sehen uns später.</q></p>
```  
- **`<code>`**: Hebt Code oder kurzen Programmiertext hervor und stellt ihn oft in einer Monospace-Schriftart dar.
```html
<p>Verwende das Kommando <code>git init</code>, um ein neues Repository zu erstellen.</p>
```
- **`<pre>`**: Zeigt vorformatierten Text an, der mit Leerzeichen und Zeilenumbrüchen genau so dargestellt wird, wie er eingegeben wurde. Nützlich für Codeblöcke oder tabellarische Daten.
```html
<pre> Zeile 1 Zeile 2 </pre>
```
## Beispiele zur praktischen Verwendung

Hier ist ein Beispiel, das die wichtigsten Tags für Text- und Inhaltsformatierung kombiniert:
```html
<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <title>Text- und Inhaltsformatierung</title>
</head>
<body>
  <h1>Willkommen auf meiner Webseite</h1>
  <p>Dies ist ein Beispieltext, der zeigt, wie man verschiedene HTML-Elemente 
     zur Strukturierung und Formatierung von Inhalten verwendet.</p>
  <h2>Wichtige Anweisungen</h2>
  <p>Hier findest du <strong>wichtige</strong> und <em>betonte</em> 
     Informationen.</p>
  <p>Weitere Details:</p>
  <ul>
    <li><b>Fett</b>zeigt Hervorhebung ohne semantische Bedeutung.</li>
    <li><i>Kursiv</i> zeigt ebenfalls dekorative Hervorhebung.</li>
  </ul>
  <h2>Zitat und Code-Beispiele</h2>
  <blockquote>
   „Wissen ist Macht.“ - Francis Bacon
  </blockquote>
  <p>Beispiel für Code:
     <code>console.log('Hallo Welt');</code>
  </p>
  <h2>Abschnitte trennen</h2>
    <p>Inhalte können auch durch horizontale Linien voneinander abgegrenzt 
      werden:
    </p>
    <hr>
    <p>Dies ist ein neuer Abschnitt.</p>
</body>
</html>
```
## Best Practices für Text- und Inhaltsformatierung
1. **Semantische Tags verwenden**: Nutze Tags wie `<strong>` und `<em>` für bedeutungsvolle Hervorhebungen, um die Lesbarkeit und Barrierefreiheit zu verbessern.
2. **Logische Struktur schaffen**: Nutze Überschriften und Absätze, um den Text lesefreundlich und strukturiert darzustellen.
3. **Vermeide übermäßige Inline-Formatierung**: Verwende CSS für Styling und Layout, um den HTML-Code sauber und wartbar zu halten.

---

Dieser Artikel bietet einen Überblick über die wichtigsten HTML-Tags zur Text- und Inhaltsformatierung. Mit diesen Grundlagen kannst du Inhalte strukturiert darstellen und gezielt formatieren, um die Lesbarkeit und Bedeutung des Textes zu verbessern.