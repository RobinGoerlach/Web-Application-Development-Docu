**Cascading Style Sheets (CSS)** verwenden eine einfache Syntax, um das Erscheinungsbild von HTML-Elementen zu steuern. Die Syntax besteht aus Regeln, die festlegen, wie Elemente auf einer Webseite aussehen sollen. Jede Regel enthält Selektoren, Eigenschaften und Werte, die zusammen das Styling eines Elements beschreiben.

## Aufbau einer CSS-Regel

Eine CSS-Regel besteht grundsätzlich aus zwei Hauptbestandteilen:

1. **Selektor**: Definiert das HTML-Element oder die Elemente, auf die das Styling angewendet wird.
2. **Deklarationsblock**: Umfasst die spezifischen Styling-Anweisungen für das ausgewählte Element.

### Beispiel einer CSS-Regel:

```css
p {
  color: blue;
  font-size: 16px;
}
```

In diesem Beispiel wird die Schriftfarbe aller `<p>`-Elemente blau und die Schriftgröße auf 16 Pixel gesetzt.

## Selektoren

Selektoren in CSS bestimmen, welche HTML-Elemente gestylt werden. Es gibt mehrere Typen von Selektoren:

- **Elementselektor**: Wendet das Styling auf alle Instanzen eines bestimmten Elements an.
```css
h1 {
  color: red;
}
```
    
- **Klassenselektor**: Wird für alle Elemente mit einer bestimmten Klasse verwendet. Klassen werden mit einem Punkt (`.`) angegeben.
```css
.intro {
  font-style: italic; 
}
```
    
- **ID-Selektor**: Richtet das Styling auf ein einzelnes Element mit einer spezifischen ID, die mit einem Hash (`#`) gekennzeichnet wird.
```css
#header {
  background-color: lightgray; 
}
```
    
- **Attributselektor**: Wählt Elemente basierend auf Attributen (z.B. `type="text"`).
```css
input[type="text"] {
  border: 1px solid black; 
}
```
## Eigenschaften und Werte

Eine CSS-Deklaration besteht aus einer **Eigenschaft** und einem **Wert**, getrennt durch einen Doppelpunkt (`:`). Eigenschaften beschreiben den Aspekt des Designs, der beeinflusst wird (z. B. `color` oder `font-size`), während Werte angeben, wie diese Eigenschaft gestaltet wird.

Beispiel:
```css
color: blue; font-size: 14px;
```
Hier legt `color` die Schriftfarbe auf Blau fest und `font-size` die Schriftgröße auf 14 Pixel.
## Deklarationsblock

Der Deklarationsblock wird in geschweifte Klammern `{}` eingeschlossen und enthält eine oder mehrere Deklarationen. Jede Deklaration wird durch ein Semikolon (`;`) beendet, um die einzelnen Stilregeln zu trennen.

Beispiel:

```css
h1 {
  color: green;
  text-align: center;
  font-weight: bold;
}
```
## Kommentare in CSS

Kommentare können in CSS hinzugefügt werden, um den Code zu erklären oder Notizen zu hinterlassen. Kommentare beginnen mit `/*` und enden mit `*/`. Sie werden beim Rendern der Seite ignoriert.

```css
/* Diese Regel ändert die Hintergrundfarbe */ 
body {
   background-color: white; 
}
```
## Beispiel zur Veranschaulichung

Hier ist ein vollständiges Beispiel, das die oben genannten Grundlagen kombiniert:
```css
/* Styling für das Hauptheader-Element */ 
#main-header {
  background-color: #333;
  color: white;
  padding: 10px;
  text-align: center;
}  

/* Styling für allgemeine Paragrafen */ 
p {
  color: #666;
  line-height: 1.6;
}

/* Styling für Links innerhalb eines bestimmten Bereichs */ 
.sidebar a {
  color: blue;
  text-decoration: none;
}
```

### Zusammenfassung

- Eine CSS-Regel besteht aus einem Selektor und einem Deklarationsblock.
- Selektoren legen fest, welche HTML-Elemente gestylt werden.
- Deklarationen enthalten Eigenschaften und Werte, um das Styling festzulegen.
- Kommentare helfen, den CSS-Code übersichtlicher zu gestalten.