Typografie ist ein wesentlicher Aspekt des Webdesigns, da sie das Leseerlebnis und die visuelle Wirkung einer Website stark beeinflusst. CSS bietet zahlreiche Möglichkeiten zur Textgestaltung und ermöglicht dir, Schriftarten, Größen, Abstände und viele weitere Aspekte zu steuern. In diesem Artikel erfährst du, wie du Texte in CSS ansprechend und leserfreundlich gestaltest.

## 1. Schriftarten festlegen (`font-family`)

Die `font-family`-Eigenschaft bestimmt die Schriftart eines Elements. Es ist üblich, eine Liste von Schriftarten anzugeben, sodass der Browser eine Alternative verwenden kann, wenn die primäre Schriftart nicht verfügbar ist.
```css
body {
  /* Fallback zu sans-serif, falls Arial nicht verfügbar ist */ 
  font-family: Arial, sans-serif; 
}
```

Typisch ist eine Mischung aus serifenlosen Schriften für moderne Designs (`Arial`, `Helvetica`) und Serifenschriften (`Times New Roman`) für einen klassischen Look. Für individuelle Stile eignen sich **Google Fonts** oder **Adobe Fonts**, die einfach in eine Webseite eingebunden werden können.

---

## 2. Schriftgröße (`font-size`)

Die `font-size`-Eigenschaft legt die Größe des Textes fest. Es gibt mehrere gängige Einheiten:
- **px**: Feste Pixelgröße, z.B. `16px`.
- **em**: Relativ zur Schriftgröße des Elternelements, z.B. `1.2em`.
- **rem**: Relativ zur Schriftgröße des Wurzelelements (`<html>`), z.B. `1rem = 16px`.
- **%**: Prozentuale Schriftgröße relativ zum Elternelement.
```css
h1 {
  font-size: 2rem; /* Skaliert basierend auf der Root-Schriftgröße */
}
```

### Responsive Schriftgrößen

Mit `clamp()` lassen sich Schriftgrößen definieren, die sich dynamisch an verschiedene Bildschirmgrößen anpassen:
```css
p {
  /* Dynamisch zwischen 1rem und 2rem */
  font-size: clamp(1rem, 2vw + 1rem, 2rem); 
}
```

---

## 3. Schriftstärke (`font-weight`)

Mit `font-weight` bestimmst du die Dicke des Textes. Typische Werte sind `normal`, `bold`, oder Zahlen von `100` bis `900` (je nach verfügbaren Schriftarten).
```css
strong {
  font-weight: bold; /* Fettdruck */
}
```

Feinere Gewichtungen wie `300` (light), `500` (medium) oder `700` (bold) ermöglichen zusätzliche Abstufungen, falls die Schrift diese Optionen bietet.

---

## 4. Schriftstil (`font-style`)

`font-style` gibt an, ob der Text normal oder kursiv dargestellt werden soll. Die häufigsten Werte sind:
- `normal`: Standard-Schriftstil.
- `italic`: Kursivschrift.
- `oblique`: Schräge Schrift (unterschiedlich zu kursiv).
```css
blockquote {
  font-style: italic; 
}
```

---

## 5. Zeilenhöhe (`line-height`)

Die `line-height`-Eigenschaft legt den Abstand zwischen den Zeilen fest und beeinflusst die Lesbarkeit erheblich. Ein Wert zwischen `1.4` und `1.6` ist für Fließtext oft optimal.
```css
body {
  line-height: 1.5; /* 1.5-fache Höhe der Schriftgröße */ 
}
```

---

## 6. Buchstaben- und Wortabstand (`letter-spacing` und `word-spacing`)

- **letter-spacing**: Abstand zwischen den Buchstaben.
- **word-spacing**: Abstand zwischen den Wörtern.
```css
h1 {
  letter-spacing: 0.05em; /* Abstand zwischen Buchstaben vergrößern */
}
```

Diese Eigenschaften helfen, die Lesbarkeit zu verbessern und können das Design je nach Schriftart unterstützen.

---

## 7. Textausrichtung (`text-align`)

Mit `text-align` bestimmst du, wie der Text innerhalb eines Elements ausgerichtet wird. Mögliche Werte sind:
- **left**: Text linksbündig.
- **right**: Text rechtsbündig.
- **center**: Text zentriert.
- **justify**: Text im Blocksatz.
```css
p {
  text-align: justify; /* Text gleichmäßig auf die Breite verteilen */
}
```

`justify` sorgt für eine ausgeglichene Textverteilung, während `center` oft für Titel und Überschriften verwendet wird.

---

## 8. Textdekorationen (`text-decoration`)

Mit `text-decoration` kannst du Effekte wie Unterstreichungen, Durchstreichungen und Überstreichungen hinzufügen. Die häufigsten Werte sind:
- **underline**: Unterstrichener Text.
- **line-through**: Durchgestrichener Text.
- **overline**: Überstrichener Text.
- **none**: Keine Dekoration.
```css
a {
  text-decoration: none; /* Unterstreichung für Links entfernen */ 
}
```

---

## 9. Textschatten (`text-shadow`)

Mit `text-shadow` kannst du Schatten für Texte hinzufügen, um Tiefe und visuelle Effekte zu erzeugen.

Syntax: `text-shadow: x-offset y-offset blur-radius color;`
```css
h1 {
  text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
}
```

In diesem Beispiel wird ein leichter, weicher Schatten auf den Text angewendet.

---

## 10. Textumbruch und -überlauf (`word-break`, `white-space`, und `text-overflow`)

### Textumbruch (`word-break`)

`word-break` steuert, wie der Text in Zeilen umbricht. Die häufigsten Werte sind:

- `normal`: Zeilenumbruch nur an Wortenden.
- `break-all`: Zeilenumbruch kann an jeder Stelle erfolgen.
- `keep-all`: Kein Zeilenumbruch mitten im Wort.

```css 
p {
  word-break: break-word; /* Längere Wörter umbrechen */ 
}
```

### Weißraum steuern (`white-space`)

Die `white-space`-Eigenschaft kontrolliert, wie Leerzeichen und Zeilenumbrüche angezeigt werden.

- **normal**: Leerzeichen und Zeilenumbrüche werden normal angezeigt.
- **nowrap**: Kein Zeilenumbruch, der Text bleibt in einer Zeile.
- **pre**: Beibehalten von Leerzeichen und Zeilenumbrüchen (wie in `<pre>`-Elementen).
```css
code {
  white-space: pre;
}
```

### Textüberlauf (`text-overflow`)
`text-overflow` wird verwendet, um überlaufenden Text zu kennzeichnen, z.B. mit „...“. Diese Eigenschaft funktioniert nur bei `overflow: hidden;` und `white-space: nowrap;`.
```css
.truncated {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis; /* Zeigt "..." am Ende des Textes */ 
}
```

---

## Beispiel für CSS Typografie

Hier ist ein Beispiel, das die grundlegenden Typografieeigenschaften kombiniert, um ein ansprechendes Textdesign zu erstellen.

HTML:
```html
<div class="article">
  <h1>CSS Typografie</h1>
  <p>Die Gestaltung und Lesbarkeit von Texten
     ist ein zentraler Aspekt im Webdesign.</p>
</div>
```

CSS:
```css
body {
  font-family: 'Open Sans', sans-serif;
  font-size: 16px;
  line-height: 1.6;
  color: #333; 
}
h1 {
  font-size: 2.5rem;
  font-weight: 700;
  letter-spacing: 0.05em;
  text-align: center;
  text-transform: uppercase;
  color: #2c3e50; 
}
p {
  margin: 1rem 0;
  text-align: justify; 
}
```

### Erläuterung

- Der Text im `body` hat eine serifenlose Schriftart und einen gut lesbaren Zeilenabstand.
- Das `<h1>`-Element ist größer, zentriert und mit Buchstabenabstand versehen, was es als Titel hervorhebt.
- Die `<p>`-Absätze sind im Blocksatz und unterstützen eine gleichmäßige Textverteilung.

---

## Zusammenfassung

CSS-Typografie ist entscheidend für die visuelle Gestaltung und die Lesbarkeit einer Website. Mit CSS kannst du:

- **Schriftarten und -größen** festlegen, um eine klare Hierarchie zu schaffen.
- **Textausrichtung, -abstände und -spezialeffekte** wie Schatten hinzufügen, um einen modernen Look zu erzeugen.
- **Erweiterte Eigenschaften** wie `word-break` und `text-overflow` nutzen, um sicherzustellen, dass dein Text auf verschiedenen Bildschirmgrößen gut aussieht.

Ein klares Verständnis der Typografie in CSS hilft dir, ansprechende, gut lesbare und visuell attraktive Texte zu gestalten.