# **Daten gemeinsam nutzen in React**

Der Hook **useContext** ist ein zentrales Werkzeug in React, das es ermöglicht, Daten oder Zustände zwischen Komponenten zu teilen, ohne explizit Props durch jede Komponente in der Hierarchie weitergeben zu müssen. Er vereinfacht die Verwaltung globaler Daten und ist eine bevorzugte Lösung, um das sogenannte "Props-Drilling" zu vermeiden.

---

## **Was ist useContext?**
`useContext` ist ein React-Hook, der den Zugriff auf einen gemeinsamen Kontextwert ermöglicht. Ein Kontext wird mit der `createContext`-Methode erstellt und stellt Daten für alle Komponenten zur Verfügung, die in seinen Bereich eingebettet sind.
### **Syntax:**
```
const value = useContext(MyContext);
```
- **`MyContext`** ist ein mit `createContext` erstellter Kontext.    
- **`value`** ist der aktuelle Wert des Kontexts, der in der Komponente verwendet werden kann.
    
---
## **Wie funktioniert useContext?**
1. **Erstellen eines Kontexts:**    
    - Mit `createContext` wird ein neuer Kontext erstellt.        
2. **Bereitstellen von Daten:**    
    - Der `Provider`-Wrapper wird verwendet, um den Wert des Kontexts an die darunter liegenden Komponenten weiterzugeben.        
3. **Zugriff auf den Kontextwert:**    
    - Komponenten innerhalb des `Provider`-Bereichs können mit `useContext` auf den Wert zugreifen.     
---
## **Beispiel: Grundlegende Verwendung von useContext**
### **1. Kontext erstellen**
```
import React, { createContext } from 'react';

const ThemeContext = createContext();
export default ThemeContext;
```
### **2. Daten bereitstellen**
```
import React from 'react';
import ThemeContext from './ThemeContext';

function App() {
  return (
    <ThemeContext.Provider value="dark">
      <ThemedComponent />
    </ThemeContext.Provider>
  );
}

export default App;
```
### **3. Kontextwert konsumieren**
```
import React, { useContext } from 'react';
import ThemeContext from './ThemeContext';

function ThemedComponent() {
  const theme = useContext(ThemeContext);

  return <div style={{ backgroundColor: theme === 'dark' ? '#333' : '#FFF' }}>Theme: {theme}</div>;
}

export default ThemedComponent;
```
In diesem Beispiel:
- Der `ThemeContext` wird erstellt und ein Wert (`dark`) bereitgestellt.    
- `ThemedComponent` greift auf den Wert des Kontexts zu und passt das Styling entsprechend an.
    
---
## **Vorteile von useContext**
1. **Vermeidung von Props-Drilling:**    
    - Daten können direkt an tief verschachtelte Komponenten weitergegeben werden, ohne dass alle Zwischenkomponenten involviert sind.        
2. **Einfachheit:**    
    - Weniger Boilerplate-Code im Vergleich zur expliziten Weitergabe von Props.        
3. **Flexibilität:**    
    - `useContext` kann mit beliebigen Daten verwendet werden, einschließlich Objekten, Arrays und Funktionen.
        
---
## **Erweiterte Anwendungsfälle**
### **1. Verwendung mit Objekten**
Kontexte können komplexe Daten wie Objekte enthalten.
#### **Beispiel:**
```
const UserContext = createContext();

function App() {
  const user = { name: "Alice", isAdmin: true };

  return (
    <UserContext.Provider value={user}>
      <UserProfile />
    </UserContext.Provider>
  );
}

function UserProfile() {
  const user = useContext(UserContext);

  return <h1>Welcome, {user.name}!</h1>;
}
```
### **2. Gemeinsame Funktionen im Kontext bereitstellen**
Ein Kontext kann auch Funktionen bereitstellen, um Aktionen global verfügbar zu machen.
#### **Beispiel:**
```
const AuthContext = createContext();

function App() {
  const login = () => console.log("User logged in");

  return (
    <AuthContext.Provider value={{ login }}>
      <LoginButton />
    </AuthContext.Provider>
  );
}

function LoginButton() {
  const { login } = useContext(AuthContext);

  return <button onClick={login}>Login</button>;
}
```
### **3. Kombination mit useReducer**
`useContext` wird häufig mit `useReducer` verwendet, um ein einfaches State-Management zu implementieren.
#### **Beispiel:**
```
const CounterContext = createContext();

function counterReducer(state, action) {
  switch (action.type) {
    case "increment":
      return state + 1;
    case "decrement":
      return state - 1;
    default:
      return state;
  }
}

function App() {
  const [count, dispatch] = useReducer(counterReducer, 0);

  return (
    <CounterContext.Provider value={{ count, dispatch }}>
      <Counter />
    </CounterContext.Provider>
  );
}

function Counter() {
  const { count, dispatch } = useContext(CounterContext);

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => dispatch({ type: "increment" })}>+</button>
      <button onClick={() => dispatch({ type: "decrement" })}>-</button>
    </div>
  );
}
```
---
## **Best Practices für useContext**
1. **Nicht für jede Kleinigkeit verwenden:**    
    - Nutzen Sie `useContext` für globale Daten, die viele Komponenten betreffen, wie Authentifizierung oder Theme.        
2. **Mehrere Kontexte trennen:**    
    - Verwenden Sie separate Kontexte für unterschiedliche Arten von Daten, um den Code übersichtlich zu halten.        
3. **Performance im Auge behalten:**    
    - Änderungen im Kontext führen dazu, dass alle konsumierenden Komponenten neu gerendert werden. Nutzen Sie `React.memo`, wenn nötig.        
4. **Klare Dokumentation:**    
    - Stellen Sie sicher, dass der Zweck des Kontexts und seine Werte klar dokumentiert sind.
        
---
## **Fazit**
`useContext` ist ein leistungsstarker Hook, der es ermöglicht, globale Daten und Funktionen effizient in React-Anwendungen zu teilen. Er reduziert die Notwendigkeit von Props-Drilling und sorgt für eine klarere Code-Struktur. In Kombination mit anderen Hooks wie `useReducer` oder `useEffect` bietet `useContext` eine flexible Grundlage für skalierbare Anwendungen.