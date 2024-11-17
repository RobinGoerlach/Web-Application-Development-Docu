## **Einführung**

Web APIs sind Schnittstellen, die von Webbrowsern bereitgestellt werden, um auf Funktionen des Browsers oder des Geräts zuzugreifen. Sie ermöglichen es, komplexe und interaktive Anwendungen zu erstellen, ohne dass externe Bibliotheken erforderlich sind.

---
### 1. **DOM API**

Die DOM API ist die Grundlage für die Manipulation von HTML und CSS im Browser.

- **Funktionen und Objekte**: Zugriff auf Elemente mit `document.querySelector`, Hinzufügen und Entfernen von Klassen, Ändern von Attributen.
- **Beispiele**:
```javascript
    let element = document.querySelector("#example"); 
    element.textContent = "Neuer Text"; 
    element.classList.add("highlight");
```
    
---
### 2. **Fetch API**

Ermöglicht das Abrufen von Ressourcen und Daten aus dem Netzwerk. Sie ist eine moderne Alternative zu `XMLHttpRequest`.

- **Hauptfunktionen**: Senden von HTTP-Anfragen, Umgang mit JSON-Antworten.
- **Beispiel**:
```javascript
    fetch("https://api.example.com/data")
         .then(response => response.json())
         .then(data => console.log(data))     
         .catch(error => console.error("Fehler:", error));
```
---
### 3. **Geolocation API**

Bietet Zugriff auf die geografische Position des Benutzers (mit dessen Erlaubnis).

- **Funktionen**: Bestimmen der aktuellen Position, Verfolgen von Standortänderungen.
- **Beispiel**:
```javascript
    navigator.geolocation.getCurrentPosition(
        position => {
            console.log(`Breite: ${position.coords.latitude}, 
            Länge: ${position.coords.longitude}`);
        },
        error => console.error("Fehler:", error) );
```
    
---
### 4. **Canvas API**

Ermöglicht die Erstellung und Bearbeitung von 2D-Grafiken direkt im Browser.

- **Hauptanwendungen**: Spiele, Diagramme, Animationen.
- **Beispiel**:
```javascript
    let canvas = document.getElementById("myCanvas"); 
    let ctx = canvas.getContext("2d"); 
    ctx.fillStyle = "blue"; ctx.fillRect(10, 10, 100, 50);
```
    
---
### 5. **Web Storage API**

Speichern von Daten lokal im Browser, entweder im **localStorage** (dauerhaft) oder **sessionStorage** (sitzungsspezifisch).

- **Beispiel**:
```javascript
    localStorage.setItem("username", "JohnDoe"); 
    let user = localStorage.getItem("username"); 
    console.log(user); // "JohnDoe"
```
    
---
### 6. **Notification API**

Ermöglicht es Webanwendungen, Benachrichtigungen an den Benutzer zu senden.

- **Beispiel**:
```javascript
    if (Notification.permission === "granted") {
         new Notification("Hallo, Benutzer!"); 
    } else {
         Notification.requestPermission().then(permission => {
             if (permission === "granted") {
                 new Notification("Erlaubnis erteilt!");
             }     
         });
    }
```
---
### 7. **File API**

Erlaubt das Lesen von Dateien, die der Benutzer hochlädt, und den Zugriff auf Dateiinformationen.

- **Beispiel**:
```javascript
    let fileInput = document.querySelector("#fileInput"); 
    fileInput.addEventListener("change", () => {
         let file = fileInput.files[0];
         console.log(`Dateiname: ${file.name}`);
    });
```
    
---
### 8. **WebRTC API**

Unterstützt Echtzeitkommunikation wie Video- und Audioanrufe direkt im Browser.

- **Anwendungen**: Videokonferenzen, Bildschirmfreigabe.

---
### 9. **Intersection Observer API**

Effizienter Umgang mit Scroll-Ereignissen, z. B. zum Laden von Bildern oder Auslösen von Animationen, wenn Elemente in den sichtbaren Bereich scrollen.

- **Beispiel**:
    
```javascript
    let observer = new IntersectionObserver(entries => {
         entries.forEach(entry => {
           if (entry.isIntersecting) {
             console.log("Element sichtbar!");
           }
         });
    });
    observer.observe(document.querySelector("#target"));
```

---
### 10. **Web Animations API**

Ermöglicht das Erstellen von Animationen direkt mit JavaScript.

- **Beispiel**:
```javascript
    let element = document.querySelector("#animate"); 
    element.animate(
         [{ transform: "translateX(0px)" }, { transform: "translateX(100px)" }],
         { duration: 1000, iterations: Infinity } 
    );
```
    
---
### 11. **Weitere APIs**

- **Speech Recognition API**: Sprachbefehle erkennen und verarbeiten.
- **Clipboard API**: Zugriff auf die Zwischenablage.
- **Battery Status API**: Informationen über den Batteriestatus des Geräts.

---
### Fazit

Web APIs bieten eine enorme Bandbreite an Möglichkeiten, um moderne, interaktive und leistungsfähige Webanwendungen zu erstellen. Eine gute Dokumentation sollte die häufigsten Anwendungsfälle abdecken, aber auch auf die offiziellen Dokumentationen wie MDN Web Docs verweisen.
