### Video-Einbindung mit dem `<video>`-Tag

Das `<video>`-Tag in HTML ermöglicht es, Videodateien direkt auf Webseiten einzubetten und den Benutzern Steuerungselemente zur Wiedergabe anzubieten. Es unterstützt verschiedene Videoformate und bietet mehrere Attribute zur Steuerung der Videowiedergabe, was es zu einer flexiblen Lösung für Video-Inhalte auf Webseiten macht.

## Grundstruktur des `<video>`-Tags

Das `<video>`-Tag wird verwendet, um eine Videodatei in HTML einzubinden. Das Attribut `src` gibt die Quelle des Videos an, und das Attribut `controls` sorgt dafür, dass dem Benutzer Bedienelemente wie Abspielen, Pause und Lautstärkeregelung angezeigt werden.
```html
<video src="videos/beispiel.mp4" controls>
  Dein Browser unterstützt das Video-Tag nicht. 
</video>
```
### Attribute des `<video>`-Tags
- **`src`**: Legt die Quelle der Videodatei fest. Dies kann ein relativer oder absoluter Pfad sein.
- **`controls`**: Fügt Steuerungselemente für die Videowiedergabe hinzu, damit Benutzer das Video abspielen, pausieren und die Lautstärke anpassen können.
- **Fallback-Inhalt**: Der Text zwischen den `<video>`-Tags wird nur angezeigt, wenn der Browser das `<video>`-Tag nicht unterstützt. Dies ist eine Möglichkeit, die Benutzer auf die Aktualisierung ihres Browsers hinzuweisen oder einen alternativen Link anzubieten.
### Beispiel für eine einfache Video-Einbindung
```html
<video src="videos/beispiel.mp4" controls>
  Dein Browser unterstützt das Video-Tag nicht.
</video>
```
In diesem Beispiel erhält der Benutzer einfache Steuerelemente, um die Videodatei `beispiel.mp4` abzuspielen.
## Wichtige Attribute des `<video>`-Tags
Zusätzlich zu `src` und `controls` bietet das `<video>`-Tag weitere Attribute, die das Abspielverhalten des Videos steuern.
- **`autoplay`**: Startet das Video automatisch beim Laden der Seite. **Hinweis**: Autoplay kann in vielen Browsern blockiert sein, insbesondere wenn das Video nicht stummgeschaltet ist.
```html
<video src="videos/beispiel.mp4" autoplay></video>
```
- **`loop`**: Wiederholt das Video endlos, bis die Wiedergabe manuell gestoppt wird.
```html
<video src="videos/beispiel.mp4" controls loop></video>
```
- **`muted`**: Startet das Video stummgeschaltet. Dies ist häufig in Kombination mit `autoplay` nützlich, da viele Browser Autoplay-Videos blockieren, wenn sie nicht stummgeschaltet sind.
```html
<video src="videos/beispiel.mp4" controls autoplay muted></video>
```
- **`preload`**: Gibt an, wie viel des Videos vorab geladen werden soll. Die Optionen sind:
    - `none`: Das Video wird nicht vorab geladen.
    - `metadata`: Nur die Metadaten (Dauer, Abmessungen usw.) werden geladen.
    - `auto`: Das gesamte Video wird beim Laden der Seite geladen.
```html
<video src="videos/beispiel.mp4" controls preload="auto"></video>
```
## Einbindung mehrerer Videoquellen für bessere Kompatibilität
Nicht alle Browser unterstützen jedes Videoformat. Um eine optimale Kompatibilität sicherzustellen, kannst du mehrere Quellen im `<video>`-Tag angeben. Der Browser wählt automatisch das erste unterstützte Format aus.
### Beispiel mit mehreren Quellen
```html
<video controls>
  <source src="videos/beispiel.mp4" type="video/mp4">
  <source src="videos/beispiel.webm" type="video/webm">
    Dein Browser unterstützt das Video-Tag nicht.
  </video>
```
In diesem Beispiel sind zwei Videoformate eingebunden: `MP4` und `WebM`. Falls der Browser das MP4-Format nicht unterstützt, versucht er das WebM-Format abzuspielen.
## Poster-Attribut
Das `poster`-Attribut zeigt ein Bild als Vorschau an, bevor das Video abgespielt wird. Es ist nützlich, um dem Benutzer eine visuelle Vorschau des Videos zu geben.
```html
<video src="videos/beispiel.mp4" controls poster="bilder/vorschaubild.jpg">
  Dein Browser unterstützt das Video-Tag nicht.
</video>
```
Hier wird `vorschaubild.jpg` als Bild angezeigt, solange das Video noch nicht abgespielt wird.
## Styling des `<video>`-Tags mit CSS
Das `<video>`-Tag kann mit CSS wie andere HTML-Elemente gestylt werden. Hier ist ein einfaches Beispiel, um den Video-Container anzupassen.
```css
video {
  max-width: 100%; /* Video passt sich der Bildschirmbreite an */
  border: 2px solid #333; /* Rahmen für das Video */
  border-radius: 8px; /* Abgerundete Ecken */
}
```
Mit diesen CSS-Regeln passt sich das Video der Bildschirmbreite an und hat abgerundete Ecken.
## Fallback für Browser ohne `<video>`-Support
Für ältere Browser, die das `<video>`-Tag nicht unterstützen, kannst du einen Download-Link oder alternativen Inhalt bereitstellen. Dies ist ein guter Ansatz, um sicherzustellen, dass alle Benutzer Zugang zum Inhalt haben.
```html
<video controls>
  <source src="videos/beispiel.mp4" type="video/mp4">
  <source src="videos/beispiel.webm" type="video/webm">
  Dein Browser unterstützt das Video-Tag nicht. Du kannst das Video direkt 
  <a href="videos/beispiel.mp4">herunterladen</a>. 
</video>
```
In diesem Fall wird ein Download-Link angezeigt, falls das Video nicht abgespielt werden kann.
## Best Practices für die Verwendung des `<video>`-Tags
1. **Mehrere Formate bereitstellen**: Verwende verschiedene Formate (z.B. MP4 und WebM), um sicherzustellen, dass das Video in allen Browsern abgespielt werden kann.
2. **Autoplay sparsam verwenden**: Autoplay kann für viele Nutzer störend sein und wird in den meisten Browsern blockiert, es sei denn, das Video ist stummgeschaltet.
3. **Dateigröße optimieren**: Videos können große Dateien sein und die Ladezeit der Seite beeinflussen. Verwende komprimierte Formate und lagere große Dateien, wenn möglich, auf externen Medienservern oder Content Delivery Networks (CDNs).
4. **Barrierefreiheit**: Füge Untertitel oder Transkripte hinzu, um den Inhalt für hörbehinderte Benutzer zugänglich zu machen. Dies kann über das `<track>`-Tag innerhalb des `<video>`-Tags erfolgen.

### Beispiel mit Untertitel-Datei
```html
<video controls>
  <source src="videos/beispiel.mp4" type="video/mp4">
  <track src="untertitel.vtt" kind="subtitles" srclang="de" label="Deutsch">
  Dein Browser unterstützt das Video-Tag nicht.
</video>
```
Hier wird eine `.vtt`-Datei für die Untertitel eingebunden, die den Video-Inhalt für Benutzer mit Hörbehinderungen zugänglich macht.

---

Dieser Artikel bietet eine fundierte Einführung in die Verwendung des `<video>`-Tags zur Einbindung von Videodateien in HTML. Mit den vorgestellten Attributen und Best Practices kannst du Videos effektiv in Webseiten integrieren und für eine breite Benutzerbasis zugänglich machen.