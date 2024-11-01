**HTML** (HyperText Markup Language) ist die grundlegende Sprache des Webs und definiert die Struktur und den Inhalt von Webseiten. Die Syntax von HTML besteht aus sogenannten **Tags** (Elementen), die die verschiedenen Bestandteile einer Seite strukturieren und formatieren. Diese Grundlagen geben dir das nötige Wissen, um ein korrekt strukturiertes HTML-Dokument zu erstellen.

## Aufbau eines HTML-Dokuments

Ein HTML-Dokument beginnt immer mit der **Doctype-Deklaration**, die den Dokumenttyp definiert und dem Browser mitteilt, dass es sich um HTML handelt. Die grundlegende Struktur sieht folgendermaßen aus:

```html
<!DOCTYPE html> <html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">     <title>Meine Webseite</title>
</head>
<body>
  <!-- Inhalt der Webseite -->
</body>
</html>
```

### Erklärung der Struktur

1. `<!DOCTYPE html>`: Diese Zeile zeigt dem Browser, dass es sich um ein HTML5-Dokument handelt.
2. `<html lang="de">`: Der `html`-Tag ist der oberste Tag und enthält das gesamte HTML-Dokument. Das `lang`-Attribut gibt die Sprache des Dokuments an.
3. `<head>`: Der `head`-Bereich enthält Metadaten und Links zu Stylesheets oder Skripten. Er ist für den Benutzer nicht sichtbar.
4. `<meta charset="UTF-8">`: Dieser Tag legt das Zeichensatz-Format auf UTF-8 fest und stellt sicher, dass Sonderzeichen korrekt angezeigt werden.
5. `<meta name="viewport" content="width=device-width, initial-scale=1.0">`: Dieser Tag sorgt für responsives Design, damit die Seite auf verschiedenen Geräten gut aussieht.
6. `<title>`: Der Titel der Webseite, der in der Titelleiste des Browsers angezeigt wird.
7. `<body>`: Der `body`-Bereich enthält den sichtbaren Inhalt der Webseite, wie Texte, Bilder und Links.

## HTML-Tags: Aufbau und Anwendung

HTML verwendet **Tags**, die durch spitze Klammern `<>` gekennzeichnet sind. Tags sind meist in **Öffnungs- und Schließ-Tags** unterteilt und umschließen den Inhalt:
```html
<p>Dies ist ein Absatz.</p>
```

Hier ist `<p>` der Öffnungstag und `</p>` der Schließtag. Viele Tags benötigen jedoch keinen Schließtag; diese werden **leere Tags** genannt, wie zum Beispiel `<br>` (Zeilenumbruch) oder `<img>` (Bild).

### Elemente und Attribute

Ein **Element** besteht aus einem Tag und dem darin enthaltenen Inhalt. Tags können **Attribute** enthalten, die zusätzliche Informationen bereitstellen. Zum Beispiel:

```html
<a href="https://example.com" target="_blank">Beispiel-Link</a>
```

Hier sind die wichtigsten Attribute des `<a>`-Tags:

- `href`: Definiert die URL, auf die der Link verweist.
- `target`: Bestimmt, wie der Link geöffnet wird. `_blank` öffnet ihn in einem neuen Tab.

## Wichtige Tags und deren Bedeutung

Hier einige grundlegende HTML-Tags, die du häufig verwenden wirst:

- **Überschriften**: `<h1>` bis `<h6>` definieren Überschriften verschiedener Größen.
```html
<h1>Hauptüberschrift</h1> <h2>Unterüberschrift</h2>
```
- **Absätze**: `<p>` für Absätze.
```html
<p>Dies ist ein Textabsatz.</p>
```
- **Bilder**: `<img>` zur Einbindung von Bildern. `src` gibt den Bildpfad an und `alt` eine Beschreibung.
```html
<img src="bild.jpg" alt="Beschreibung des Bildes">
```
- **Links**: `<a>` für Verlinkungen, wie bereits oben erwähnt.
## Nesting und Strukturierung von Inhalten

In HTML können Elemente ineinander verschachtelt (genestet) sein. Beachte jedoch, dass die Tags immer korrekt geschlossen werden müssen:
```html
<div>
 <h2>Überschrift</h2>
  <p>Ein Absatz innerhalb einer Division.</p>
</div>
```
Hier wird `<div>` als Container für andere Elemente verwendet. Diese Struktur ist wichtig, um den Inhalt logisch zu ordnen und das Layout der Seite zu gestalten.

## Kommentare

Kommentare in HTML werden mit `<!-- Kommentartext -->` erstellt und sind für den Benutzer nicht sichtbar. Sie helfen beim Strukturieren des Codes und beim Hinzufügen von Anmerkungen:
```html
<!-- Dies ist ein Kommentar --> <p>Dies ist ein Absatz.</p>
```
## Best Practices
1. **Saubere Strukturierung**: Verwende Einrückungen, um die Hierarchie der Elemente zu verdeutlichen.
2. **Semantische Tags**: Nutze aussagekräftige Tags, wie `<header>`, `<footer>`, `<article>`, um die Lesbarkeit und SEO deiner Seite zu verbessern.
3. **Validierung**: Verwende Validatoren (z.B. [W3C Validator](https://validator.w3.org/)), um sicherzustellen, dass dein HTML-Code den Standards entspricht.

---

Dieser Artikel bietet eine solide Grundlage für das Verständnis der HTML-Syntax. Von hier aus kannst du tiefer in die Anwendung und Best Practices eintauchen, um komplexere Webseiten zu erstellen.