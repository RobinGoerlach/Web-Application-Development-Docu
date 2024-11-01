## Modernen HTML5-Features: Übersicht über wichtige HTML5-Elemente und -Funktionen
HTML5 hat das Web revolutioniert, indem es eine Reihe neuer Elemente und Funktionen eingeführt hat, die dynamische, interaktive und visuell ansprechende Inhalte direkt in HTML ermöglichen. Zu den modernen HTML5-Features gehören die Elemente `<canvas>` und Inline-SVGs, die für Grafiken und Animationen genutzt werden können, sowie andere Tools, die die Flexibilität und Funktionalität von HTML erheblich erweitern.
## 1. Das `<canvas>`-Element
Das `<canvas>`-Element bietet eine Zeichenfläche, auf der man mithilfe von JavaScript Grafiken, Diagramme, Animationen und sogar Spiele erstellen kann. Es ist ein leeres HTML-Element, das nur in Kombination mit JavaScript funktioniert.
### Grundstruktur von `<canvas>`
Das `<canvas>`-Element selbst zeigt ohne JavaScript-Inhalte nichts an. Die Größe wird über die `width`- und `height`-Attribute festgelegt (Standard ist 300x150 Pixel).
```html
<canvas id="myCanvas" width="400" height="300"></canvas>
```
### Einfache Verwendung von `<canvas>` mit JavaScript
Mit JavaScript und der `getContext("2d")`-Methode kannst du auf die Zeichenfläche zugreifen und einfache Grafiken zeichnen.
**Beispiel**: Ein Rechteck auf der Zeichenfläche zeichnen
```html
<canvas id="myCanvas" width="400" height="300"></canvas>
<script>
  const canvas = document.getElementById("myCanvas");
  const ctx = canvas.getContext("2d");
  ctx.fillStyle = "blue";
  ctx.fillRect(50, 50, 200, 100);
</script>
```
**Anwendungsfälle für `<canvas>`**:
- **Diagramme und Datenvisualisierungen**
- **2D- und 3D-Spiele**
- **Animationen und interaktive Grafiken**
## 2. Inline-SVG (Scalable Vector Graphics)
SVG ist ein XML-basiertes Grafikformat für Vektorgrafiken, das sich besonders für Logos, Icons, Diagramme und interaktive Grafiken eignet. SVG-Grafiken sind skalierbar, ohne an Qualität zu verlieren, was sie für responsive Webseiten ideal macht.
### Einfache Inline-SVG-Grafik
SVG kann direkt in HTML eingebettet werden und wird dabei als Vektorgrafik dargestellt.
**Beispiel**: Ein einfaches SVG-Kreuz
```html
<svg width="100" height="100">
  <circle cx="50" cy="50" r="40" fill="blue" />
</svg>
```
### Vorteile von SVG
- **Skalierbar**: SVGs verlieren keine Qualität, wenn sie vergrößert oder verkleinert werden.
- **Animierbar**: SVG-Elemente lassen sich mit CSS und JavaScript animieren.
- **Interaktiv**: SVGs können auf Benutzereingaben reagieren, was sie ideal für interaktive Grafiken und Animationen macht.
### Anwendungsfälle für SVG
- **Icons und Logos**: SVGs sind ideal für Logos und Icons auf Webseiten.
- **Diagramme und Graphen**: SVGs eignen sich hervorragend für Vektorgrafiken wie Diagramme und Infografiken.
## 3. Audio- und Video-Einbettung
HTML5 führte die `<audio>`- und `<video>`-Elemente ein, die die Integration von Multimedia-Inhalten ohne externe Plugins (z.B. Flash) ermöglichen. Diese Elemente verfügen über eingebaute Steuerungen und können direkt mit HTML5 und JavaScript interagieren.
### Einfache Video-Einbindung
```html
<video controls width="320" height="240">
  <source src="video.mp4" type="video/mp4">
  Dein Browser unterstützt das Video-Tag nicht.
</video>
```
### Einfache Audio-Einbindung
```html
<audio controls>
  <source src="audio.mp3" type="audio/mpeg">
  Dein Browser unterstützt das Audio-Tag nicht.
</audio>
```
### Vorteile
- **Einfaches Einbinden**: Erlaubt das Einfügen von Multimedia ohne Plugins.
- **Browser-Kompatibilität**: Die meisten modernen Browser unterstützen diese Formate.
- **Responsive Steuerungen**: Integrierte Bedienelemente für Play, Pause, Lautstärke und Vollbild.
## 4. Geolocation API

Die Geolocation API ermöglicht es, den Standort des Benutzers mit dessen Zustimmung abzurufen und bietet eine wertvolle Funktionalität für standortbasierte Dienste. Diese API funktioniert nur in Verbindung mit JavaScript.
### Beispiel für Geolocation
```html
<button onclick="getLocation()">Standort abrufen</button>
<p id="location"></p>
<script>
  function getLocation() {
    if (navigator.geolocation) {
      navigator.geolocation.getCurrentPosition(showPosition);
	} else { 
      document.getElementById("location").innerHTML 
      = "Geolocation wird nicht unterstützt.";
    }
  }
  function showPosition(position) {
    document.getElementById("location").innerHTML =
      "Breitengrad: " + position.coords.latitude +
      "<br>Längengrad: " + position.coords.longitude;
  }
</script>
```
**Anwendungsfälle**:
- **Kartenanwendungen**
- **Standortbasierte Services** (z.B. lokale Wetterdaten, Standortinformationen)
## 5. Web Storage (Local Storage und Session Storage)
Mit HTML5 wurde die Möglichkeit eingeführt, Daten direkt im Browser des Benutzers zu speichern, was mit `localStorage` und `sessionStorage` umgesetzt wird. Diese Methode ist sicherer und effizienter als Cookies und wird häufig für Benutzereinstellungen oder Zwischenspeicherungen verwendet.
### Unterschied zwischen Local und Session Storage
- **`localStorage`**: Speichert Daten ohne Ablaufdatum. Die Daten bleiben auch nach dem Schließen des Browsers erhalten.
- **`sessionStorage`**: Speichert Daten nur für die aktuelle Sitzung und löscht sie beim Schließen des Tabs.
### Beispiel: Speichern von Daten in `localStorage`
```html
<button onclick="saveData()">Daten speichern</button>
<button onclick="getData()">Daten abrufen</button>
<p id="output"></p>

<script>
function saveData() {
  localStorage.setItem("name", "Max Mustermann");
}
function getData() {
  const name = localStorage.getItem("name");           
  document.getElementById("output").innerHTML 
    = name ? name : "Keine Daten vorhanden";
}
</script>
```
## 6. Formularelemente und -validierung
HTML5 führt erweiterte Formularelemente und eingebaute Validierungsmöglichkeiten ein, die das Erstellen und Überprüfen von Formularen erheblich erleichtern.
### Neue HTML5-Formularelemente
- **`<input type="date">`**: Ermöglicht die Auswahl eines Datums.
- **`<input type="email">`**: Überprüft automatisch das E-Mail-Format.
- **`<input type="number">`**: Lässt nur numerische Eingaben zu.
- **`<input type="range">`**: Erzeugt einen Schieberegler zur Auswahl eines Wertes.
### Beispiel für ein Formular mit HTML5-Validierung
```html
<form>
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" required>

  <label for="email">E-Mail:</label>
  <input type="email" id="email" name="email" required>
  
  <label for="birthdate">Geburtsdatum:</label>
  <input type="date" id="birthdate" name="birthdate">
  
  <button type="submit">Absenden</button>
</form>
```
## 7. `<datalist>` für Auto-Vervollständigung
Das `<datalist>`-Element ermöglicht eine Auto-Vervollständigung in Eingabefeldern. Es erstellt eine Liste von Vorschlägen für den Benutzer, basierend auf den zuvor definierten Optionen.
### Beispiel für `<datalist>`
```html
<label for="city">Stadt:</label>
<input list="cities" id="city" name="city">
<datalist id="cities">
  <option value="Berlin">
  <option value="Hamburg">
  <option value="München">
</datalist>
```
## Zusammenfassung der modernen HTML5-Features
HTML5 bietet eine Vielzahl neuer Funktionen, die Webseiten interaktiver, benutzerfreundlicher und visueller machen:
- **Grafiken und Animationen**: `<canvas>` und SVGs bieten leistungsstarke Tools für dynamische Grafiken und interaktive Animationen.
- **Multimedia**: Mit `<audio>` und `<video>` wird das Einfügen von Medieninhalten einfach und nativ.
- **Geolocation und Web Storage**: Standortdienste und Local Storage verbessern die Benutzererfahrung durch personalisierte und standortbezogene Inhalte.
- **Erweiterte Formularelemente**: HTML5-Formulare erleichtern die Benutzerinteraktion und Datenvalidierung.
Diese HTML5-Features machen Webseiten flexibler und ansprechender und bieten gleichzeitig eine solide Grundlage für moderne Webanwendungen.