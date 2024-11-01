## Die wichtigsten HTML-Elemente und Attribute auf einen Blick

#### 1. **Grundstruktur einer HTML-Seite**

```html
<!DOCTYPE html>
<html lang="de"> 
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Seitentitel</title>
  </head>
  <body>
     <!-- Inhalt hier -->
  </body>
</html>
```

#### 2. **Textformatierung**

| Tag           | Beschreibung                      | Beispiel                      |
| ------------- | --------------------------------- | ----------------------------- |
| `<p>`         | Absatz                            | `<p>Dies ist ein Absatz.</p>` |
| `<h1>`–`<h6>` | Überschriften von groß nach klein | `<h1>Hauptüberschrift</h1>`   |
| `<strong>`    | Fett (starke Betonung)            | `<strong>Wichtig!</strong>`   |
| `<em>`        | Kursiv (Betonung)                 | `<em>Besonders</em>`          |
| `<br>`        | Zeilenumbruch                     | `Text<br>Umbruch`             |

#### 3. **Links und Bilder**

| Tag               | Beschreibung              | Beispiel                                    |
| ----------------- | ------------------------- | ------------------------------------------- |
| `<a>`             | Hyperlink                 | `<a href="https://example.com">Link</a>`    |
| `<img>`           | Bild einfügen             | `<img src="bild.jpg" alt="Beschreibung">`   |
| `target="_blank"` | Link in neuem Tab öffnen  | `<a href="#" target="_blank">Neuer Tab</a>` |
| `alt`             | Alternativtext für Bilder | `<img src="bild.jpg" alt="Beschreibung">`   |

#### 4. **Listen**

| Tag    | Beschreibung      | Beispiel                      |
| ------ | ----------------- | ----------------------------- |
| `<ul>` | Ungeordnete Liste | `<ul><li>Element 1</li></ul>` |
| `<ol>` | Geordnete Liste   | `<ol><li>Element 1</li></ol>` |
| `<li>` | Listenelement     | `<li>Listenpunkt</li>`        |

#### 5. **Tabellen**

| Tag                           | Beschreibung        | Beispiel                  |
| ----------------------------- | ------------------- | ------------------------- |
| `<table>`                     | Tabelle             | `<table>...</table>`      |
| `<tr>`                        | Tabellenzeile       | `<tr>...</tr>`            |
| `<td>`                        | Tabellenzelle       | `<td>Inhalt</td>`         |
| `<th>`                        | Tabellenüberschrift | `<th>Überschrift</th>`    |
| `<thead>` `<tbody>` `<tfoot>` | Tabellenstruktur    | `<thead>...</thead>` usw. |

#### 6. **Formularelemente**

| Tag             | Beschreibung                 | Beispiel                                 |
| --------------- | ---------------------------- | ---------------------------------------- |
| `<form>`        | Formular                     | `<form action="/send" method="post">`    |
| `<input>`       | Eingabefeld                  | `<input type="text" name="name">`        |
| `<button>`      | Schaltfläche                 | `<button type="submit">Senden</button>`  |
| `<label>`       | Beschriftung für Eingabefeld | `<label for="id">Name:</label>`          |
| `type="email"`  | E-Mail-Eingabe               | `<input type="email">`                   |
| `type="number"` | Nummer-Eingabe               | `<input type="number" min="1" max="10">` |

#### 7. **HTML5-Semantische Tags**

| Tag         | Beschreibung           | Beispiel                       |
| ----------- | ---------------------- | ------------------------------ |
| `<header>`  | Kopfbereich            | `<header>Seitentitel</header>` |
| `<nav>`     | Navigationsbereich     | `<nav>Navigation</nav>`        |
| `<main>`    | Hauptinhalt            | `<main>Hauptinhalt</main>`     |
| `<article>` | Eigenständiger Artikel | `<article>Blogpost</article>`  |
| `<section>` | Abschnitt              | `<section>Abschnitt</section>` |
| `<footer>`  | Fußbereich             | `<footer>Fußzeile</footer>`    |

#### 8. **Multimedia**

| Tag        | Beschreibung           | Beispiel                                      |
| ---------- | ---------------------- | --------------------------------------------- |
| `<img>`    | Bild                   | `<img src="bild.jpg" alt="Bildbeschreibung">` |
| `<video>`  | Video                  | `<video controls src="video.mp4"></video>`    |
| `<audio>`  | Audio                  | `<audio controls src="audio.mp3"></audio>`    |
| `<source>` | Quelle für Video/Audio | `<source src="datei.mp4" type="video/mp4">`   |

#### 9. **Metadaten und Dokument-Header**

| Tag                      | Beschreibung               | Beispiel                                                                 |
| ------------------------ | -------------------------- | ------------------------------------------------------------------------ |
| `<meta charset="UTF-8">` | Zeichensatz festlegen      | `<meta charset="UTF-8">`                                                 |
| `<meta name="viewport">` | Viewport für Responsivität | `<meta name="viewport" content="width=device-width, initial-scale=1.0">` |
| `<title>`                | Seitentitel                | `<title>Mein Titel</title>`                                              |
| `<link>`                 | Verlinkung zu CSS/Icons    | `<link rel="stylesheet" href="styles.css">`                              |

#### 10. **Spezial-Tags**

| Tag                  | Beschreibung                    | Beispiel                                      |
| -------------------- | ------------------------------- | --------------------------------------------- |
| `<!-- Kommentar -->` | Kommentar                       | `<!-- Dies ist ein Kommentar -->`             |
| `<iframe>`           | Externe Inhalte einbetten       | `<iframe src="https://example.com"></iframe>` |
| `<script>`           | JavaScript einbinden            | `<script src="script.js"></script>`           |
| `<noscript>`         | Alternative für kein JavaScript | `<noscript>JS nicht verfügbar</noscript>`     |
| `<style>`            | Inline-CSS                      | `<style>body { font-size: 16px; }</style>`    |

---

Dieser HTML Cheatsheet bietet eine kompakte Übersicht der wichtigsten HTML-Elemente und Attribute für schnelle Referenzen.