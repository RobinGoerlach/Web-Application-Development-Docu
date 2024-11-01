**Kontrollstrukturen** in JavaScript ermöglichen es, den Programmfluss zu steuern und Entscheidungen zu treffen. Sie sind entscheidend, um Bedingungen zu prüfen und den Code in Abhängigkeit von bestimmten Bedingungen oder Wiederholungen auszuführen. Die grundlegenden Kontrollstrukturen umfassen bedingte Anweisungen und Schleifen.

## 1. Bedingte Anweisungen

Bedingte Anweisungen erlauben es, Code nur dann auszuführen, wenn eine bestimmte Bedingung erfüllt ist.

### if-Anweisung

Die **if-Anweisung** führt den Codeblock nur dann aus, wenn die Bedingung `true` ist.

**Syntax:**

```javascript
if (Bedingung) {   
  // Code, der ausgeführt wird, wenn die Bedingung wahr ist 
}
```

**Beispiel:**

```javascript
let age = 20;  
if (age >= 18) {
  console.log("Du bist volljährig."); 
}
```

### if...else-Anweisung

Die **if...else-Anweisung** bietet eine Alternative für den Fall, dass die Bedingung `false` ist.

**Syntax:**

```javascript
if (Bedingung) {   
  // Code, der ausgeführt wird, wenn die Bedingung wahr ist 
} else {
  // Code, der ausgeführt wird, wenn die Bedingung falsch ist 
}
```

**Beispiel:**

```javascript
let age = 16;  
if (age >= 18) {   
  console.log("Du bist volljährig."); 
} else {
  console.log("Du bist minderjährig."); 
}
```

### if...else if...else-Anweisung

Mit der **if...else if...else-Anweisung** lassen sich mehrere Bedingungen nacheinander prüfen. Der erste `true`-Wert wird ausgeführt, alle anderen Bedingungen werden ignoriert.

**Syntax:**

```javascript
if (Bedingung1) {   
  // Code für Bedingung1 
} else if (Bedingung2) {   
  // Code für Bedingung2 
} else {   
  // Code, wenn keine Bedingung wahr ist 
}
```

**Beispiel:**

```javascript
let score = 85;  
if (score >= 90) {
  console.log("Hervorragend!"); 
} else if (score >= 75) {
  console.log("Gut gemacht!"); 
} else {
  console.log("Du kannst noch besser werden."); 
}
```

### switch-Anweisung

Die **switch-Anweisung** prüft eine Variable auf verschiedene Werte und führt den entsprechenden Codeblock aus. Sie eignet sich gut, wenn viele feste Werte geprüft werden müssen.

**Syntax:**

```javascript
switch (Ausdruck) {
  case Wert1:
    // Code für Wert1
    break;
  case Wert2:
    // Code für Wert2
    break;
  default:
    // Code, wenn keiner der Fälle zutrifft 
}
```

**Beispiel:**

```javascript
let day = "Montag";  
switch (day) {   
  case "Montag":
    console.log("Wochenstart!");
    break;
  case "Freitag":
    console.log("Fast Wochenende!");
    break;   
  default:
    console.log("Ein gewöhnlicher Tag."); 
}
```

## 2. Schleifen

Schleifen ermöglichen das wiederholte Ausführen von Code, solange eine Bedingung `true` ist.

### for-Schleife

Die **for-Schleife** ist eine Zählschleife und eignet sich gut, um Code eine bestimmte Anzahl von Malen auszuführen.

**Syntax:**

```javascript
for (Initialisierung; Bedingung; Inkrement/Update) {
  // Code, der wiederholt ausgeführt wird 
}
```

**Beispiel:**

```javascript
for (let i = 0; i < 5; i++) {
  console.log("Durchlauf Nummer " + i);
}
```

### while-Schleife

Die **while-Schleife** wiederholt den Code so lange, wie die Bedingung `true` ist.

**Syntax:**

```javascript
while (Bedingung) {
  // Code, der wiederholt ausgeführt wird 
}
```

**Beispiel:**

```javascript
let count = 0;
while (count < 3) {
  console.log("Count ist " + count);
  count++; 
}
```

### do...while-Schleife

Die **do...while-Schleife** ähnelt der `while`-Schleife, führt jedoch den Code mindestens einmal aus, bevor die Bedingung geprüft wird.

**Syntax:**

```javascript
do {
  // Code, der mindestens einmal ausgeführt wird 
} while (Bedingung);
```

**Beispiel:**

```javascript
let count = 0;
do {
  console.log("Count ist " + count);
  count++;
} while (count < 3);
```

## 3. break und continue

Diese Schlüsselwörter helfen, den Ablauf von Schleifen gezielt zu steuern.

- **break**: Beendet die Schleife vollständig.
- **continue**: Bricht den aktuellen Durchlauf ab und springt zur nächsten Iteration.

**Beispiel mit break:**

```javascript
for (let i = 0; i < 5; i++) {
  if (i === 3) {
    break; // Schleife endet bei i = 3   
  }
  console.log(i); 
}
```

**Beispiel mit continue:**

```javascript
for (let i = 0; i < 5; i++) {
  if (i === 2) {
    continue; // Überspringt den Durchlauf bei i = 2
  }
  console.log(i); 
}
```

## Zusammenfassung

Kontrollstrukturen sind zentrale Werkzeuge in JavaScript und helfen dabei, den Ablauf eines Programms dynamisch und anpassungsfähig zu gestalten. Die Kombination aus bedingten Anweisungen und Schleifen ermöglicht komplexe Entscheidungslogik und Wiederholungen im Code, die jede JavaScript-Anwendung flexibler machen.