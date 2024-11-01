**Media Queries** sind ein leistungsstarkes Werkzeug in CSS, das es ermöglicht, Layouts flexibel zu gestalten und an verschiedene Bildschirmgrößen und Geräte anzupassen. Durch Media Queries kannst du spezifische CSS-Regeln nur unter bestimmten Bedingungen anwenden und so ein responsives Design erstellen, das auf Mobilgeräten, Tablets und Desktops gleichermaßen gut funktioniert.

## Grundlagen von Media Queries

Eine Media Query überprüft bestimmte Eigenschaften des Ansichtsfensters oder Geräts, z.B. die Breite oder Höhe des Bildschirms, und führt CSS-Regeln nur dann aus, wenn die Bedingungen erfüllt sind. Die Syntax für eine Media Query sieht wie folgt aus:
```css
@media (Bedingung) {     /* CSS-Regeln, die nur gelten, wenn die Bedingung erfüllt ist */ 
}
```

### Beispiel: Media Query für Bildschirme bis 768px Breite
```css
@media (max-width: 768px) {
  .container {
     padding: 10px;
  } 
}
```
In diesem Beispiel wird das `padding` der `.container`-Klasse auf 10px gesetzt, aber nur, wenn die Bildschirmbreite 768px oder weniger beträgt.

---

## 1. Wichtige Media Query-Bedingungen

### `max-width` und `min-width`
- **`max-width`**: Wendet die Regeln an, wenn die Bildschirmbreite kleiner oder gleich dem angegebenen Wert ist.
- **`min-width`**: Wendet die Regeln an, wenn die Bildschirmbreite mindestens dem angegebenen Wert entspricht.

Diese beiden Bedingungen sind die am häufigsten verwendeten und eignen sich besonders für responsive Layouts, die auf einer mobilen Ansicht basieren.
```css
@media (max-width: 600px) {
  /* Regeln für schmale Bildschirme (z.B. Smartphones) */ 
}  
@media (min-width: 1024px) {
  /* Regeln für große Bildschirme (z.B. Desktops) */ 
}
```

### `max-height` und `min-height`
- **`max-height`** und **`min-height`** funktionieren ähnlich wie `max-width` und `min-width`, beziehen sich jedoch auf die Höhe des Ansichtsfensters. Diese Bedingungen sind nützlich für die Anpassung an spezielle Bildschirmhöhen.
```css
@media (min-height: 800px) {     /* Regeln für hohe Bildschirme */ 
}
```

### `orientation`
Mit der **`orientation`**-Bedingung kannst du festlegen, ob eine Regel nur im Hochformat (`portrait`) oder im Querformat (`landscape`) gelten soll.
```css
@media (orientation: portrait) {
  /* Regeln für Hochformat (z.B. bei Smartphones) */ 
}  
@media (orientation: landscape) {
  /* Regeln für Querformat (z.B. bei Tablets im Querformat) */ 
}
```

### `aspect-ratio`

Die **`aspect-ratio`**-Bedingung ermöglicht es, das Verhältnis von Breite zu Höhe des Ansichtsfensters als Bedingung zu verwenden. Diese Funktion ist nützlich, um Layouts auf bestimmte Bildschirmverhältnisse anzupassen.
```css
@media (aspect-ratio: 16/9) {
 /* Regeln für Bildschirme mit einem Seitenverhältnis von 16:9 */
}
```

---

## 2. Kombinierte Bedingungen

Media Queries unterstützen auch kombinierte Bedingungen. Du kannst mehrere Bedingungen mit den Operatoren `and`, `or` (als `,`) und `not` kombinieren.

### Beispiel: Kombination von `max-width` und `orientation`
```css
@media (max-width: 768px) and (orientation: portrait) {
  .sidebar {
    display: none;
  }
}
```

In diesem Beispiel wird die `.sidebar`-Klasse ausgeblendet, wenn die Bildschirmbreite maximal 768px beträgt und sich das Gerät im Hochformat befindet.

### Beispiel: Mehrere Breakpoints

Du kannst Media Queries auch hintereinander verwenden, um spezifische Regeln für verschiedene Bildschirmgrößen zu definieren. Dies nennt man **Breakpoints**.
```css
/* Für Smartphones im Hochformat */ 
@media (max-width: 480px) {
  .container {
    font-size: 14px;
  }
}  
/* Für Tablets im Hochformat */ 
@media (max-width: 768px) {
  .container {
     font-size: 16px;
  }
}  
/* Für Desktops und größere Geräte */ 
@media (min-width: 1024px) {
  .container {
    font-size: 18px;
  } 
}
```

---

## 3. Mobile-First-Ansatz

Ein **Mobile-First-Ansatz** bedeutet, dass du dein Grundlayout für mobile Geräte (kleine Bildschirme) erstellst und das Layout dann mit `min-width`-Media Queries für größere Bildschirme anpasst. Dieser Ansatz ist effizient und reduziert das Laden überflüssiger Styles auf mobilen Geräten.

### Beispiel: Mobile-First-Design
```css
/* Grundlayout für Mobilgeräte */ 
.container {
  font-size: 14px;
  padding: 10px;
}
/* Anpassungen für Tablets */ 
@media (min-width: 768px) {
  .container {
    font-size: 16px;
    padding: 20px;
  }
} 
/* Anpassungen für Desktops */
@media (min-width: 1024px) {
  .container {
    font-size: 18px;
    padding: 30px;
  }
}
```
Im obigen Beispiel wird das Grundlayout für mobile Geräte erstellt und mit `min-width`-Bedingungen für Tablets und Desktops angepasst.

---

## 4. Häufige Breakpoints für responsive Designs

Hier sind einige häufig verwendete Breakpoints für responsive Designs. Beachte, dass es keine festen Standardwerte gibt, aber diese Werte häufig genutzt werden:
- **320px**: Kleine Smartphones
- **480px**: Größere Smartphones
- **768px**: Tablets im Hochformat
- **1024px**: Tablets im Querformat, kleine Laptops
- **1200px**: Desktops
- **1600px** und mehr: Große Desktops und Bildschirme

---

## 5. Beispiel: Komplettes responsives Layout mit Media Queries

Hier ist ein Beispiel, das zeigt, wie Media Queries verwendet werden können, um ein responsives Layout für verschiedene Bildschirmgrößen zu erstellen.
HTML:
```html
<div class="header">Header</div>
<div class="content">Content</div>
<div class="sidebar">Sidebar</div>
<div class="footer">Footer</div>
```
CSS:
```css
/* Grundlayout für mobile Geräte */
.header, .footer {
  background-color: #3498db;
  color: #fff;
  padding: 10px;
  text-align: center;
}
.content, .sidebar {
  padding: 10px;
}
.sidebar {  
  /* Sidebar auf Mobilgeräten ausblenden */
  display: none;  
}
/* Tablets im Hochformat */
@media (min-width: 768px) {
  .sidebar {
     display: block;
     background-color: #f1c40f;
  }
  .content {
     width: 70%;
     float: left;
  }
  .sidebar {
     width: 30%;
     float: left;
  }
}  
/* Desktops und größere Geräte */ 
@media (min-width: 1024px) {
  .content {
     width: 75%;
  }
  .sidebar {
     width: 25%;
  } 
}
```

### Erläuterung
- Auf **Mobilgeräten** (Standard-Layout) wird die `.sidebar` ausgeblendet, und alle Bereiche sind untereinander angeordnet.
- Auf **Tablets** wird die `.sidebar` eingeblendet und neben dem `.content` platziert, um den Bildschirmplatz optimal zu nutzen.
- Auf **Desktops** nimmt der `.content`-Bereich mehr Platz ein, während die `.sidebar` auf 25% begrenzt ist.

---

## Zusammenfassung
Media Queries sind unverzichtbar für das Erstellen responsiver Layouts in CSS. Mit ihnen kannst du:
- **Spezifische Layouts für verschiedene Bildschirmgrößen und Geräte** erstellen.
- **Mobile-First oder Desktop-First** Ansätze anwenden, um deine CSS-Regeln zu organisieren.
- **Flexible und anpassungsfähige Designs** entwickeln, die auf allen Geräten gut funktionieren.

Durch das Verständnis von Media Queries und deren Anwendung auf Breakpoints kannst du benutzerfreundliche, flexible und responsive Webseiten erstellen, die sich an die Anforderungen der modernen Webnutzung anpassen.