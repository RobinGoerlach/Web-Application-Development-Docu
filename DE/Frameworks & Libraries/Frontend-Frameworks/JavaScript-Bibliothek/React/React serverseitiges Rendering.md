# **Das Framework für moderne Webanwendungen**

**Next.js** ist ein leistungsstarkes React-Framework, das die Entwicklung moderner Webanwendungen erheblich vereinfacht. Es bietet Funktionen wie serverseitiges Rendering (SSR), statische Seitengenerierung (SSG) und API-Routing, wodurch es sich hervorragend für Performance-optimierte Anwendungen eignet. Dieser Artikel beleuchtet die Grundlagen, Vorteile und die Nutzung von Next.js in React-Projekten.

---
## **Warum Next.js?**
Next.js erweitert React um Funktionen, die in modernen Webprojekten unverzichtbar sind:
1. **Serverseitiges Rendering (SSR):**    
    - Dynamische Inhalte werden auf dem Server gerendert und an den Client gesendet, was zu schnelleren Ladezeiten und besserer SEO führt.        
2. **Statische Seitengenerierung (SSG):**    
    - Seiten können zur Build-Zeit generiert werden, was die Performance und Sicherheit erhöht.        
3. **Integriertes Routing:**    
    - Kein zusätzliches Routing-Paket nötig. Die Dateistruktur definiert automatisch die Routen   
4. **API-Integration:**    
    - Mit Next.js können APIs direkt innerhalb des Projekts erstellt werden.        
5. **Vorteile für SEO:**    
    - Durch SSR und SSG sind Inhalte für Suchmaschinen direkt sichtbar.        
6. **Automatisches Code-Splitting:**    
    - JavaScript wird nur für die benötigten Seiten geladen, wodurch die Performance optimiert wird.
        
---
## **Installation und Setup**
### **1. Neues Next.js-Projekt erstellen**
Next.js kann mit dem Befehl `create-next-app` schnell eingerichtet werden:
```
npx create-next-app@latest my-next-app
cd my-next-app
npm run dev
```
### **2. Projektstruktur**
Nach der Erstellung hat das Projekt folgende Struktur:
```
my-next-app/
├── pages/
│   ├── index.js
│   ├── about.js
├── public/
├── styles/
├── next.config.js
```
- `**pages/**`: Enthält die Seiten der Anwendung. Jede Datei entspricht einer Route.    
- `**public/**`: Statische Dateien wie Bilder.    
- `**styles/**`: CSS- oder SCSS-Dateien.    
- `**next.config.js**`: Konfigurationsdatei für das Projekt.
    
---
## **Routing in Next.js**
Das Routing in Next.js basiert auf der Dateistruktur im Verzeichnis `pages/`.
### **1. Basisrouting**
Erstellen Sie eine neue Datei `about.js` im Ordner `pages/`:
```
export default function About() {
  return <h1>About Page</h1>;
}
```
Die Seite ist automatisch unter `/about` verfügbar.
### **2. Dynamische Routen**
Dynamische Routen werden durch Dateinamen mit eckigen Klammern definiert.
```
// Datei: pages/post/[id].js
import { useRouter } from 'next/router';

export default function Post() {
  const router = useRouter();
  const { id } = router.query;

  return <h1>Post ID: {id}</h1>;
}
```
Die Route `/post/123` rendert die Seite mit `Post ID: 123`.

---
## **Datenfetching in Next.js**
Next.js bietet verschiedene Methoden, um Daten zu laden:
### **1.** `**getStaticProps**`
Für statische Seiten, deren Daten zur Build-Zeit geladen werden.
```
export async function getStaticProps() {
  const data = await fetch('https://api.example.com/data').then(res => res.json());
  return { props: { data } };
}

export default function Page({ data }) {
  return <div>{JSON.stringify(data)}</div>;
}
```
### **2.** **`getServerSideProps`**
Für serverseitig gerenderte Seiten, bei denen Daten bei jeder Anfrage geladen werden.
```
export async function getServerSideProps() {
  const data = await fetch('https://api.example.com/data').then(res => res.json());
  return { props: { data } };
}

export default function Page({ data }) {
  return <div>{JSON.stringify(data)}</div>;
}
```
### **3.** **`getStaticPaths`**
Für dynamische statische Seiten mit mehreren möglichen Routen.
```
export async function getStaticPaths() {
  const paths = [
    { params: { id: '1' } },
    { params: { id: '2' } },
  ];
  return { paths, fallback: false };
}

export async function getStaticProps({ params }) {
  const data = await fetch(`https://api.example.com/data/${params.id}`).then(res => res.json());
  return { props: { data } };
}

export default function Page({ data }) {
  return <div>{JSON.stringify(data)}</div>;
}
```
---
## **API-Routen in Next.js**
Next.js erlaubt das Erstellen von API-Endpunkten im Verzeichnis `pages/api/`.
### **Beispiel:**
```
// Datei: pages/api/hello.js
export default function handler(req, res) {
  res.status(200).json({ message: 'Hello, API!' });
}
```
Die API ist unter `/api/hello` verfügbar.

---
## **Best Practices für Next.js**
1. **Datenfetching strategisch einsetzen:**    
    - Verwenden Sie `getStaticProps` für häufig besuchte, sich selten ändernde Seiten.        
    - Nutzen Sie `getServerSideProps` für personalisierte oder oft aktualisierte Daten.        
2. **SEO optimieren:**    
    - Nutzen Sie das `<Head>`-Modul von Next.js für Meta-Tags.
            
    ```
    import Head from 'next/head';
    
    export default function Page() {
      return (
        <>
          <Head>
            <title>My Page</title>
            <meta name="description" content="My Page Description" />
          </Head>
          <h1>Content</h1>
        </>
      );
    }
    ```    
3. **Code-Splitting effektiv nutzen:**    
    - Importieren Sie Komponenten und Module dynamisch mit `next/dynamic`.
            
    ```
    import dynamic from 'next/dynamic';    
    const DynamicComponent = dynamic(() => import('../components/MyComponent'));
    ```    
4. **Bildoptimierung:**    
    - Verwenden Sie das `next/image`-Modul für optimierte Bilder.
            
    ```
    import Image from 'next/image';
    
    export default function Page() {
      return <Image src="/my-image.jpg" width={500} height={300} alt="My Image" />;
    }
    ```    

---
## **Fazit**
Next.js erweitert die Möglichkeiten von React, indem es leistungsstarke Features wie serverseitiges Rendering, statische Seitengenerierung und integriertes Routing bereitstellt. Es ist die ideale Wahl für Anwendungen, die hohe Performance, SEO-Optimierung und eine nahtlose Entwicklererfahrung erfordern. Mit Next.js können Sie moderne Webanwendungen schnell und effizient entwickeln.