Dieses Cheat Sheet bietet eine kompakte Übersicht über die wichtigsten Konzepte und Syntaxelemente in JavaScript. Nutze es als schnelle Referenz für deine tägliche Arbeit mit JavaScript.

### 1. Grundlegende Syntax

#### Variablendeklaration
```javascript
let variable = "wert";    // veränderbar 
const KONSTANTE = 10;     // unveränderlich 
var globalVariable = 5;   // nicht empfohlen, globaler Scope
```

#### Datentypen
```javascript
let str = "Hello";       // string 
let num = 123;           // number 
let bool = true;         // boolean 
let obj = {name: "Max"}; // object 
let arr = [1, 2, 3];     // array (Sonderform des Objects) 
let und = undefined;     // undefined 
let nll = null;          // null
```

### 2. Operatoren

#### Arithmetische Operatoren
```javascript
let sum = 5 + 10;     // Addition 
let diff = 10 - 5;    // Subtraktion 
let product = 5 * 2;  // Multiplikation 
let quotient = 10 / 2; // Division 
let mod = 10 % 3;     // Modulus
```

#### Vergleichsoperatoren
```javascript
a == b    // Gleichheit (Typumwandlung möglich) 
a === b   // Strikte Gleichheit (kein Typumwandlung) 
a != b    // Ungleichheit 
a !== b   // Strikte Ungleichheit 
a > b     // Größer 
a < b     // Kleiner 
a >= b    // Größer oder gleich 
a <= b    // Kleiner oder gleich
```

### 3. Kontrollstrukturen

#### Bedingungsanweisungen
```javascript
if (condition) { 
  // code 
} else if (anotherCondition) {
  // code 
} else {
  // code 
}
switch(value) {  
  case 1: 
    // code
    break;
  case 2:
    // code
    break;
  default:
    // code
}
```

#### Schleifen
```javascript
for (let i = 0; i < 5; i++) {
  console.log(i);
}
let i = 0; while (i < 5) {
  console.log(i);
  i++;
}
do {
  console.log(i);
  i++;
} while (i < 5);
```

### 4. Funktionen

#### Funktionserstellung
```javascript
function greet(name) {
  return `Hello, ${name}`;
}
const add = (a, b) => a + b; // Arrow Function
```

### 5. Arrays und Objekte

#### Array-Methoden
```javascript
let arr = [1, 2, 3]; 
arr.push(4);         // Hinzufügen am Ende 
arr.pop();           // Entfernen vom Ende 
arr.shift();         // Entfernen vom Anfang 
arr.unshift(0);      // Hinzufügen am Anfang 
arr.map(x => x * 2); // Map-Funktion 
arr.filter(x => x > 1); // Filter-Funktion 
arr.reduce((sum, x) => sum + x, 0); // Reduzieren auf einen Wert
```

#### Objekteigenschaften und -Methoden
```javascript
let user = {
  name: "Max",
  age: 30
};
console.log(user.name);   // Zugriff auf Eigenschaften
user.location = "Berlin"; // Hinzufügen neuer Eigenschaften 
delete user.age;          // Entfernen einer Eigenschaft
```

### 6. String-Methoden
```javascript
let str = "JavaScript";
str.length;               // Länge 
str.toUpperCase();        // In Großbuchstaben umwandeln 
str.toLowerCase();        // In Kleinbuchstaben umwandeln 
str.includes("Script");   // Enthält "Script"? 
str.slice(0, 4);          // Schneidet "Java" aus
```

### 7. DOM-Manipulation

#### Zugriff auf HTML-Elemente
```javascript
document.getElementById("id"); document.querySelector(".class"); document.querySelectorAll("div");
```

#### Ändern von Inhalten und Stilen
```javascript
let element = document.querySelector("#id");
element.textContent = "Neuer Text";
element.style.color = "blue";
```

#### Event-Handling
```javascript
element.addEventListener("click", function() {
  console.log("Element geklickt!");
});
```

### 8. Asynchrone Programmierung

#### Promises
```javascript
let promise = new Promise((resolve, reject) => {
  // async code 
});
promise.then(result => {     
// handle result 
}).catch(error => {
  // handle error
});
```

#### Async/Await
```javascript
async function fetchData() {
  try {
    let response = await fetch("url");
    let data = await response.json();
     console.log(data);
  } catch (error) {
    console.error(error);
  }
}
```

---

Dieses Cheat Sheet dient als praktische Referenz für häufig genutzte JavaScript-Syntax und -Konzepte. Es bietet dir einen schnellen Überblick über die wichtigsten Themen und hilft dir dabei, JavaScript-Projekte effizienter zu entwickeln.