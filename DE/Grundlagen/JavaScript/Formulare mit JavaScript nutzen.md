Formulare sind ein integraler Bestandteil von Webseiten, die Benutzern ermöglichen, Daten einzugeben und zu senden. JavaScript bietet leistungsstarke Werkzeuge, um Formulare dynamisch zu manipulieren, Eingaben zu validieren und die Benutzererfahrung zu verbessern.

---

## Zugriff auf Formulare und ihre Elemente

### Zugriff auf Formularelemente

Mit JavaScript kannst du auf Formulare und ihre Eingabeelemente zugreifen:

- **Formulare im Dokument**: Über `document.forms` oder `getElementById`.
- **Elemente eines Formulars**: Mit `form.elements`.

**Beispiel**:

```javascript
let form = document.getElementById("myForm"); 
let usernameInput = form.elements["username"]; 
console.log(usernameInput.value); // Wert des Eingabefeldes
```

### Dynamisches Ändern von Werten

Du kannst Eingabewerte direkt über JavaScript ändern:

```javascript
usernameInput.value = "JohnDoe";
```

---

## Validierung von Formulareingaben

Die Validierung von Eingaben ist ein zentraler Schritt, um sicherzustellen, dass die Benutzerdaten den Anforderungen entsprechen.

### HTML5-Validierung erweitern

HTML5 bietet grundlegende Validierungsfunktionen wie `required`, `pattern` und `type`. Diese können durch JavaScript ergänzt werden.

**HTML-Beispiel**:

```html
<form id="myForm">
   <input type="text" name="username" required>
   <input type="email" name="email">
   <button type="submit">Absenden</button> 
</form>
```

### JavaScript-basierte Validierung

Mit JavaScript kannst du benutzerdefinierte Validierungen implementieren.

**Beispiel**:

```javascript
form.addEventListener("submit", (event) => {
  let username = form.elements["username"];
  if (!username.value) {
    event.preventDefault(); // Verhindert das Absenden des Formulars
    alert("Der Benutzername ist erforderlich!");
  }
});
```

### Benutzerfreundliche Fehlermeldungen

Anstelle eines `alert` kannst du benutzerfreundliche Fehlermeldungen direkt im Formular anzeigen:

```javascript
let errorMessage = document.createElement("div");
errorMessage.className = "error"; 
form.insertBefore(errorMessage, form.firstChild);  

form.addEventListener("submit", (event) => {
  let email = form.elements["email"];
  if (!email.value.includes("@")) {
    event.preventDefault();
    errorMessage.textContent =
         "Bitte geben Sie eine gültige E-Mail-Adresse ein.";
  }
});
```

Hier ist eine vertiefte Betrachtung von Themen  rund um **FormData**. Der Artikel **[Einfaches Arbeiten mit Formulardaten](Einfaches%20Arbeiten%20mit%20Formulardaten.md)** bietet Informationen zu **benutzerdefinierte Validierungen** und **dynamische Formularmanipulation**.

---
## Dynamische Formularmanipulation

### Hinzufügen und Entfernen von Eingabefeldern

Formularelemente können dynamisch hinzugefügt oder entfernt werden:

```javascript
let newInput = document.createElement("input");
newInput.type = "text"; 
newInput.name = "newField"; 
form.appendChild(newInput);  
newInput.remove(); // Entfernt das Feld
```

### Aktivieren/Deaktivieren von Buttons

Buttons können basierend auf der Eingabe dynamisch aktiviert oder deaktiviert werden:

```javascript
let submitButton = form.elements["submit"];
form.elements["username"].addEventListener("input", (event) => {
     // Deaktiviert den Button, wenn das Feld leer ist 
     submitButton.disabled = !event.target.value; 
});
```

---

## Verarbeitung von Formulardaten

### Verhindern des Standardverhaltens

Das `submit`-Event kann abgefangen werden, um benutzerdefinierte Verarbeitung durchzuführen:

``javascript
form.addEventListener("submit", (event) => {
     event.preventDefault(); // Verhindert das Standard-Submit-Verhalten
     console.log("Formular erfolgreich verarbeitet!");
});

### Verwendung von `FormData`

Das `FormData`-Objekt erleichtert das Sammeln von Formulardaten und das Senden per Fetch API:

```javascript
form.addEventListener("submit", (event) => {
     event.preventDefault();
     let formData = new FormData(form);
     // Gibt den Wert des Eingabefelds "username" aus
     
     console.log(formData.get("username"));       
     // Daten per Fetch API senden
     fetch("/submit", {
              method: "POST",
              body: formData,
     }).then(response => console.log("Daten gesendet!")); 
});
```

---

## Beispiele für interaktive Funktionen

### Autovervollständigung

Mit JavaScript kannst du eine einfache Autovervollständigung implementieren:

```javascript
let suggestions = ["Alice", "Bob", "Charlie"];
form.elements["username"].addEventListener("input", (event) => {
     let match = suggestions.filter(name => 
          name.startsWith(event.target.value));
     console.log("Vorschläge:", match);
});
```

### Fortschrittsanzeige

Erstelle eine Fortschrittsanzeige basierend auf den ausgefüllten Feldern:

```javascript
let progress = document.getElementById("progress");
form.addEventListener("input", () => {
     let filled = Array.from(form.elements).filter(input => 
        input.value).length;
     let total = form.elements.length;
     progress.value = (filled / total) * 100; // Fortschritt in Prozent });
```

---
Ein wichtiges Thema neben **[Sicherheit](JavaScript%20Sicherheit.md)** ist **[Zugänglichkeit](JavaScript%20Accessibility.md) (Accessibility)**, es bezieht sich auf die Gestaltung von Webseiten und Anwendungen, damit sie für alle Benutzer, einschließlich Menschen mit Behinderungen, leicht zugänglich sind. In Bezug auf Formulare bedeutet das, sicherzustellen, dass Benutzer mit unterschiedlichen Bedürfnissen (z. B. Sehbehinderungen, motorische Einschränkungen oder kognitive Beeinträchtigungen) das Formular effektiv nutzen können.

----
## Fazit

JavaScript eröffnet zahlreiche Möglichkeiten, Formulare dynamisch und interaktiv zu gestalten. Durch Validierung, Manipulation und Verarbeitung von Formulardaten kannst du die Benutzererfahrung verbessern und sicherstellen, dass die eingegebenen Daten den Anforderungen entsprechen.
