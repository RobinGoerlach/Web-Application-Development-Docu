# Ereignisse (Events)

sind ein zentraler Bestandteil interaktiver Webseiten. Sie ermöglichen es, auf Aktionen des Benutzers – wie Klicks, Eingaben oder das Laden einer Seite – zu reagieren. In diesem Artikel werden die Grundlagen von Events, Event-Handling und fortgeschrittene Konzepte wie Event-Bubbling und Delegation behandelt.

---

## Was sind Events?

Ein Event repräsentiert eine Aktion oder ein Ereignis, das in einer Webseite stattfindet, wie z. B.:

- **Benutzeraktionen**: Klicken, Eingaben in ein Formular, Bewegen der Maus.
- **Systemereignisse**: Laden der Seite, Fehler im Skript, Änderungen an Elementen.

Beispiele für gängige Events:

- `click`: Benutzer klickt auf ein Element.
- `input`: Benutzer gibt Text in ein Eingabefeld ein.
- `submit`: Formular wird abgeschickt.
- `keydown`: Eine Taste wird gedrückt.

---

## Event-Handling

Mit Event-Handling kannst du Funktionen definieren, die als Reaktion auf bestimmte Events ausgeführt werden.

### Hinzufügen eines Event-Listeners

Die Methode `addEventListener` wird verwendet, um Event-Listener zu einem Element hinzuzufügen:

javascript

Copy code

`let button = document.querySelector("button"); button.addEventListener("click", () => {     console.log("Button wurde geklickt!"); });`

### Entfernen eines Event-Listeners

Mit `removeEventListener` kannst du Event-Listener wieder entfernen:

javascript

Copy code

`function handleClick() {     console.log("Button wurde geklickt!"); } button.addEventListener("click", handleClick); button.removeEventListener("click", handleClick);`

---

## Timer und Events kombinieren

Timer wie `setTimeout` und `setInterval` sind nützliche Werkzeuge, um zeitgesteuerte Aktionen in Verbindung mit Events zu implementieren.

### Verzögerte Aktionen mit `setTimeout`

Du kannst `setTimeout` verwenden, um eine Aktion nach einer bestimmten Verzögerung auszuführen:

javascript

Copy code

`button.addEventListener("click", () => {     setTimeout(() => {         console.log("3 Sekunden später...");     }, 3000); });`

### Wiederholte Aktionen mit `setInterval`

`setInterval` führt eine Aktion in regelmäßigen Abständen aus. Dies ist nützlich für wiederkehrende Aufgaben:

javascript

Copy code

``button.addEventListener("click", () => {     let count = 0;     let intervalId = setInterval(() => {         console.log(`Sekunde ${++count}`);         if (count === 5) {             clearInterval(intervalId); // Stoppt das Intervall nach 5 Sekunden         }     }, 1000); });``

### Timer abbrechen

Timer können mit `clearTimeout` und `clearInterval` gestoppt werden:

javascript

Copy code

`let timeoutId = setTimeout(() => {     console.log("Das wird nie ausgeführt"); }, 5000);  clearTimeout(timeoutId);`

----
## Event-Objekt

Jedes Event erzeugt ein **Event-Objekt**, das detaillierte Informationen über das Ereignis enthält. Es wird automatisch an den Event-Listener übergeben:

javascript

Copy code

`button.addEventListener("click", (event) => {     console.log(event.type); // "click"     console.log(event.target); // Element, auf dem das Event ausgelöst wurde });`

### Wichtige Eigenschaften des Event-Objekts

- `type`: Typ des Events (`click`, `input` usw.).
- `target`: Element, auf dem das Event ausgelöst wurde.
- `currentTarget`: Das Element, an das der Listener gebunden ist.
- `preventDefault()`: Verhindert die Standardaktion eines Events (z. B. das Absenden eines Formulars).
- `stopPropagation()`: Stoppt die Weiterleitung des Events im Event-Baum.

---

## Event-Bubbling und -Capturing

### Was ist Event-Bubbling?

Event-Bubbling beschreibt die Phase, in der ein Event vom Zielknoten (Target) nach oben durch den DOM-Baum wandert:

html

Copy code

`<div id="parent">   <button id="child">Klicken</button> </div>`

javascript

Copy code

`document.getElementById("parent").addEventListener("click", () => {     console.log("Parent geklickt!"); }); document.getElementById("child").addEventListener("click", () => {     console.log("Child geklickt!"); });`

Beim Klick auf `#child` wird zuerst die Nachricht `Child geklickt!` und anschließend `Parent geklickt!` ausgegeben.

### Was ist Event-Capturing?

Event-Capturing (oder "Trickle-Down") ist die Phase, in der das Event von der Wurzel bis zum Zielknoten wandert. Um diese Phase zu nutzen, wird ein zusätzlicher Parameter `true` an `addEventListener` übergeben:

javascript

Copy code

`document.getElementById("parent").addEventListener("click", () => {     console.log("Parent während Capturing!"); }, true);`

---

## Event-Delegation

### Warum Event-Delegation nutzen?

Anstatt jedem Element separat einen Listener hinzuzufügen, kannst du einen Listener auf einen gemeinsamen Elternknoten setzen und Events basierend auf ihrem Ziel (`event.target`) behandeln.

Beispiel:

html

Copy code

`<ul id="list">   <li>Eintrag 1</li>   <li>Eintrag 2</li> </ul>`

javascript

Copy code

``document.getElementById("list").addEventListener("click", (event) => {     if (event.target.tagName === "LI") {         console.log(`Geklickt: ${event.target.textContent}`);     } });``

---

## Häufige Event-Typen und ihre Anwendungen

1. **Maus-Events**
    - `click`, `dblclick`, `mousedown`, `mouseup`, `mousemove`, `mouseover`, `mouseout`
2. **Tastatur-Events**
    - `keydown`, `keyup`, `keypress`
    - Beispiel: Eine Aktion auslösen, wenn die Enter-Taste gedrückt wird:
        
        javascript
        
        Copy code
        
        `input.addEventListener("keydown", (event) => {     if (event.key === "Enter") {         console.log("Enter gedrückt!");     } });`
        
3. **Formular-Events**
    - `submit`, `input`, `change`, `focus`, `blur`
    - Beispiel: Eingaben validieren:
        
        javascript
        
        Copy code
        
        `form.addEventListener("submit", (event) => {     event.preventDefault(); // Verhindert das Standard-Formular-Submit     console.log("Formular abgeschickt!"); });`
        
4. **Seiten-Events**
    - `load`, `DOMContentLoaded`, `resize`, `scroll`
    - Beispiel: Scrollposition überwachen:
        
        javascript
        
        Copy code
        
        `window.addEventListener("scroll", () => {     console.log(window.scrollY); });`
        

---

## Fazit

Events sind das Herzstück interaktiver Webanwendungen. Sie erlauben es, Benutzeraktionen zu erfassen und darauf zu reagieren. Ein tiefes Verständnis von Event-Handling, Bubbling, Capturing und Delegation ist essenziell, um sauberen und effizienten Code zu schreiben.

Für fortgeschrittene Anwendungen lohnt es sich, Events mit DOM-Manipulationen und Techniken wie Shadow DOM zu kombinieren, um flexible und wartbare Anwendungen zu erstellen.