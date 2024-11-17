## **Einführung in die Versionskontrolle**

Versionskontrolle ist ein unverzichtbarer Bestandteil moderner Softwareentwicklung. Sie ermöglicht es Entwicklern, Änderungen an ihrem Code zu verfolgen, frühere Versionen wiederherzustellen und effektiv in Teams zusammenzuarbeiten. Dieser Artikel gibt einen Überblick über die Grundlagen der Versionskontrolle und ihre Bedeutung in der Entwicklungspraxis. Zudem werden Hinweise auf verschiedene Systeme gegeben, zu denen weiterführende Artikel in Ihrer Dokumentation verlinkt werden können.

---

### **Was ist Versionskontrolle?**

Versionskontrolle (englisch: Version Control) ist ein System, das Änderungen an Dateien oder einem Set von Dateien über die Zeit hinweg aufzeichnet, sodass frühere Versionen wiederhergestellt werden können. Die Hauptziele der Versionskontrolle sind:

1. **Nachvollziehbarkeit:** Nachverfolgung, wer welche Änderungen wann vorgenommen hat.
2. **Wiederherstellbarkeit:** Zurückkehren zu einem früheren Zustand der Dateien, falls ein Fehler auftritt.
3. **Kollaboration:** Ermöglichung paralleler Arbeit an denselben Dateien durch verschiedene Entwickler.

---

### **Warum Versionskontrolle?**

#### **1. Sicherheit:**

- Dateien können durch Fehler, unvorhergesehene Systemabstürze oder Überschreiben verloren gehen. Ein Versionskontrollsystem (VCS) sorgt dafür, dass keine Änderungen verloren gehen.

#### **2. Teamarbeit:**

- VCS ermöglicht es mehreren Entwicklern, gleichzeitig an einem Projekt zu arbeiten, indem Konflikte verwaltet und Änderungen intelligent zusammengeführt werden.

#### **3. Dokumentation:**

- Änderungsprotokolle (Commits) bieten eine Historie der Entwicklung und helfen dabei, zu verstehen, warum bestimmte Entscheidungen getroffen wurden.

#### **4. Flexibilität:**

- Funktionen wie Branching erlauben es, neue Features oder Experimente zu entwickeln, ohne den Hauptcode zu beeinflussen.

---

### **Arten von Versionskontrollsystemen**

#### **1. Lokale Versionskontrollsysteme**

Die frühesten VCS arbeiteten lokal, wobei die Versionshistorie auf einem einzigen Computer gespeichert wurde. Sie bieten Grundfunktionen wie das Speichern und Zurücksetzen von Versionen, aber keine Unterstützung für Teamarbeit.

#### **2. Zentrale Versionskontrollsysteme (Centralized VCS, z.B. SVN, CVS)**

In zentralen Systemen wird die Versionshistorie auf einem Server gespeichert, auf den alle Entwickler zugreifen. Beispiele sind **Subversion (SVN)** und **Concurrent Versions System (CVS)**.

Vorteile:

- Alle Dateien werden an einem zentralen Ort gespeichert.
- Änderungen sind für alle Teammitglieder sofort sichtbar.

Nachteile:

- Ohne Verbindung zum Server ist die Arbeit eingeschränkt.
- Serverausfälle können zu Unterbrechungen führen.

#### **3. Verteilte Versionskontrollsysteme (Distributed VCS, z.B. Git, Mercurial)**

Verteilte Systeme speichern die gesamte Historie sowohl auf einem zentralen Server als auch auf den Computern der Entwickler. Beispiele sind **[Git](Git%20-%20Version%20Control.md)** und **Mercurial**.

Vorteile:

- Offline-Arbeit ist vollständig möglich.
- Redundanz durch mehrere Kopien der Historie.
- Effiziente Branch- und Merge-Funktionen.

Nachteile:

- Einarbeitungszeit kann höher sein, da die Konzepte komplexer sind.

---

### **Populäre Versionskontrollsysteme**

- **[Git](Git%20-%20Version%20Control.md):** Weit verbreitetes verteiltes Versionskontrollsystem, bekannt für seine leistungsstarken Branching- und Merge-Funktionen sowie seine Flexibilität in der Teamarbeit.
- **[Subversion](Subversion.md) (SVN):** Beliebt für Projekte mit klaren hierarchischen Entwicklungsstrukturen.
- **[Concurrent Versions System](Concurrent%20Versions%20System.md) (CVS):** Älter, aber historisch wichtig.
- **[Mercuria](Mercurial.md)l:** Alternative zu Git mit ähnlichen Konzepten, aber weniger verbreitet.
- **[Perforce](Perforce.md):** Besonders in der Spieleentwicklung und großen Unternehmen im Einsatz.

---

### **Vergleich der Systeme**

|**Merkmal**|**CVS**|**SVN**|**Git**|**Mercurial**|**Perforce (Helix Core)**|
|---|---|---|---|---|---|
|**Repository-Typ**|Zentralisiert|Zentralisiert|Dezentralisiert|Dezentralisiert|Zentralisiert|
|**Atomic Commits**|Nicht unterstützt|Unterstützt|Unterstützt|Unterstützt|Unterstützt|
|**Branching**|Grundlegende Unterstützung|Gut|Sehr leistungsstark|Gut, aber weniger populär|Flexibel|
|**Geschwindigkeit**|Langsamer bei großen Projekten|Moderat|Schnell, auch bei großen Projekten|Moderat|Sehr hoch bei großen Projekten|
|**Dateisupport**|Standardmäßig|Standardmäßig|Schwach bei großen Binärdateien|Moderat|Hervorragend für große Binärdateien|
|**Berechtigungen**|Weniger granular|Sehr detailliert|Einschränkungen bei Git selbst (Workarounds möglich)|Weniger granular|Granular und umfassend|
|**Locks**|Unterstützt|Unterstützt|Keine native Unterstützung|Unterstützt|Vollständige Unterstützung|
|**Aktive Entwicklung**|Eingestellt|Aktiv|Aktiv|Aktiv|Aktiv|


---

### **Fazit**

Versionskontrollsysteme sind ein essenzielles Werkzeug für jede Softwareentwicklungsumgebung. Ob zentralisiert oder verteilt, sie bieten die nötigen Werkzeuge, um sicher, effizient und produktiv zu arbeiten. Die Wahl des richtigen Systems hängt von den Anforderungen des Projekts und der Präferenz des Teams ab.

Von hier aus können Sie zu den spezifischen Artikeln der Versionskontrollsysteme springen, um mehr über die jeweiligen Tools und ihre Einsatzmöglichkeiten zu erfahren.
