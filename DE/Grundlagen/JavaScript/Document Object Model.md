### Was ist das Document Object Model (DOM)?

Das DOM ist eine Darstellung eines HTML- oder XML-Dokuments in Form eines Objektes, das von JavaScript und anderen Programmiersprachen manipuliert werden kann. Es modelliert die logische Struktur des Dokuments als Baum von Knoten (Nodes). Jeder Knoten repräsentiert einen Teil des Dokuments, wie z. B. ein HTML-Tag, einen Text oder einen Kommentar.

Beispiel: Die folgende HTML-Struktur:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Beispiel</title>
  </head>
  <body>
    <div id="content">
       <p>Hallo Welt!</p>
    </div>
  </body>
</html>
```

Im obigen Beispiel ist `<html>` das Wurzelelement, und die anderen Tags sind dessen Kindknoten. Diese Beispiel wird im DOM wie folgt dargestellt:

```less
Document
 └── html
      ├── head
      │     └── title
      │          └── Text: "Beispiel"
      └── body
            └── div#content
                └── p
                   └── Text: "Hallo Welt!"
```

#### Wichtige Bestandteile des DOM:

1. **Document**: Das Wurzelobjekt, das das gesamte Dokument repräsentiert.
2. **Elemente**: Knoten, die HTML-Tags wie `<div>`, `<p>` oder `<h1>` repräsentieren.
3. **Attribute**: Eigenschaften von Elementen, wie `id`, `class` oder `src`.
4. **Textknoten**: Knoten, die den Text innerhalb von Elementen repräsentieren.
5. **Eltern- und Kindknoten**: Beziehungen zwischen den Knoten, die die Baumstruktur definieren.

---

### Zugriff auf das DOM mit JavaScript

#### `document`-Objekt

Das `document`-Objekt repräsentiert die gesamte Webseite. Es ist der Einstiegspunkt für die DOM-Manipulation.

Beispiele:

- Zugriff auf den Titel des Dokuments:
```javascript
    console.log(document.title); // "Beispiel"
    ```
    
- Zugriff auf den gesamten HTML-Inhalt:
	```javascript
    console.log(document.documentElement.outerHTML);
    ```
    
### Zugriff auf DOM-Elemente

#### `getElementById`

Wird verwendet, um ein Element mit einer bestimmten `id` auszuwählen:
```javascript
let element = document.getElementById("content"); 
console.log(element); // <div id="content">...</div>
```

#### `querySelector` und `querySelectorAll`

Erlaubt die Auswahl von Elementen mit CSS-Selektoren:
```javascript
let firstParagraph = document.querySelector("p"); 
let allParagraphs = document.querySelectorAll("p");
```

#### `getElementsByClassName` und `getElementsByTagName`

Wird verwendet, um mehrere Elemente basierend auf Klassen- oder Tag-Namen auszuwählen:
```javascript
let elements = document.getElementsByClassName("example"); 
let divs = document.getElementsByTagName("div");
```

---

### DOM-Inhalte und Attribute ändern

#### Ändern von Textinhalten

Mit `textContent` kann der Text eines Elements geändert werden:
```javascript
let element = document.getElementById("content"); 
element.textContent = "Neuer Text!";
```

#### Ändern von HTML-Inhalten

Mit `innerHTML` kann der HTML-Inhalt eines Elements geändert werden:
```javascript
element.innerHTML = "<strong>Starker Text!</strong>";
```

#### Ändern von Attributen

Mit `setAttribute` oder direkten Zugriffen können Attribute geändert werden:
```javascript
element.setAttribute("class", "new-class"); 
element.id = "new-id";
```

---

### Hinzufügen und Entfernen von DOM-Elementen

#### Elemente erstellen

Mit `document.createElement` können neue Elemente erstellt werden:
```javascript
let newElement = document.createElement("p"); 
newElement.textContent = "Neuer Absatz"; document.body.appendChild(newElement);
```

#### Elemente entfernen

Mit `removeChild` oder der `remove`-Methode können Elemente entfernt werden:
```javascript
let parent = document.getElementById("content"); 
let child = parent.querySelector("p"); 
parent.removeChild(child);
```

#### Elemente an spezifischen Positionen einfügen

Mit `insertBefore` kann ein Element an einer bestimmten Stelle eingefügt werden:
```javascript
let newElement = document.createElement("p"); 
newElement.textContent = "Neuer Absatz"; 
parent.insertBefore(newElement, parent.firstChild);
```

---

### Stile und Klassen dynamisch ändern

#### Klassen hinzufügen, entfernen und überprüfen

Verwende `classList` für die Arbeit mit Klassen:

```javascript
element.classList.add("highlight");
element.classList.remove("highlight"); console.log(element.classList.contains("highlight")); // true/false
```

#### CSS-Stile dynamisch ändern

Stile können direkt geändert werden:

```javascript
element.style.color = "blue"; 
element.style.fontSize = "20px";
```

---

### Fazit

Das **Document Object Model (DOM)** bildet die Grundlage für alle Interaktionen zwischen JavaScript und HTML. Es erlaubt die Manipulation von Inhalten, Strukturen und Stilen einer Webseite. Indem du die grundlegenden DOM-APIs beherrschst, kannst du dynamische und interaktive Inhalte erstellen.

Wenn du tiefer in die DOM-Manipulation einsteigen möchtest, lohnt sich ein Blick auf **[DOM Manipulation In Depth](DOM%20Manipulation%20In%20Depth.md)**, wo fortgeschrittene Techniken wie Shadow DOM, Performance-Optimierung und die Arbeit mit komplexeren Knotenstrukturen behandelt werden.

Für die Arbeit mit Benutzerinteraktionen und Ereignissen solltest du den separaten Artikel zu **[Events](Events.md)** lesen, in dem Themen wie Event-Bubbling, Delegation und praktische Beispiele erklärt werden.