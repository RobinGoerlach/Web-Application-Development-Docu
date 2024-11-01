# in HTML, CSS und JavaScript

_[HTML](HTML/HTML%20Überblick.md)_, _[CSS](CSS/CSS%20Überblick.md)_ und _[JavaScript](JavaScript%20Überblick.md)_ sind die drei grundlegenden Technologien für die Erstellung und Gestaltung von Webseiten. Jedes hat seine eigene Aufgabe und Funktion im Webentwicklungsprozess und bildet zusammen die Basis für moderne, interaktive und ansprechende Websites.

## 1. HTML (HyperText Markup Language)

**[HTML](HTML/HTML%20Überblick.md)** ist die Auszeichnungssprache, die die Struktur und den Inhalt einer Webseite definiert. Es ermöglicht die Anordnung von Text, Bildern, Links und anderen Inhalten auf einer Webseite.

### Grundlegende HTML-Struktur

Ein einfaches [HTML](HTML/HTML%20Überblick.md)-Dokument enthält die grundlegenden Elemente:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">  
  <title>Meine Webseite</title>
</head>
<body>
  <h1>Willkommen auf meiner Webseite</h1>
     <p>Dies ist ein Beispiel für HTML-Struktur.</p>
</body>
</html>
```

### Wichtige HTML-Elemente

- **Überschriften** (`<h1>` bis `<h6>`): Strukturieren den Text in Hierarchien.
- **Absätze** (`<p>`): Definieren Textabsätze.
- **Links** (`<a href="URL">`): Erstellen Verknüpfungen zu anderen Seiten oder Ressourcen.
- **Bilder** (`<img src="URL" alt="Beschreibung">`): Binden Grafiken ein.
- **Listen** (`<ul>`, `<ol>`, `<li>`): Erstellen geordnete und ungeordnete Listen.

[HTML](HTML/HTML%20Überblick.md) dient also dazu, eine Webseite in ihre Bestandteile zu gliedern und jedem Element eine bestimmte Funktion zuzuweisen.

---

## 2. CSS (Cascading Style Sheets)

**[CSS](CSS/CSS%20Überblick.md)** wird verwendet, um das Design und Layout einer Webseite zu definieren. Es ermöglicht das Styling von HTML-Elementen, einschließlich Farben, Schriftarten, Abständen und Anordnungen.

### Grundlegende CSS-Syntax

[CSS](CSS/CSS%20Überblick.md) besteht aus Selektoren und Deklarationen. Ein Selektor wählt das zu stylende HTML-Element aus, und die Deklaration enthält die Eigenschaft und ihren Wert.
```css
/* CSS-Beispiel */
h1 {
  color: blue;
  font-size: 24px;
}
p {
  color: gray;
  line-height: 1.6;
}
```

### Einbindung von CSS

[CSS](CSS/CSS%20Überblick.md) kann auf verschiedene Weisen eingebunden werden:

1. **Inline**: Direkt im HTML-Tag mit dem `style`-Attribut.
2. **Intern**: Im `<style>`-Tag im `<head>`-Bereich des HTML-Dokuments.
3. **Extern**: Über eine separate CSS-Datei, die mit `<link rel="stylesheet" href="style.css">` verknüpft wird.

### Wichtige CSS-Konzepte

- **Farbe und Hintergrund**: Ändern Farben von Text und Hintergründen (`color`, `background-color`).
- **Schriften und Textstile**: Kontrollieren Schriftart, -größe und -gewicht (`font-family`, `font-size`, `font-weight`).
- **Abstände**: Verwenden von `margin` und `padding` zur Anpassung der Abstände.
- **Layout-Techniken**: Nutzung von `display`, `position`, `flexbox` und `grid`, um Inhalte zu positionieren und Layouts zu erstellen.

[CSS](CSS/CSS%20Überblick.md) ist dafür zuständig, eine Webseite visuell ansprechend zu gestalten und für eine einheitliche Darstellung zu sorgen.

---

## 3. JavaScript (JS)

**[JavaScript](JavaScript%20Überblick.md)** ist die Programmiersprache des Webs und wird verwendet, um Interaktivität und dynamische Funktionen zu einer Webseite hinzuzufügen. [JavaScript](JavaScript%20Überblick.md) ermöglicht das Reagieren auf Benutzereingaben, das Manipulieren von [HTML](HTML/HTML%20Überblick.md) und [CSS](CSS/CSS%20Überblick.md) und das Erstellen interaktiver Erlebnisse.

### Grundlegende JavaScript-Syntax

[JavaScript](JavaScript%20Überblick.md)-Code wird innerhalb von `<script>`-Tags geschrieben oder in eine separate Datei ausgelagert, die mit `<script src="script.js"></script>` eingebunden wird.

```javascript
// JavaScript-Beispiel
document.querySelector("button").addEventListener("click", function() {     
  alert("Button wurde geklickt!"); 
});
```

### Wichtige JavaScript-Konzepte

- **Variablen**: Speichern und Verwalten von Daten (mit `let`, `const` oder `var`).
- **Funktionen**: Definieren wiederverwendbare Codeblöcke.
- **DOM-Manipulation**: Zugriff und Änderungen an HTML-Elementen über das Document Object Model.
- **Ereignissteuerung**: Reagieren auf Benutzeraktionen wie Klicks, Eingaben oder Hover-Effekte.
- **Kontrollstrukturen**: Bedingte Anweisungen (`if`, `else`) und Schleifen (`for`, `while`) zur Steuerung des Programmflusses.

### Ein einfaches JavaScript-Beispiel

[JavaScript](JavaScript%20Überblick.md) kann verwendet werden, um eine Nachricht anzuzeigen, wenn ein Button geklickt wird:
```html
<button id="myButton">Klicke mich!</button>
<script>
  document.getElementById("myButton").addEventListener("click", function() {
       alert("Button wurde geklickt!");
   });
</script>
```

[JavaScript](JavaScript%20Überblick.md) erweitert [HTML](HTML/HTML%20Überblick.md) und [CSS](CSS/CSS%20Überblick.md), indem es eine interaktive und dynamische Benutzererfahrung ermöglicht.

---

## Zusammenwirken von HTML, CSS und JavaScript

[HTML](HTML/HTML%20Überblick.md), [CSS](CSS/CSS%20Überblick.md) und [JavaScript](JavaScript%20Überblick.md) arbeiten zusammen, um vollständige Webseiten zu erstellen:

1. **[HTML](HTML/HTML%20Überblick.md)** liefert die Struktur und den Inhalt der Webseite.
2. **[CSS](CSS/CSS%20Überblick.md)** sorgt für das Design und die optische Gestaltung.
3. **[JavaScript](JavaScript%20Überblick.md)** fügt Interaktivität hinzu und ermöglicht dynamische Funktionen.

Hier ist ein Beispiel, das das Zusammenspiel von HTML, CSS und JavaScript demonstriert:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Grundlagen von HTML, CSS und JavaScript</title>
  <style>
       /* CSS */
       body { font-family: Arial, sans-serif; text-align: center; }
       button { padding: 10px 20px; font-size: 16px; }
  </style>
</head>
<body>
  <!-- HTML -->
  <h1>Willkommen auf meiner Webseite</h1>
  <p>Diese Webseite ist mit HTML, CSS und JavaScript erstellt.</p>
  <button id="myButton">Klicke mich!</button>
  <script>
     // JavaScript
     document.getElementById("myButton").addEventListener("click", function() {
            alert("Button wurde geklickt!");
	 });
  </script>
</body>
</html>
```

Dieses Beispiel kombiniert die Struktur von [HTML](HTML/HTML%20Überblick.md), das Styling von [CSS](CSS/CSS%20Überblick.md) und die Interaktivität von [JavaScript](JavaScript%20Überblick.md), um eine vollständige, ansprechende Webseite zu erstellen.

---

## Zusammenfassung

[HTML](HTML/HTML%20Überblick.md), [CSS](CSS/CSS%20Überblick.md) und JavaScript bilden das Fundament der Webentwicklung:

- **[HTML](HTML/HTML%20Überblick.md)** definiert die Struktur und den Inhalt.
- **[CSS](CSS/CSS%20Überblick.md)** gestaltet das Aussehen und Layout.
- **[JavaScript](JavaScript%20Überblick.md)** fügt Interaktivität und dynamische Funktionen hinzu.

Ein solides Verständnis dieser drei Technologien ist notwendig, um moderne und interaktive Webseiten zu entwickeln. Sie ergänzen sich gegenseitig und sind als Kombination die Grundlage des modernen Webs.

---

Dieses Einführungsdokument bietet dir einen Überblick über die Rolle und die Funktionsweise von [HTML](HTML/HTML%20Überblick.md), [CSS](CSS/CSS%20Überblick.md) und [JavaScript](JavaScript%20Überblick.md) und gibt dir die Grundlage für den weiteren Aufbau deiner Webentwicklungsfähigkeiten.