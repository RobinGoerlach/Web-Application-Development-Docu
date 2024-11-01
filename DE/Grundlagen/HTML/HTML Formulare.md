## # HTML-Formulare: Einführung in Formularelemente (`form`, `input`, `textarea`, `button`, `select`, etc.)

Formulare sind essenziell für Interaktionen auf Webseiten. Sie ermöglichen Benutzern, Informationen einzugeben und zu senden – sei es zur Registrierung, zum Ausfüllen von Kontaktformularen oder für Bestellungen. HTML bietet verschiedene Formularelemente, um Daten strukturiert einzugeben und zu sammeln.
## Das `<form>`-Tag
Das `<form>`-Tag ist der Container für das gesamte Formular und bildet die Basis für die Dateneingabe. Es enthält alle Formularelemente und steuert die Übermittlung der Daten.
### Grundstruktur eines Formulars

```html
<form action="/submit" method="post">
  <!-- Formularelemente -->
</form>
```
### Wichtige Attribute des `<form>`-Tags
- **`action`**: Die URL, an die die Formulardaten gesendet werden sollen.
- **`method`**: Gibt die HTTP-Methode an, mit der die Daten gesendet werden (`GET` oder `POST`).
    - `GET`: Überträgt die Daten als URL-Parameter; gut für Suchanfragen oder nicht vertrauliche Daten.
    - `POST`: Überträgt die Daten im HTTP-Body und eignet sich für vertrauliche oder umfangreiche Daten.
## Formularelemente im Überblick
### 1. Das `<input>`-Tag
Das `<input>`-Tag ist das vielseitigste Formularelement und kann verschiedene Datentypen annehmen, je nachdem, welches `type`-Attribut gesetzt ist.
#### Textfeld (`type="text"`)
Ein einfaches Textfeld, in das der Benutzer Text eingeben kann.
```html
<label for="name">Name:</label> <input type="text" id="name" name="name">
```
#### E-Mail-Feld (`type="email"`)
Ermöglicht die Eingabe einer E-Mail-Adresse und überprüft automatisch die Formatierung.
```html
<label for="email">E-Mail:</label>
<input type="email" id="email" name="email">
```
#### Passwortfeld (`type="password"`)
Zeigt die eingegebenen Zeichen als Punkte oder Sterne an, um die Privatsphäre zu schützen.
```html
<label for="password">Passwort:</label>
<input type="password" id="password" name="password">
```
#### Kontrollkästchen (`type="checkbox"`)
Erlaubt die Auswahl mehrerer Optionen unabhängig voneinander.
```html
<label><input type="checkbox" name="option1" value="1"> Option 1</label> 
<label><input type="checkbox" name="option2" value="2"> Option 2</label>
```
#### Optionsfeld (`type="radio"`)
Erlaubt die Auswahl nur einer Option aus einer Gruppe. Alle Optionsfelder in einer Gruppe sollten denselben `name`-Wert haben.
```html
<label><input type="radio" name="gender" value="male"> Männlich</label>
<label><input type="radio" name="gender" value="female"> Weiblich</label>
```
#### Zahlenfeld (`type="number"`)
Erlaubt die Eingabe einer Zahl und enthält zusätzlich Steuerungselemente für die Erhöhung oder Verringerung der Zahl.
```html
<label for="age">Alter:</label>
<input type="number" id="age" name="age" min="1" max="100">
```
#### Datumsfeld (`type="date"`)
Erlaubt die Eingabe eines Datums und zeigt in unterstützenden Browsern einen Kalender an.
```html
<label for="date">Datum:</label>
<input type="date" id="date" name="date">
```
### 2. Das `<textarea>`-Tag
Das `<textarea>`-Tag wird für mehrzeilige Textfelder verwendet, die längerem Text oder Kommentaren dienen.
```html
<label for="message">Nachricht:</label>
<textarea id="message" name="message" rows="4" cols="50"></textarea>
```
- **`rows`** und **`cols`**: Definieren die Anzahl der Zeilen und Spalten und damit die Größe des Textbereichs.
### 3. Das `<button>`-Tag
Das `<button>`-Tag erstellt eine Schaltfläche, die eine Aktion im Formular auslöst. Es kann auch mit dem `type`-Attribut spezifiziert werden.
- **`type="submit"`**: Sendet die Formulardaten an die im `<form>`-Tag definierte `action`.
- **`type="reset"`**: Setzt das Formular auf die Standardwerte zurück.
```html
<button type="submit">Absenden</button> <button type="reset">Zurücksetzen</button>
```
### 4. Das `<select>`-Tag
Das `<select>`-Tag erstellt ein Dropdown-Menü mit mehreren Auswahlmöglichkeiten. Jede Option wird durch ein `<option>`-Tag definiert.
```html
<label for="city">Stadt:</label>
<select id="city" name="city">
  <option value="berlin">Berlin</option>
  <option value="hamburg">Hamburg</option>
  <option value="muenchen">München</option>
</select>
```
- **`multiple`**: Ermöglicht die Auswahl mehrerer Optionen, indem `multiple` zum `<select>`-Tag hinzugefügt wird.
## Einfache Formular-Beispiel
Hier ein Beispiel für ein Kontaktformular, das verschiedene Formularelemente verwendet:
```html
<form action="/submit-form" method="post">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" required>
  
  <label for="email">E-Mail:</label>
  <input type="email" id="email" name="email" required>
  
  <label for="message">Nachricht:</label>
  <textarea id="message" name="message" rows="4" cols="50"></textarea>
  
  <label for="city">Stadt:</label>
  <select id="city" name="city">
    <option value="berlin">Berlin</option>
    <option value="hamburg">Hamburg</option>
    <option value="muenchen">München</option>
  </select>
  <button type="submit">Absenden</button>
</form>
```
## Zusätzliche nützliche Attribute für Formularelemente
- **`required`**: Macht das Feld erforderlich und verhindert das Absenden des Formulars, solange das Feld leer ist.
```html
<input type="text" name="username" required>
```
- **`placeholder`**: Zeigt einen Platzhaltertext in Eingabefeldern an, der verschwindet, wenn der Benutzer beginnt, etwas einzugeben.
```html
<input type="text" name="username" placeholder="Gib deinen Benutzernamen ein">
```
- **`disabled`**: Macht das Feld nicht bearbeitbar und grau dargestellt.
```html
<input type="text" name="username" disabled>
```
- **`maxlength`** und **`minlength`**: Legt die maximale bzw. minimale Zeichenanzahl für Eingabefelder fest.
```html
<input type="text" name="username" maxlength="15" minlength="3">
```
## Best Practices für Formulare
1. **Nutzerführung**: Verwende aussagekräftige `label`-Tags, um Felder klar zu beschreiben und die Zugänglichkeit zu verbessern.
2. **Barrierefreiheit**: Mit `aria`-Attributen oder `label`-Elementen werden Formulare auch für Screenreader-Nutzer verständlich.
3. **Validierung**: Nutze HTML-Validierung (z.B. `required`, `type="email"`) und ergänze sie, wenn nötig, durch serverseitige Validierung.
4. **Sicherheitsaspekte beachten**: Verwende `method="POST"` für Formulare, die sensible Daten enthalten, und implementiere Maßnahmen gegen Cross-Site-Scripting (XSS).

---

Dieser Artikel bietet eine Einführung in die Erstellung und Nutzung von Formularen in HTML. Mit diesen Grundlagen kannst du benutzerfreundliche und funktionale Formulare erstellen, die eine effiziente und sichere Dateneingabe ermöglichen.