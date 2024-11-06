Für schnellen Zugriff auf die wichtigsten CSS-Befehle und -Eigenschaften ist ein Cheat Sheet unerlässlich. Hier findest du praktische Übersichten über häufig verwendete CSS-Elemente, Layout-Eigenschaften und Einheiten. Ideal für die tägliche Arbeit und um immer wiederkehrende CSS-Konzepte im Blick zu behalten!

## 1. CSS-Syntax
```css
selector {
  property: value;
}
```

## 2. Grundlegende CSS-Eigenschaften

| Eigenschaft   | Funktion                    | Beispiel                  |
| ------------- | --------------------------- | ------------------------- |
| `color`       | Textfarbe festlegen         | `color: #333;`            |
| `background`  | Hintergrundfarbe oder -bild | `background: #fafafa;`    |
| `border`      | Rahmen festlegen            | `border: 1px solid #ccc;` |
| `margin`      | Außenabstand eines Elements | `margin: 20px;`           |
| `padding`     | Innenabstand eines Elements | `padding: 10px;`          |
| `font-size`   | Schriftgröße festlegen      | `font-size: 16px;`        |
| `font-weight` | Schriftgewicht (dick/dünn)  | `font-weight: bold;`      |

## 3. Farben und Transparenz

| Farbeinstellung    | Beispiel                          |
| ------------------ | --------------------------------- |
| HEX                | `color: #3498db;`                 |
| RGB                | `color: rgb(52, 152, 219);`       |
| RGBA (Transparenz) | `color: rgba(52, 152, 219, 0.5);` |

## 4. Layout: Box-Modell

| Eigenschaft | Funktion              |
| ----------- | --------------------- |
| `width`     | Breite des Elements   |
| `height`    | Höhe des Elements     |
| `border`    | Rahmen um das Element |
| `margin`    | Außenabstand          |
| `padding`   | Innenabstand          |

## 5. Positionierung

| Positionierungs-Typ | Beschreibung                                       |
| ------------------- | -------------------------------------------------- |
| `static`            | Standardpositionierung ohne Verschiebung           |
| `relative`          | Relativ zur ursprünglichen Position                |
| `absolute`          | Absolut zur nächsthöheren relativen Ebene          |
| `fixed`             | Fest am Bildschirmrand                             |
| `sticky`            | Haftet beim Scrollen bis zu einem bestimmten Punkt |

## 6. Flexbox

| Eigenschaft       | Beschreibung                      |
| ----------------- | --------------------------------- |
| `display: flex;`  | Aktiviert Flexbox für ein Element |
| `justify-content` | Horizontale Ausrichtung           |
| `align-items`     | Vertikale Ausrichtung             |
| `flex-direction`  | Richtung des Flex-Layouts         |
| `flex-wrap`       | Zeilenumbruch erlauben            |

### Beispiel:

```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
}
```

## 7. CSS Grid

| Eigenschaft                | Beschreibung                        |
| -------------------------- | ----------------------------------- |
| `display: grid;`           | Aktiviert Grid für ein Element      |
| `grid-template-columns`    | Spaltenanzahl und -breite festlegen |
| `grid-template-rows`       | Zeilenanzahl und -höhe festlegen    |
| `gap`                      | Abstand zwischen Elementen          |
| `grid-column` / `grid-row` | Platzierung einzelner Elemente      |

### Beispiel:

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}
```

## 8. Typografie

| Eigenschaft   | Beispiel                          |
| ------------- | --------------------------------- |
| `font-family` | `font-family: Arial, sans-serif;` |
| `font-size`   | `font-size: 16px;`                |
| `font-weight` | `font-weight: bold;`              |
| `line-height` | `line-height: 1.5;`               |
| `text-align`  | `text-align: center;`             |

## 9. Animation und Transition

| Eigenschaft  | Funktion                    |
| ------------ | --------------------------- |
| `transition` | Übergang zwischen Zuständen |
| `animation`  | Ablauf einer Animation      |
| `@keyframes` | Schritte einer Animation    |

### Beispiel:

```css
.button {
  transition: background-color 0.3s;
}
.button:hover {
  background-color: #3498db;
}
@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
```

## 10. Responsive Design mit Media Queries

Media Queries helfen, das Layout je nach Bildschirmgröße anzupassen.

```css
@media (max-width: 768px) {
  .container {
     flex-direction: column;
  }
}
```

---

Dieses Cheat Sheet bietet dir einen schnellen Überblick über die wichtigsten CSS-Eigenschaften und Konzepte. Perfekt für den Alltag und ideal, um CSS-Designs effizient zu gestalten!