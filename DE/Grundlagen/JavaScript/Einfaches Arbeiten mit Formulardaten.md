Das `FormData`-Objekt ermöglicht das Sammeln und Verarbeiten von Formulardaten in einer strukturierten Weise. Es ist besonders nützlich für das Senden von Daten an Server, da es automatisch die Namen und Werte der Eingabefelder eines Formulars erfasst.

### Erstellung eines `FormData`-Objekts

Das `FormData`-Objekt wird aus einem Formular erstellt:

```javascript
let formData = new FormData(document.getElementById("myForm"));
```

### Zugriff auf Formulardaten

Mit den Methoden `get`, `set`, und `append` kannst du auf die Daten zugreifen oder sie ändern:

```javascript
console.log(formData.get("username")); // Gibt den Wert des Feldes "username" aus
formData.set("username", "NewName");  // Überschreibt den Wert von "username"
formData.append("age", "30");         // Fügt ein neues Feld "age" hinzu
```

### Senden von Daten mit Fetch API

Das `FormData`-Objekt kann direkt an die Fetch API übergeben werden, um Daten an einen Server zu senden:

```javascript
fetch("/submit", {
     method: "POST",
     body: formData,
}).then(response => console.log("Daten erfolgreich gesendet!"));
```

### Beispiel: Dynamisches Hinzufügen von Feldern und Senden

```javascript
let form = document.getElementById("myForm"); 
form.addEventListener("submit", (event) => {
     event.preventDefault();
     // Dynamisches Hinzufügen eines zusätzlichen Feldes
     let formData = new FormData(form);
     formData.append("extraData", "value");
     fetch("/submit", {
              method: "POST",
              body: formData,
     }).then(response => console.log("Formulardaten gesendet!")); });
```

---

## **Benutzerdefinierte Validierungen**

Während HTML5-Validierungen für viele Standardfälle ausreichen, kannst du mit JavaScript spezifische Regeln implementieren und Benutzerfeedback bereitstellen.

### Eigene Validierungslogik

Erstelle benutzerdefinierte Validierungsregeln für Eingabefelder:

```javascript
let form = document.getElementById("myForm"); 
form.addEventListener("submit", (event) => {
     let username = form.elements["username"];
     let email = form.elements["email"];
     let isValid = true;      // Benutzerdefinierte Validierung
     if (username.value.length < 3) {
              isValid = false;
              username.setCustomValidity(
                 "Der Benutzername muss mindestens 3 Zeichen lang sein.");
     } else {
              username.setCustomValidity(""); // Fehler zurücksetzen
     } if (!email.value.includes("@")) {
              isValid = false;
              email.setCustomValidity(
                 "Bitte geben Sie eine gültige E-Mail-Adresse ein.");
     } else {
              email.setCustomValidity("");
     } if (!isValid) {
              event.preventDefault(); // Verhindert das Absenden bei Fehlern     
     }
});
```

### Dynamische Fehlermeldungen anzeigen

Zeige Fehlermeldungen direkt im DOM an, um die Benutzererfahrung zu verbessern:

```javascript
let errorContainer = document.getElementById("errors");
form.addEventListener("submit", (event) => {
     errorContainer.innerHTML = ""; // Vorherige Fehler löschen
     if (!username.value) {
              event.preventDefault();
              let error = document.createElement("div");
              error.textContent = "Benutzername darf nicht leer sein.";
              errorContainer.appendChild(error);
     }
});
```

---

## **Dynamische Formularmanipulation**

Formulare können mit JavaScript flexibel angepasst werden, indem Felder dynamisch hinzugefügt, entfernt oder modifiziert werden.

### Dynamisches Hinzufügen und Entfernen von Feldern

Du kannst Eingabefelder und andere Elemente zur Laufzeit erstellen und dem Formular hinzufügen:

```javascript
let form = document.getElementById("myForm");
let addButton = document.getElementById("addField");
addButton.addEventListener("click", () => {
     let newInput = document.createElement("input");
     newInput.type = "text";
     newInput.name = "newField";
     newInput.placeholder = "Neues Feld";
     form.appendChild(newInput); 
});
let removeButton = document.getElementById("removeField");
removeButton.addEventListener("click", () => {
let lastInput = form.querySelector("input:last-of-type");
if (lastInput) 
     lastInput.remove();
});
```

### Dynamisches Ändern von Feldern

Du kannst die Attribute und Werte vorhandener Felder dynamisch ändern:

```javascript
let username = form.elements["username"];
username.addEventListener("input", () => {
     if (username.value.length < 3) {
              username.style.borderColor = "red";
     } else {
              username.style.borderColor = "green";
     }
});
```

### Erstellen eines Formulars zur Laufzeit

Ein komplettes Formular kann mit JavaScript generiert werden:

```javascript
let newForm = document.createElement("form");
newForm.id = "dynamicForm";
newForm.method = "POST";
newForm.action = "/submit";
let input = document.createElement("input");
input.type = "text";
input.name = "username";
input.placeholder = "Benutzername";
let submitButton = document.createElement("button");
submitButton.type = "submit";
submitButton.textContent = "Absenden";
newForm.appendChild(input);
newForm.appendChild(submitButton);
document.body.appendChild(newForm);
```

---

## Fazit

Die Arbeit mit **FormData**, benutzerdefinierten Validierungen und dynamischer Formularmanipulation bietet mächtige Werkzeuge, um Formulare auf Webseiten funktional und benutzerfreundlich zu gestalten. Diese Techniken helfen, Formulare an die spezifischen Anforderungen deiner Anwendung anzupassen und eine verbesserte Benutzererfahrung zu bieten.
