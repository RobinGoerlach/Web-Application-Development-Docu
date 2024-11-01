Bilder sind ein wesentlicher Bestandteil moderner Webseiten und tragen zur visuellen Attraktivität und Benutzererfahrung bei. In HTML wird das `<img>`-Tag verwendet, um Bilder in Webseiten einzubinden. Dabei helfen die Attribute `src` und `alt`, das Bild zu laden und es für alle Nutzer – einschließlich Suchmaschinen und Screenreader – zugänglich zu machen.
## Das `<img>`-Tag
Das `<img>`-Tag ist ein sogenanntes **leeres Tag**, das keinen Schließtag (`</img>`) benötigt. Es steht einfach allein und enthält alle Informationen, die zum Laden und Anzeigen eines Bildes erforderlich sind.
### Grundstruktur des `<img>`-Tags
```html
<img src="bild.jpg" alt="Beschreibung des Bildes">
```
### Erklärung der wichtigsten Attribute
- **`src`** (source): Gibt die Bildquelle an, also den Pfad zum Bild. Dies kann eine URL zu einem externen Bild oder eine relative Pfadangabe zu einem Bild auf dem eigenen Server sein.
- **`alt`** (alternative): Beschreibt das Bild für den Fall, dass es nicht geladen wird oder für Nutzer, die Screenreader verwenden. Das `alt`-Attribut ist ein wesentlicher Bestandteil barrierefreier Webgestaltung.
## Das `src`-Attribut

Das `src`-Attribut ist erforderlich und definiert die Bildquelle. Du kannst absolute oder relative Pfade verwenden:
- **Absoluter Pfad**: Ein externer Link, der auf ein Bild außerhalb der eigenen Webseite verweist.
```html
<img src="https://example.com/images/logo.png" alt="Beispiel-Logo">
```
- **Relativer Pfad**: Ein Pfad, der auf ein Bild verweist, das sich auf dem gleichen Server wie die Webseite befindet.
```html
<img src="images/logo.png" alt="Beispiel-Logo">
```
Bei relativen Pfaden ist es sinnvoll, eine klare Ordnerstruktur anzulegen, etwa einen „images“-Ordner für Bilder. So bleibt die Dateistruktur übersichtlich und das Laden der Bilder erfolgt effizient.
## Das `alt`-Attribut
Das `alt`-Attribut ist eine kurze Beschreibung des Bildes und erfüllt mehrere wichtige Funktionen:
1. **Barrierefreiheit**: Screenreader lesen den `alt`-Text vor, damit sehbehinderte Benutzer die Bedeutung des Bildes verstehen können.
2. **Suchmaschinenoptimierung (SEO)**: Suchmaschinen bewerten den `alt`-Text, um den Inhalt von Bildern besser zu verstehen und zu indexieren.
3. **Fallback-Text**: Wenn ein Bild nicht geladen werden kann (z.B. aufgrund einer langsamen Verbindung oder eines fehlenden Bildes), wird der `alt`-Text angezeigt.
**Beispiel mit einem aussagekräftigen `alt`-Text**:
```html
<img src="bilder/sonnenuntergang.jpg" alt="Sonnenuntergang am Strand mit Palmen">
```
### Tipps für das `alt`-Attribut
- Der Text sollte das Bild kurz, aber aussagekräftig beschreiben.
- Vermeide den Gebrauch von „Bild von...“ oder „Grafik zeigt...“, da dies bereits vom `alt`-Attribut impliziert wird.
- Verzichte auf leere `alt`-Attribute nur dann, wenn das Bild rein dekorativ ist und keine semantische Bedeutung für den Inhalt hat.
## Weitere nützliche Attribute für das `<img>`-Tag
- **`width` und `height`**: Legen die Breite und Höhe des Bildes fest. Diese Attribute sind optional, aber nützlich, um das Layout vorab zu definieren und das Rendering der Seite zu optimieren.
```html
<img src="bilder/logo.png" alt="Beispiel-Logo" width="200" height="100">
```
> **Hinweis**: Die Angabe von `width` und `height` in HTML kann das Layout stabilisieren, indem der Browser den Platz für das Bild vorab reserviert. 
- **`title`**: Fügt einen Tooltipp hinzu, der angezeigt wird, wenn der Benutzer mit der Maus über das Bild fährt.
```html
<img src="bilder/logo.png" alt="Beispiel-Logo" title="Unser Firmenlogo">
```
## Beispiele für die Bild-Einbindung
### 1. Einfache Einbindung eines Bildes
```html
<img src="images/natur.jpg" alt="Ein Wald mit hohen Bäumen">
```
### 2. Bild mit Größenangaben
Wenn du die Größe des Bildes in HTML festlegst, kannst du Platz reservieren und das Layout stabilisieren. Dies kann vor allem bei langsam ladenden Seiten hilfreich sein.
```html
<img src="images/landschaft.jpg" alt="Schöne Landschaft mit Bergen" width="300" height="200">
```
### 3. Bild mit absolutem Pfad
```html
<img src="https://example.com/images/landschaft.jpg" alt="Berglandschaft mit Sonnenaufgang">
```
### 4. Beispiel mit dekorativem Bild (leerer `alt`-Text)
Manchmal gibt es Bilder, die nur zur Dekoration dienen und keine zusätzliche Information vermitteln. In solchen Fällen kann der `alt`-Text leer bleiben:
```html
<img src="images/borduere.png" alt="">
```
## Best Practices für die Verwendung von Bildern in HTML
1. **Optimierte Dateigröße**: Verwende komprimierte Bildformate wie JPEG für Fotos und PNG für Grafiken. Dadurch wird die Ladezeit der Webseite reduziert.
2. **Responsives Design**: Für Webseiten, die auf verschiedenen Geräten verwendet werden, solltest du sicherstellen, dass die Bilder auf kleineren Bildschirmen angepasst und eventuell durch kleinere Versionen ersetzt werden.
3. **Aussagekräftiger `alt`-Text**: Der `alt`-Text sollte das Bild in wenigen Worten beschreiben und so die Barrierefreiheit und SEO verbessern.
4. **Verwende das `srcset`-Attribut**: Das `srcset`-Attribut erlaubt es, unterschiedliche Bildversionen für verschiedene Bildschirmauflösungen bereitzustellen und so die Ladezeiten zu optimieren.
**Beispiel für `srcset`:**
```html
<img src="images/natur-klein.jpg" 
	 srcset="images/natur-gross.jpg 1024w, images/natur-medium.jpg 768w, images/natur-klein.jpg 480w" 
	 alt="Waldlandschaft">
```
Im `srcset`-Attribut können verschiedene Bildgrößen für verschiedene Bildschirmauflösungen definiert werden. Der Browser wählt dann die passendste Größe basierend auf der Bildschirmbreite des Benutzers aus.

---

Dieser Artikel bietet eine Übersicht über das `<img>`-Tag und die Verwendung von `src` und `alt`, um Bilder auf Webseiten korrekt und barrierefrei einzubinden. Durch eine durchdachte Bildauswahl und Optimierung kannst du die visuelle Qualität und Benutzerfreundlichkeit deiner Webseite verbessern.