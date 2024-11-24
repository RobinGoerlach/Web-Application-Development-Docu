# Eine Einführung

**CSS Float** ist eine ältere Layout-Technik, die in den frühen Tagen des Webdesigns eine zentrale Rolle spielte. Ursprünglich entwickelt, um Inhalte wie Text und Bilder nebeneinander darzustellen, wurde Float für viele Jahre als Standard-Tool zur Erstellung von Layouts verwendet. Auch wenn moderne Technologien wie **Flexbox** und **Grid** heute bevorzugt werden, bleibt das Verständnis von Float wichtig, um ältere Projekte zu warten und historische Konzepte zu verstehen.

## Was ist Float?

Der Float-Eigenschaft wird ein Element „aus dem normalen Dokumentenfluss entfernt“, sodass der nachfolgende Inhalt um es herumfließen kann. Float wurde vor allem für die Erstellung einfacher zweispaltiger Layouts verwendet oder um Text neben einem Bild anzuordnen.

### Mögliche Werte für Float:

- `**none**`: (Standard) Das Element bleibt im normalen Fluss und wird nicht gefloatet.
    
- `**left**`: Das Element wird an den linken Rand seines Containers verschoben.
    
- `**right**`: Das Element wird an den rechten Rand seines Containers verschoben.
    
- `**inherit**`: Übernimmt den Float-Wert des übergeordneten Elements.
    

## Grundlegende Anwendung

```
<div style="float: left; width: 50%;">
    <p>Dies ist eine gefloatete Box, die links ausgerichtet ist.</p>
</div>
<div style="float: right; width: 50%;">
    <p>Dies ist eine gefloatete Box, die rechts ausgerichtet ist.</p>
</div>
```

In diesem Beispiel werden zwei Boxen erstellt, die jeweils die Hälfte des verfügbaren Platzes einnehmen und an entgegengesetzten Seiten des Containers ausgerichtet sind.

## Probleme und Herausforderungen

Obwohl Float mächtig war, brachte es auch einige Herausforderungen mit sich:

### 1. **Collapsing Container**

Wenn alle Kind-Elemente eines Containers gefloatet sind, wird der Container oft auf eine Höhe von 0 reduziert, da gefloatete Elemente nicht zur Höhe des Containers beitragen.

**Lösung:** Verwenden eines clearfix-Hacks:

```
.clearfix::after {
    content: "";
    display: table;
    clear: both;
}
```

Füge diese Klasse zum übergeordneten Container hinzu, um das Problem zu beheben:

```
<div class="clearfix">
    <div style="float: left; width: 50%;">Linke Spalte</div>
    <div style="float: right; width: 50%;">Rechte Spalte</div>
</div>
```

### 2. **Reihenfolge und Flexibilität**

Gefloatete Layouts können starr sein, da die Reihenfolge der Elemente im DOM die Reihenfolge im Layout beeinflusst. Das macht es schwierig, Elemente zu repositionieren oder ein responsives Design zu erstellen.

## Float und modernes Webdesign

Heute wird Float selten für Layouts verwendet, da **Flexbox** und **CSS Grid** wesentlich flexibler und leichter zu handhaben sind. Float findet jedoch noch immer Anwendung, insbesondere für kleinere Aufgaben wie das Platzieren von Bildern in Text:

```
<img src="beispiel.jpg" alt="Beispiel" style="float: left; margin: 0 10px 10px 0;">
<p>Dieser Text fließt um das Bild herum, da es nach links gefloatet wurde.</p>
```

## Vor- und Nachteile von Float

### Vorteile:

- Einfach zu implementieren.
- Funktioniert in allen Browsern, selbst in sehr alten Versionen.
- Gut geeignet für einfache Layouts oder um Text um Bilder fließen zu lassen.
    
### Nachteile:

- Anfällig für Layout-Probleme (z. B. Collapsing Container).   
- Nicht flexibel für komplexe oder responsive Layouts.    
- Pflege und Erweiterung sind schwieriger im Vergleich zu modernen Methoden.
    
## Fazit

Float war eine bahnbrechende Technologie, die die Entwicklung des Webdesigns revolutionierte. Mit der Einführung moderner Layout-Techniken wie **[Flexbox](CSS&20Felxbox.md)** und **[Grid](CSS%20Grid.md)** ist Float jedoch in den Hintergrund getreten. Dennoch bleibt ein solides Verständnis von Float unerlässlich, insbesondere für Entwickler, die mit älteren Codebasen arbeiten oder das historische Wissen über CSS erweitern möchten.