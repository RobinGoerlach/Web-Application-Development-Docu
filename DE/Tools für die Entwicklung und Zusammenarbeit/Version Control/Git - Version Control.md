## Einführung – Git als Versionskontrollsystem

Git ist ein verteiltes Versionskontrollsystem (VCS), das Entwicklern hilft, den Quellcode zu verwalten und Änderungen nachzuverfolgen. Es wurde ursprünglich von Linus Torvalds entwickelt, um den Code des Linux-Kernels effizient zu verwalten, und hat sich schnell zum Standardtool in der Softwareentwicklung etabliert. Mit Git können Teams unabhängig voneinander arbeiten und den Code ohne Gefahr von Datenverlust oder Konflikten gemeinsam bearbeiten.

### Ziel und Bedeutung von Git

Das Ziel von Git ist es, Entwicklern eine zuverlässige Methode zur Versionskontrolle zu bieten, die es ihnen ermöglicht, Änderungen an Projekten zu verfolgen, Änderungen rückgängig zu machen und die Arbeit im Team zu organisieren. Mit Git können verschiedene Versionen des Codes erstellt und verwaltet werden, was es zu einem unverzichtbaren Werkzeug in der modernen Softwareentwicklung macht. Es unterstützt sowohl das kollaborative Arbeiten im Team als auch die individuelle Verwaltung von Projekten.

### Grundlegende Konzepte in Git

1. **Repository (Repo)**  
    Ein Repository ist das zentrale Projektverzeichnis, das alle Dateien und Änderungen speichert. Es gibt zwei Haupttypen: **lokale Repositories** (auf deinem Rechner) und **Remote-Repositories** (in der Cloud oder auf einem Server wie GitHub).
    
2. **Branching und Merging**  
    Git ermöglicht es, mehrere Entwicklungszweige (Branches) innerhalb eines Repositories zu erstellen. Der Hauptbranch ist normalerweise der „**main**“- oder „**master**“-Branch. Neben dem Hauptbranch können Entwickler neue Branches für Features, Bugfixes oder Experimente erstellen und diese später wieder zusammenführen (mergen), wenn die Entwicklung abgeschlossen ist.
    
3. **Commit**  
    Ein Commit speichert eine bestimmte Version des Projekts und dokumentiert, was geändert wurde. Jeder Commit hat eine einzigartige ID, die zur Rückverfolgung und Wiederherstellung früherer Versionen dient.
    
4. **Stage**  
    Die Staging-Area in Git ist eine Art Zwischenspeicher, in dem Änderungen vorbereitet werden, bevor sie endgültig durch einen Commit festgehalten werden. Mit dem **add**-Befehl können Änderungen zur Staging-Area hinzugefügt werden.
    
5. **Remote**  
    Ein Remote-Repository ist eine externe Kopie des Projekts, die z. B. auf Plattformen wie GitHub oder GitLab gespeichert ist. Remote-Repositories ermöglichen es, den Code online zu teilen und im Team zu kollaborieren.
    

### Wichtige Git-Befehle

1. **`git init`**  
    Erstellt ein neues lokales Repository in dem aktuellen Verzeichnis.
    
2. **`git clone [URL]`**  
    Erstellt eine Kopie (Klon) eines Remote-Repositories auf dem lokalen Rechner.
    
3. **`git add [Datei]`** oder **`git add .`**  
    Fügt Dateien zur Staging-Area hinzu. Mit **`.`** werden alle geänderten Dateien hinzugefügt.
    
4. **`git commit -m "Nachricht"`**  
    Speichert die Änderungen in der Staging-Area und versieht sie mit einer aussagekräftigen Nachricht.
    
5. **`git status`**  
    Zeigt den Status des Repositories an und listet geänderte Dateien und den Zustand der Staging-Area auf.
    
6. **`git branch`**  
    Listet alle Branches im Repository auf. Mit **`git branch [Branch-Name]`** kann ein neuer Branch erstellt werden.
    
7. **`git checkout [Branch-Name]`**  
    Wechselt zu einem anderen Branch.
    
8. **`git merge [Branch-Name]`**  
    Führt den angegebenen Branch mit dem aktuellen Branch zusammen. Dies wird häufig verwendet, um neue Features in den Hauptbranch zu integrieren.
    
9. **`git pull`**  
    Aktualisiert das lokale Repository mit den neuesten Änderungen vom Remote-Repository.
    
10. **`git push`**  
    Sendet die lokalen Änderungen in das Remote-Repository und aktualisiert dort den Code.
    

### Git-Workflow im Team

Ein typischer Workflow sieht folgendermaßen aus:

1. **Repository klonen**: Ein neues Teammitglied klont das Remote-Repository, um eine Kopie lokal zu erstellen.
2. **Branch erstellen**: Für ein neues Feature oder einen Bugfix wird ein eigener Branch erstellt.
3. **Änderungen hinzufügen und committen**: Nach den Änderungen werden die Dateien zur Staging-Area hinzugefügt und committet.
4. **Änderungen pushen**: Der neue Branch wird zum Remote-Repository hochgeladen, um ihn mit anderen zu teilen.
5. **Merge-Request oder Pull-Request**: Der Entwickler erstellt eine Anfrage zum Zusammenführen, um die Änderungen in den Hauptbranch aufzunehmen.
6. **Code-Review und Zusammenführung**: Die Änderungen werden von einem Teammitglied überprüft und schließlich in den Hauptbranch integriert.

### Best Practices

1. **Aussagekräftige Commit-Nachrichten**: Schreib kurze und prägnante Nachrichten, die den Inhalt der Änderungen beschreiben.
2. **Regelmäßige Commits**: Häufige Commits erleichtern das Nachvollziehen und Rückgängig-Machen von Änderungen.
3. **Branches für spezifische Aufgaben**: Erstelle für jede Funktion oder jeden Bugfix einen eigenen Branch, um die Übersichtlichkeit zu bewahren.
4. **Pull-Requests und Reviews**: Nutze Pull-Requests für die Zusammenarbeit und um sicherzustellen, dass Änderungen geprüft werden, bevor sie in den Hauptbranch kommen.

---

Mit Git lassen sich die Änderungen im Projekt nachvollziehen und eine stabile Basis für die Zusammenarbeit schaffen. Es bildet den Kern des modernen Software-Workflows und sorgt dafür, dass Projekte konsistent, organisiert und für das Team jederzeit nachvollziehbar bleiben.

git clone git@github.com:RobinGoerlach/KW44-Project.git
git config pull.rebase false
git config user.email robin.goerlach@sasd.de
git config user.name "Robin Goerlach"


git push --setupstream feature/hero