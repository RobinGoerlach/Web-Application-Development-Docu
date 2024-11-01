**Scope** bezeichnet in JavaScript den Bereich im Code, in dem eine Variable sichtbar und zugänglich ist. Ein gutes Verständnis des Scopes hilft, unerwartete Fehler zu vermeiden und sauberen, gut strukturierten Code zu schreiben. JavaScript unterstützt mehrere Scoping-Mechanismen, darunter den globalen Scope, den Funktions-Scope und den Block-Scope.

## 1. Globaler Scope

Der **globale Scope** umfasst Variablen, die außerhalb von Funktionen oder Blöcken deklariert werden. Sie sind im gesamten Programm verfügbar und können von jedem Codeabschnitt verwendet werden. Allerdings können globale Variablen schnell zu Konflikten führen, wenn verschiedene Teile des Codes auf dieselben Namen zugreifen oder diese ändern.

**Beispiel:**

```javascript
let globalVar = "Ich bin global";
function printGlobalVar() {
  console.log(globalVar); 
}

printGlobalVar(); // Output: Ich bin global 
console.log(globalVar); // Output: Ich bin global
```

In diesem Beispiel ist `globalVar` im globalen Scope deklariert und daher überall zugänglich, auch innerhalb von `printGlobalVar`.

## 2. Funktions-Scope

JavaScript unterstützt **Funktions-Scope**, was bedeutet, dass Variablen, die innerhalb einer Funktion deklariert werden, nur innerhalb dieser Funktion zugänglich sind. Sobald die Funktion beendet ist, werden ihre Variablen aus dem Speicher entfernt.

### Beispiel für Funktions-Scope

```javascript
function myFunction() {
  let localVar = "Ich bin lokal";
  console.log(localVar); // Output: Ich bin lokal
}

myFunction(); 
// console.log(localVar); // Error: localVar is not defined
```

In diesem Beispiel ist `localVar` nur innerhalb von `myFunction` verfügbar. Außerhalb der Funktion ist `localVar` nicht definiert, was zu einem Fehler führt.

## 3. Block-Scope

Mit der Einführung von `let` und `const` in ES6 unterstützt JavaScript jetzt **Block-Scope**. Ein Block wird durch `{}` definiert, und Variablen, die innerhalb eines Blocks mit `let` oder `const` deklariert werden, sind nur innerhalb dieses Blocks sichtbar.

### Beispiel für Block-Scope

```javascript
if (true) {
  let blockScopedVar = "Ich bin im Block";
  console.log(blockScopedVar); // Output: Ich bin im Block
}

// console.log(blockScopedVar); // Error: blockScopedVar is not defined
```

Hier ist `blockScopedVar` nur im Block des `if`-Statements sichtbar und außerhalb des Blocks nicht zugänglich.

### Unterschied zwischen `var`, `let` und `const`

- **`var`**: Wird im Funktions-Scope deklariert, nicht im Block-Scope. Eine mit `var` deklarierte Variable ist sichtbar im gesamten Funktionsblock, in dem sie definiert ist, oder im globalen Scope, wenn sie außerhalb von Funktionen deklariert wird.
- **`let` und `const`**: Werden im Block-Scope deklariert und sind nur innerhalb des Blocks sichtbar, in dem sie deklariert wurden.

**Beispiel:**

```javascript
function testScope() {
  if (true) {
    var functionScopedVar = "Ich bin im Funktions-Scope";
    let blockScopedLet = "Ich bin im Block-Scope";
    const blockScopedConst = "Ich bin auch im Block-Scope";
  }
  console.log(functionScopedVar); // Output: Ich bin im Funktions-Scope   
  // console.log(blockScopedLet); // Error: blockScopedLet is not defined
  // console.log(blockScopedConst); // Error: blockScopedConst is not defined
}

testScope();
```

In diesem Beispiel ist `functionScopedVar` außerhalb des `if`-Blocks sichtbar, weil `var` im Funktions-Scope deklariert wird. `blockScopedLet` und `blockScopedConst` hingegen sind nur innerhalb des `if`-Blocks zugänglich.

## 4. Lexikalischer Scope

JavaScript verwendet **lexikalischen Scope**, was bedeutet, dass der Scope zur Kompilierzeit festgelegt wird, also zu dem Zeitpunkt, an dem der Code geschrieben wird, und nicht zur Laufzeit. Funktionen „merken“ sich den Scope, in dem sie definiert wurden, und behalten Zugriff auf Variablen aus diesem Scope, auch wenn sie in einem anderen Kontext aufgerufen werden.

### Beispiel für lexikalischen Scope

```javascript
function outerFunction() {
  let outerVar = "Ich komme aus outerFunction";
  function innerFunction() {
    console.log(outerVar); // Zugriff auf outerVar durch lexikalischen Scope
  }
  innerFunction(); 
}

outerFunction(); // Output: Ich komme aus outerFunction
```

In diesem Beispiel hat `innerFunction` Zugriff auf `outerVar`, da sie sich im lexikalischen Scope von `outerFunction` befindet. Das bedeutet, dass `innerFunction` den Wert von `outerVar` auch dann „kennt“, wenn sie in einem anderen Kontext aufgerufen wird.

## 5. Hoisting

In JavaScript werden Variablendeklarationen mit `var` im Hintergrund „an den Anfang“ ihres Scopes verschoben, ein Prozess, der als **Hoisting** bezeichnet wird. Variablen, die mit `let` und `const` deklariert werden, sind zwar ebenfalls „gehoisted“, aber können nicht vor ihrer Deklaration verwendet werden. Dies führt zu einem **ReferenceError**.

### Beispiel für Hoisting

```javascript
console.log(hoistedVar); // Output: undefined 
var hoistedVar = "Ich wurde gehoisted";  

console.log(notHoistedLet); // Error: Cannot access 'notHoistedLet' before initialization 
let notHoistedLet = "Ich wurde nicht gehoisted";
```

Hier wird `hoistedVar` mit `var` deklariert und durch Hoisting an den Anfang verschoben, wodurch der Code `undefined` zurückgibt. `notHoistedLet` führt zu einem Fehler, da `let` vor der Deklaration nicht zugänglich ist.

## Zusammenfassung

In JavaScript gibt es verschiedene Scoping-Mechanismen, die den Gültigkeitsbereich von Variablen steuern:

- **Globaler Scope**: Variablen sind im gesamten Skript sichtbar.
- **Funktions-Scope**: Variablen sind nur innerhalb der Funktion sichtbar, in der sie deklariert wurden.
- **Block-Scope**: Variablen, die mit `let` und `const` deklariert werden, sind nur innerhalb des Blocks sichtbar, in dem sie definiert wurden.
- **Lexikalischer Scope**: Variablen behalten den Scope, in dem sie deklariert wurden, unabhängig davon, wo die Funktion später aufgerufen wird.
- **Hoisting**: Variablen, die mit `var` deklariert werden, werden an den Anfang ihres Scopes verschoben, während `let` und `const`-Variablen nur nach ihrer Deklaration zugänglich sind.

Ein gutes Verständnis des Scopes in JavaScript hilft dabei, den Code sicher und effizient zu gestalten und häufige Fehler zu vermeiden.