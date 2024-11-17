# Best Practices Schutzmaßnahmen

JavaScript ist eine der meistgenutzten Programmiersprachen für Webanwendungen, was sie zu einem Hauptziel für Angriffe macht. Um deine Anwendungen sicher zu gestalten, ist es wichtig, die häufigsten Bedrohungen zu kennen und Gegenmaßnahmen zu implementieren.

---

## **1. Schutz vor Cross-Site Scripting (XSS)**

### Was ist XSS?

XSS tritt auf, wenn Angreifer bösartigen Code in eine Webseite einschleusen, der von anderen Benutzern ausgeführt wird. Dies geschieht oft durch Eingabefelder oder URLs.

### Maßnahmen gegen XSS

1. **Eingaben validieren und bereinigen**:
    
    - Validierung: Überprüfe Benutzereingaben auf erwartete Formate.
    - Bereinigung: Entferne gefährliche Zeichen wie `<`, `>`, oder JavaScript-Schlüsselwörter.
    
```javascript
function sanitizeInput(input) {
     return input.replace(/</g, "&lt;").replace(/>/g, "&gt;");
}
```
    
2. **Ausgabe escapen**: Verwende HTML-Escaping, bevor du Benutzereingaben in das DOM einfügst.
    
```javascript
let userInput = sanitizeInput("<script>alert('XSS')</script>"); document.getElementById("output").textContent = userInput;
```
    
3. **CSP (Content Security Policy) einsetzen**: Eine CSP verhindert die Ausführung nicht vertrauenswürdiger Skripte:
    
```html
<meta http-equiv="Content-Security-Policy" content="default-src 'self'; script-src 'self';">
```  

---

## **2. Schutz vor Cross-Site Request Forgery (CSRF)**

### Was ist CSRF?

CSRF-Angriffe zwingen einen Benutzer, ohne sein Wissen Anfragen an eine Webseite zu senden, bei der er authentifiziert ist.

### Maßnahmen gegen CSRF

1. **CSRF-Tokens verwenden**: Füge ein verstecktes CSRF-Token in Formulare ein und überprüfe es serverseitig.
    
```html
<input type="hidden" name="csrf_token" value="dein_token">
```
    
2. **SameSite-Cookies aktivieren**: Setze Cookies so, dass sie nur von der ursprünglichen Domain gesendet werden.
    
```http
Set-Cookie: sessionId=abc123; SameSite=Strict;
```
    
3. **Methoden-Restriktion**: Erlaube wichtige Aktionen nur für `POST`- oder `PUT`-Methoden.
    
---

## **3. Schutz vor Clickjacking**

### Was ist Clickjacking?

Ein Angreifer überlagert eine vertrauenswürdige Webseite mit einer unsichtbaren Schicht, um Benutzeraktionen zu manipulieren.

### Maßnahmen gegen Clickjacking

1. **`X-Frame-Options`-Header setzen**: Verhindere, dass deine Seite in Frames eingebettet wird.
    
```http
X-Frame-Options: DENY
```
    
2. **CSP nutzen**: Beschränke die Erlaubnis für Frames:
    
```http
Content-Security-Policy: frame-ancestors 'none';
```
    
---

## **4. Sichere Speicherung und Verarbeitung von Daten**

### Keine sensiblen Daten im Client speichern

- Vermeide die Speicherung von Passwörtern, Tokens oder API-Schlüsseln in `localStorage` oder `sessionStorage`.
- Verwende stattdessen sichere Cookies mit `HttpOnly`-Attribut:
    
```http
Set-Cookie: authToken=secure_token; HttpOnly; Secure;
```    

### Verschlüsselung sensibler Daten

- Nutze Web Cryptography API für die Verschlüsselung im Browser:
    
```javascript
async function encryptData(data, key) {
     let encodedData = new TextEncoder().encode(data);
     return await crypto.subtle.encrypt({ name: "AES-GCM", iv: key }, key, encodedData); 
}
```  

---

## **5. Sichere Nutzung von Drittanbieter-Skripten**

### Nur vertrauenswürdige Skripte laden

- Lade Skripte nur von vertrauenswürdigen Quellen.
- Nutze Subresource Integrity (SRI), um sicherzustellen, dass externe Skripte nicht manipuliert wurden:
    
```html
<script src="https://example.com/script.js" 
        integrity="sha384-abc123" crossorigin="anonymous"></script>
```    

---

## **6. Schutz vor Code-Injection**

### Verwendung sicherer APIs

- Vermeide dynamische Ausführung von JavaScript mit `eval` oder `Function`.
    
```javascript
// Unsicher 
eval("alert('Gefährlich!')");
// Sicher
console.log("Keine dynamische Ausführung!");
```   

### DOM-basierte Sicherheitsmaßnahmen

- Vermeide direktes Einfügen von HTML mit `innerHTML`. Nutze stattdessen `textContent`:
    
```javascript
// Unsicher 
element.innerHTML = userInput;  
// Sicher 
element.textContent = userInput;
```
 
---

## **7. Zugriffskontrolle und Berechtigungen**

### Schutz sensibler Aktionen

- Prüfe, ob Benutzer authentifiziert und autorisiert sind, bevor kritische Aktionen ausgeführt werden.
- Nutze serverseitige Überprüfungen:
    
```javascript
app.post("/delete", (req, res) => {
     if (req.user.role !== "admin") {
              res.status(403).send("Nicht autorisiert");
     } else {
              // Aktion durchführen
     }
});
```

---

## **8. Logging und Monitoring**

### Verdächtige Aktivitäten verfolgen

- Implementiere Logging für sicherheitsrelevante Ereignisse, wie fehlgeschlagene Login-Versuche.
- Nutze Webhooks oder Alarme, um ungewöhnliches Verhalten zu melden.

---

## Fazit

Sicherheitsbewusste Programmierung ist ein essenzieller Teil der Entwicklung moderner JavaScript-Anwendungen. Mit den oben genannten Best Practices kannst du gängige Sicherheitsrisiken wie XSS, CSRF und Clickjacking minimieren und die Integrität deiner Anwendung gewährleisten.
