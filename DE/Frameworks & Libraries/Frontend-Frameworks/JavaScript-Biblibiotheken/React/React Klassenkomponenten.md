Vor der Einführung von Hooks waren **Klassenkomponenten** der Standardansatz für die Erstellung von Komponenten in React. Obwohl sie inzwischen von funktionalen Komponenten abgelöst wurden, sind Klassenkomponenten immer noch relevant, insbesondere in bestehenden Codebasen. In diesem Artikel betrachten wir die Grundlagen, Eigenschaften und Best Practices für Klassenkomponenten.

---

## **Was sind Klassenkomponenten?**

Klassenkomponenten sind ES6-Klassen, die von `React.Component` erben. Sie bieten Zugriff auf State und Lifecycle-Methoden, was sie für die Entwicklung komplexer Komponenten geeignet macht.

### **Beispiel:**

```
import React, { Component } from 'react';

class Greeting extends Component {
  render() {
    return <h1>Hello, {this.props.name}!</h1>;
  }
}

export default Greeting;
```

In diesem Beispiel:

- `Greeting` ist eine Klasse, die von `React.Component` erbt.
    
- Die Methode `render()` gibt JSX zurück, das die Komponente darstellt.
    

---

## **State in Klassenkomponenten**

Klassenkomponenten verwalten ihren internen Zustand mit einem `state`-Objekt. Änderungen am State werden über die Methode `setState` vorgenommen.

### **Beispiel:**

```
class Counter extends Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
  }

  increment = () => {
    this.setState({ count: this.state.count + 1 });
  };

  render() {
    return (
      <div>
        <p>Count: {this.state.count}</p>
        <button onClick={this.increment}>Increase</button>
      </div>
    );
  }
}

export default Counter;
```

Hier:

- Der Zustand `count` wird in `state` initialisiert.
    
- `setState` aktualisiert den Zustand und löst ein erneutes Rendern der Komponente aus.
    

---

## **Lifecycle-Methoden in Klassenkomponenten**

Klassenkomponenten bieten spezielle Methoden, um auf verschiedene Phasen des Komponentenlebenszyklus zu reagieren.

### **Wichtige Lifecycle-Methoden:**

1. **Mounting (Komponente wird hinzugefügt):**
    
    - `constructor()`
        
    - `componentDidMount()`
        
2. **Updating (Komponente wird aktualisiert):**
    
    - `componentDidUpdate(prevProps, prevState)`
        
3. **Unmounting (Komponente wird entfernt):**
    
    - `componentWillUnmount()`
        

### **Beispiel:**

```
class Timer extends Component {
  constructor(props) {
    super(props);
    this.state = { seconds: 0 };
  }

  componentDidMount() {
    this.interval = setInterval(() => {
      this.setState({ seconds: this.state.seconds + 1 });
    }, 1000);
  }

  componentWillUnmount() {
    clearInterval(this.interval);
  }

  render() {
    return <p>Time elapsed: {this.state.seconds} seconds</p>;
  }
}

export default Timer;
```

Hier:

- `componentDidMount` startet einen Timer.
    
- `componentWillUnmount` räumt den Timer auf, wenn die Komponente entfernt wird.
    

---

## **Props in Klassenkomponenten**

Wie funktionale Komponenten akzeptieren Klassenkomponenten Props, die sie über `this.props` nutzen können.

### **Beispiel:**

```
class Welcome extends Component {
  render() {
    return <h1>Welcome, {this.props.name}!</h1>;
  }
}

export default Welcome;
```

Hier:

- Die Props werden mit `this.props.name` referenziert.
    

---

## **Vergleich: Klassenkomponenten vs. Funktionale Komponenten**

|**Merkmal**|**Klassenkomponenten**|**Funktionale Komponenten**|
|---|---|---|
|**State-Verwaltung**|`this.state`, `setState`|`useState`, `useReducer`|
|**Lifecycle-Methoden**|`componentDidMount`, `componentDidUpdate`|`useEffect`|
|**Code-Komplexität**|Mehr Boilerplate|Weniger Boilerplate|
|**Performance**|Etwas langsamer|Performanter|

---

## **Wann sollte man Klassenkomponenten verwenden?**

- **Bestehende Codebasen:**
    
    - Wenn Sie an Projekten arbeiten, die vor der Einführung von Hooks erstellt wurden.
        
- **Spezifische Frameworks oder Tools:**
    
    - Einige ältere Bibliotheken oder Frameworks unterstützen ausschließlich Klassenkomponenten.
        
- **Schulung und Verständnis:**
    
    - Das Verständnis von Klassenkomponenten hilft, ältere Codebasen zu lesen und zu warten.
        

---

## **Best Practices für Klassenkomponenten**

1. **State minimal halten:**
    
    - Verwenden Sie den State nur für Daten, die sich ändern können.
        
2. **Lifecycle-Methoden effizient nutzen:**
    
    - Vermeiden Sie komplexe Logik in `componentDidMount` oder `componentDidUpdate`. Delegieren Sie diese Logik an Hilfsfunktionen.
        
3. **Props und State klar trennen:**
    
    - Props sollten unveränderlich sein, während der State sich dynamisch ändern kann.
        
4. **Eindeutige Benennung:**
    
    - Verwenden Sie beschreibende Namen für Methoden und State-Variablen.
        

---

## **Fazit**

Klassenkomponenten waren lange Zeit das Rückgrat der React-Entwicklung. Obwohl funktionale Komponenten mit Hooks sie inzwischen weitgehend ersetzt haben, sind sie in vielen bestehenden Codebasen weiterhin relevant. Ein solides Verständnis von Klassenkomponenten ist daher unerlässlich, um ältere Projekte zu warten oder zu modernisieren. Durch die Anwendung der vorgestellten Best Practices bleiben Klassenkomponenten übersichtlich und effektiv.