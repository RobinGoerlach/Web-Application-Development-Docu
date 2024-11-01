HTML-Elemente sind die Bausteine, aus denen Webseiten aufgebaut werden. Sie definieren den Inhalt und die Struktur einer Seite, wie Überschriften, Absätze, Links, Bilder und vieles mehr. Ein HTML-Element besteht in der Regel aus einem **öffnenden Tag**, einem **Inhalt** und einem **schließenden Tag**.
## Aufbau eines HTML-Elements

Ein einfaches HTML-Element sieht wie folgt aus:
```html
<tagname>Inhalt des Elements</tagname>
```
- **Tagname**: Der Name des HTML-Tags, das den Inhalt umschließt (z. B. `p`, `h1`, `div`).
- **Inhalt**: Der tatsächliche Inhalt des Elements (z. B. Text oder eingebettete Medien).
- **Schließtag**: Der Tag, der das Ende des Elements markiert, meist `</tagname>`.
Einige HTML-Elemente wie `<img>` oder `<br>` haben jedoch keinen Inhalt und keinen Schließtag – diese nennt man **leere Tags**.
## Typen von HTML-Elementen
HTML-Elemente lassen sich nach ihrer Funktion und Bedeutung in verschiedene Typen einteilen. Hier sind einige der wichtigsten Typen:

### 1. **Strukturierende Elemente**
Diese Elemente geben dem Dokument eine klare Struktur und Hierarchie.
- **Überschriften (`<h1>` bis `<h6>`)**: Die verschiedenen Überschriftsebenen strukturieren Inhalte hierarchisch, wobei `<h1>` die höchste und `<h6>` die niedrigste Ebene darstellt.
```html
<h1>Hauptüberschrift</h1>
<h2>Unterüberschrift</h2>
```
- **Absatz (`<p>`)**: Definiert einen Textabsatz.
```html
<p>Dies ist ein Absatz.</p>
```
- **Container (`<div>` und `<span>`)**:   
    - `<div>` ist ein Block-Container und wird verwendet, um größere Bereiche zu gruppieren, die blockartig erscheinen.
    - `<span>` ist ein Inline-Container, der zur Gruppierung von Inhalten innerhalb eines Textblocks dient.
```html
<div>
  <p>In diesem Bereich befinden sich mehrere Absätze.</p>
</div>
<p>Ein Text mit <span>hervorgehobenem Abschnitt</span>.</p>
```

### 2. **Textformatierungs-Elemente**
Diese Elemente bieten Möglichkeiten zur Formatierung von Text.
- **Fett und kursiv (`<strong>`, `<em>`)**: `<strong>` hebt Inhalte durch Fettschrift hervor und `<em>` durch Kursivschrift. Beide sind semantische Tags, die zusätzlich betonen, wie wichtig oder hervorzuheben der Text ist.
```html
<p>Dies ist ein <strong>wichtiger</strong> Hinweis.</p> 
<p>Ein <em>hervorgehobener</em> Textabschnitt.</p>
```
- **Zeilenumbruch (`<br>`)**: Fügt einen Zeilenumbruch ein.
```html
<p>Dies ist der erste Satz.<br>Und dies ist der nächste Satz in einer neuen Zeile.</p>
```
- **Horizontaler Strich (`<hr>`)**: Fügt eine horizontale Linie als Trennung zwischen Abschnitten ein.
```html
<p>Textabschnitt</p> <hr> <p>Neuer Abschnitt</p>
```
### 3. **Medien-Elemente**
Medienelemente ermöglichen das Einfügen von Bildern, Videos und Audios.
- **Bilder (`<img>`)**: Bindet ein Bild ein. Es hat kein Schließtag und benötigt die Attribute `src` (Bildquelle) und `alt` (Beschreibung für Screenreader und SEO).
```html
<img src="bild.jpg" alt="Ein beschreibendes Bild">
```
- **Audio und Video (`<audio>`, `<video>`)**: Ermöglichen das Einbinden von Audio- und Videodateien.
```html
<audio controls>
  <source src="audio.mp3" type="audio/mpeg">
</audio>
<video width="320" height="240" controls>
  <source src="video.mp4" type="video/mp4">
</video>
```
### 4. **Verlinkungs-Elemente**
Verlinkungs-Elemente machen den Inhalt interaktiv, indem sie Verweise zu anderen Seiten oder internen Bereichen der Seite hinzufügen.
- **Link (`<a>`)**: Erstellt einen Hyperlink. Das `href`-Attribut gibt die URL des Links an.
```html
<a href="https://example.com" target="_blank">Besuche Beispielseite</a>
```
### 5. **Listen-Elemente**
Listen helfen, Inhalte in übersichtliche Listen zu gliedern.
- **Ungeordnete Liste (`<ul>`)**: Erstellt eine Liste ohne numerische Reihenfolge, oft mit Aufzählungspunkten.
- **Geordnete Liste (`<ol>`)**: Erstellt eine numerierte Liste.
- **Listenelement (`<li>`)**: Ein Eintrag innerhalb einer Liste.
```html
<ul>
  <li>Ein Element</li>
  <li>Ein weiteres Element</li>
</ul>
<ol>
  <li>Erstes Element</li>
  <li>Zweites Element</li>
</ol>
```
### 6. **Formularelemente**
Formulare ermöglichen Benutzereingaben und Interaktionen.
- **Formular (`<form>`)**: Der Container für die Eingabefelder eines Formulars.
- **Eingabefelder (`<input>`, `<textarea>`, `<button>`)**: Ermöglichen Benutzereingaben, wie Textfelder, Schaltflächen, Dropdowns usw.
```html
<form action="/submit-form" method="post">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name">
  <button type="submit">Absenden</button>
</form>
```

### 7. **Semantische Elemente**
HTML5 führt semantische Elemente ein, die den Code lesbarer und besser strukturiert machen.
- **`<header>`, `<footer>`, `<main>`, `<article>`, `<section>`, `<aside>`**: Diese Tags geben dem Dokument eine bessere semantische Struktur und helfen Suchmaschinen und Screenreadern, den Inhalt zu interpretieren.
```html
<header>
  <h1>Willkommen</h1>
</header>
<main>
  <article>
    <h2>Erster Artikel</h2>
    <p>Dies ist der Hauptinhalt des Artikels.</p>
  </article>
  <aside>
    <p>Zusätzliche Informationen oder Links</p>
  </aside>
</main>
<footer>
  <p>&copy; 2024 Meine Webseite</p>
</footer>
```

## Best Practices für HTML-Elemente
1. **Semantische Tags verwenden**: Nutze semantische Elemente, um die Struktur des Inhalts zu verbessern.
2. **Barrierefreiheit durch Attribute**: Verwende beschreibende Attribute wie `alt` für Bilder oder `aria-label` für Screenreader.
3. **Saubere Strukturierung und Einrückung**: Eine konsistente Einrückung macht den Code lesbarer und hilft beim Erkennen von Fehlern.