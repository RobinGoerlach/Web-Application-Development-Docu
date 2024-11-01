CSS-Eigenschaften sind der Kern von CSS und ermöglichen die Kontrolle über das Erscheinungsbild von HTML-Elementen. Jede Eigenschaft legt einen spezifischen Aspekt des Designs fest, z.B. Farbe, Schriftgröße oder Abstände. Jede Eigenschaft ist mit einem **Wert** verbunden, der die genaue Ausprägung festlegt.

## 1. Farben und Hintergründe

### color

Die `color`-Eigenschaft bestimmt die Textfarbe eines Elements. Farben können auf verschiedene Weisen angegeben werden:

- **Benannte Farben**: Vordefinierte Farben wie `red`, `blue`, `green`, usw.
- **Hexadezimale Werte**: Farbe in hexadezimalem Format, z.B. `#ff5733`.
- **RGB-Farben**: Definiert Farben durch Rot-, Grün- und Blauwerte, z.B. `rgb(255, 87, 51)`.
- **RGBA-Farben**: Wie RGB, aber mit einem zusätzlichen Wert für die Transparenz (Alpha-Kanal), z.B. `rgba(255, 87, 51, 0.5)`.

Beispiel:

```css
p {
  color: #333; /* dunkles Grau */
}
```

### background-color

Die `background-color`-Eigenschaft legt die Hintergrundfarbe eines Elements fest.

```css
div {
  background-color: lightblue;
}
```

## 2. Schrift-Eigenschaften

### font-size

Die `font-size`-Eigenschaft bestimmt die Schriftgröße. Sie kann in verschiedenen Einheiten angegeben werden:

- **px**: Feste Pixelgröße, z.B. `16px`.
- **em**: Relativ zur Schriftgröße des übergeordneten Elements, z.B. `1.5em`.
- **rem**: Relativ zur Schriftgröße des Wurzelelements (`<html>`), z.B. `1.2rem`.
- **%**: Prozentual relativ zur Schriftgröße des übergeordneten Elements, z.B. `120%`.

Beispiel:

```css
h1 {
  font-size: 24px;
}
```
### font-family

Die `font-family`-Eigenschaft definiert die Schriftart eines Textes. Es ist gängig, mehrere Schriften als Fallback anzugeben, falls eine Schriftart nicht verfügbar ist.

```css
p {
  font-family: Arial, sans-serif;
}
```

### font-weight

`font-weight` steuert die Dicke des Textes. Häufige Werte sind `normal`, `bold`, `lighter`, oder Zahlen von `100` bis `900`.

```css
strong {
  font-weight: bold;
}
```

---

## 3. Abstände

CSS bietet zwei Hauptwerkzeuge für Abstände um Elemente: `margin` und `padding`.

### padding

Die `padding`-Eigenschaft legt den Innenabstand (Abstand zwischen Inhalt und Rand) eines Elements fest. Sie kann einen einzigen Wert oder vier Werte (oben, rechts, unten, links) enthalten:

```css
div {     padding: 10px; /* Gleicher Innenabstand auf allen Seiten */ }
```

Oder differenziert:

```css
div {
  padding: 10px 15px 20px 5px; /* Oben, Rechts, Unten, Links */
}
```

### margin

`margin` steuert den Außenabstand zwischen einem Element und den benachbarten Elementen. Es folgt denselben Prinzipien wie `padding`.

```css
h2 {
  margin: 20px 0; /* Oben und unten 20px, rechts und links 0 */
}
```

---

## 4. Rahmen und Umrandungen

### border

Die `border`-Eigenschaft fügt einen Rahmen um ein Element hinzu. Sie besteht normalerweise aus drei Werten: Breite, Stil und Farbe.

Beispiel:
```css
img {
  border: 2px solid black; 
}
```

Weitere Details:

- **border-width**: Dicke des Rahmens, z.B. `1px`, `medium`, `thin`.
- **border-style**: Rahmentyp, z.B. `solid`, `dashed`, `dotted`, usw.
- **border-color**: Farbe des Rahmens.

---

## Beispiel zur Kombination von Eigenschaften

Hier ist ein Beispiel, das einige der oben genannten Eigenschaften kombiniert, um das Aussehen einer Textbox zu gestalten:

```css
.textbox {
  background-color: #f0f0f0; /* Heller Hintergrund */
  color: #333; /* Dunkler Text */
  font-size: 16px; /* Schriftgröße */
  font-family: Arial, sans-serif; /* Schriftart */
  padding: 15px; /* Innenabstand */
  margin: 20px 0; /* Außenabstand oben und unten */
  border: 1px solid #ccc; /* Rahmen */
}
```

---

## Zusammenfassung

CSS-Eigenschaften und ihre Werte erlauben dir:

- **Farben** zu steuern und dem Text sowie Hintergründen visuelles Interesse zu verleihen.
- **Schriftgröße und -stil** anzupassen, um eine klare Hierarchie im Text zu schaffen.
- **Abstände und Rahmen** zu definieren, um Elemente voneinander zu trennen und Layouts zu gestalten.

Diese Eigenschaften bieten eine Basis, um Webseiten einheitlich und benutzerfreundlich zu gestalten. Mit einem klaren Verständnis der Eigenschaften und ihrer Werte kannst du präzise und ansprechende Designs entwickeln.
