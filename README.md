# Workshop: Einführung in Git für Azubis

Di 21. bis Do 23. Mai 2024
mit Clemens, Jacob, Jonas, Tim

 
## Teil 1: Was ist Git?

### 1.1 Einführung in Versionskontrolle

-   Definition von Versionskontrolle:
    -   System zur Verwaltung von Änderungen an Dokumenten, Code oder anderen Dateien über die Zeit hinweg.
-   Warum ist Versionskontrolle wichtig?
    -   Verfolgung von Änderungen: Wer hat was, wann und warum geändert?
    -   Rückverfolgbarkeit: Ermöglicht das Zurückkehren zu früheren Versionen.
    -   Zusammenarbeit: Erlaubt es mehreren Personen, gleichzeitig an einem Projekt zu arbeiten, ohne dass ihre Änderungen einander überschreiben.

### 1.2 Was ist Git?

-   Geschichte von Git:
    -   Entwickelt von Linus Torvalds 2005 für die Verwaltung des Linux-Kernel-Codes.
    -   Entworfen, um schnell, effizient und skalierbar zu sein.
-   Konzept und Funktionsweise von Git:
    -   Dezentrales Versionskontrollsystem: Jeder Benutzer hat eine vollständige Kopie des Repositories.
    -   Snapshots: Speichert Zustände des Projekts zu verschiedenen Zeitpunkten.
    -   Branching: Ermöglicht das parallele Entwickeln von Features und das spätere Zusammenführen.
-   Unterschiede zwischen Git und anderen Versionskontrollsystemen:
    -   Unterscheidet sich stark von zentralisierten Systemen wie SVN durch sein dezentrales Modell.
    -   Verwendung von Hashes zur Identifizierung von Commits statt sequenziellen Versionsnummern.

### 1.3 Was Git nicht ist

-   Missverständnisse über Git klären:
    -   Git ist kein Dateispeicher, sondern ein Werkzeug zur Verwaltung von Dateiänderungen.
    -   Es ist nicht nur für Entwickler: Git kann für jede Art von Datei verwendet werden, nicht nur für Code.
-   Gemeinsame Irrtümer vermeiden:
    -   Git ist nicht dasselbe wie GitHub: GitHub ist eine Plattform für die Zusammenarbeit mit Git-Repositories, aber Git selbst ist unabhängig davon nutzbar.
    -   Git ist nicht nur für Teams: Auch Einzelpersonen können von den Vorteilen der Versionskontrolle profitieren.

## Teil 2: Einrichten von Git

### 2.1 Installation von Git

-   Herunterladen von Git:
    -   Offizielle Website besuchen (https://git-scm.com/) oder Paketmanager verwenden (z. B. apt, yum, Homebrew).
-   Installation auf verschiedenen Betriebssystemen:
    -   Windows: Ausführbares Installationsprogramm herunterladen und ausführen.
    -   macOS: Installation über Homebrew, Installer oder Xcode Command Line Tools.
    -   Linux: Installation über Paketmanager (z. B. apt für Ubuntu, yum für Fedora).

### 2.2 Konfiguration von Git

-   Konfigurieren von Benutzername und E-Mail-Adresse:
    -   `git config --global user.name "Your Name"`
    -   `git config --global user.email "your.email@example.com"`
-   Konfigurieren von Standardeditoren und anderen Optionen:
    -   `git config --global core.editor "editor-name"`
    -   Weitere Optionen: z. B. Farbunterstützung, Verhalten bei Konflikten.
-   Überprüfen der Git-Konfiguration:
    -   `git config --list`: Zeigt alle globalen Einstellungen an.
    -   `git config <key>`: Zeigt den Wert einer bestimmten Konfigurationsoption an.

### 2.3 Erste Schritte mit Git

-   Initialisierung eines Git-Repositories:
    -   `git init`: Startet ein neues Git-Repository im aktuellen Verzeichnis.
-   Clonen eines vorhandenen Repositories:
    -   `git clone <repository-url>`: Lädt ein Remote-Repository herunter und erstellt eine lokale Kopie.
-   Überprüfen des Status und Hinzufügen von Dateien zum Index:
    -   `git status`: Zeigt den Status des Arbeitsverzeichnisses und des Staging-Bereichs an.
    -   `git add <file>`: Fügt eine Datei zum Staging-Bereich hinzu, um sie für den nächsten Commit vorzubereiten.

### 2.4 GitHub

-   GitHub als Plattform für kollaboratives Arbeiten:
    -   GitHub ist eine Webplattform, auf der du Git-Repositories hosten kannst und die Funktionen für Zusammenarbeit, Code-Überprüfung und Projektmanagement bietet.
    -   Hier kannst du gemeinsam mit anderen an Projekten arbeiten, Code überprüfen und Probleme verwalten.

#### Anmeldung bei GitHub

-   Erstelle einen Account bei GitHub:
    -   Gehe zu [GitHub](https://github.com/) und folge den Anweisungen, um einen neuen Account zu erstellen.
-   Verknüpfe dein lokales Git-Repository mit GitHub:
    -   Nach der Anmeldung kannst du deine Git-Repositories auf GitHub hochladen, um sie mit anderen zu teilen und von den Kollaborationsfunktionen zu profitieren.
-   Künftige Arbeit mit GitHub:
    -   Nutze GitHub, um deine Projekte zu hosten, mit anderen zusammenzuarbeiten und von der breiten Palette an Tools und Diensten zu profitieren, die die Plattform bietet.

Die Anmeldung bei GitHub eröffnet dir Möglichkeiten zur Zusammenarbeit und zum Austausch von Code mit anderen Entwicklern weltweit.

## Teil 3: Grundlegende Git-Befehle

### 3.1 Lokale Änderungen verfolgen

-   Hinzufügen von Dateien zum Commit:
    -   `git add <file>`: Fügt eine bestimmte Datei zum Staging-Bereich hinzu.
    -   `git add .`: Fügt alle geänderten Dateien im Arbeitsverzeichnis zum Staging-Bereich hinzu.
-   Committing von Änderungen:
    -   `git commit -m "Commit message"`: Speichert alle im Staging-Bereich befindlichen Änderungen in einem neuen Commit.
-   Überprüfen des Commit-Verlaufs:
    -   `git log`: Zeigt eine chronologische Liste aller Commits im Repository an.
    -   `git log --oneline`: Zeigt eine kompakte Liste der Commit-Nachrichten an.

### 3.2 Zusammenarbeit mit Remote-Repositories

-   Verbindung zu einem Remote-Repository herstellen:
    -   `git remote add origin <repository-url>`: Verknüpft das lokale Repository mit einem Remote-Repository.
-   Pushen von Commits auf ein Remote-Repository:
    -   `git push origin <branch-name>`: Überträgt lokale Commits auf den angegebenen Remote-Branch.
-   Pullen von Änderungen aus einem Remote-Repository:
    -   `git pull origin <branch-name>`: Aktualisiert das lokale Repository mit den neuesten Änderungen aus dem Remote-Repository.

### 3.3 Branching und Merging

-   Erstellen und Wechseln zwischen Branches:
    -   `git branch <branch-name>`: Erstellt einen neuen Branch.
    -   `git checkout <branch-name>`: Wechselt zum angegebenen Branch.
-   Zusammenführen von Branches:
    -   `git merge <branch-name>`: Führt die Änderungen aus einem anderen Branch in den aktuellen Branch zusammen.
-   Auflösen von Merge-Konflikten:
    -   Bei Konflikten müssen die Dateien manuell bearbeitet werden, um die Konflikte aufzulösen.
    -   Anschließend wird der Commit abgeschlossen, um den Merge abzuschließen.

## Teil 4: Best Practices und Tipps

### 4.1 Verwendung von Branches

-   Sinnvolle Nutzung von Branches:
    -   Verwende Branches, um neue Features zu entwickeln, Bugfixes vorzunehmen oder Experimente durchzuführen.
    -   Halte Branches klein und fokussiert, um Konflikte und Probleme zu minimieren.
-   Benennungskonventionen für Branches:
    -   Verwende aussagekräftige Namen, die den Zweck des Branches beschreiben.
    -   Gängige Konventionen umfassen Feature-Branches (z. B. `feature/new-login-page`) oder Bugfix-Branches (z. B. `bugfix/fix-404-error`).

### 4.2 Commit-Best Practices

-   Klare und aussagekräftige Commit-Nachrichten schreiben:
    -   Beschreibe präzise, welche Änderungen der Commit enthält und warum sie vorgenommen wurden.
    -   Verwende eine aktive Sprache und einen imperativen Stil (z. B. "Add feature" statt "Added feature").
-   Aufteilen von Änderungen in kleinere, zusammenhängende Commits:
    -   Teile große Änderungen in kleinere, logische Schritte auf, um die Nachvollziehbarkeit und Zusammenarbeit zu verbessern.
    -   Vermeide das Hinzufügen von nicht verwandten Änderungen in einem einzigen Commit.

### 4.3 Arbeiten mit Remote-Repositories

-   Häufiges Pushen von Commits:
    -   Lade regelmäßig Commits auf das Remote-Repository hoch, um den Fortschritt zu sichern und mit anderen zu teilen.
    -   Vermeide lange Phasen ohne Pushes, um Datenverluste zu vermeiden.
-   Beachten von Änderungen im Remote-Repository vor dem Pushen:
    -   Überprüfe vor dem Pushen, ob es im Remote-Repository Änderungen gibt, die mit den lokalen Commits in Konflikt stehen könnten.
    -   Löse eventuelle Konflikte lokal, bevor du deine Änderungen pushst.

### 4.4 Behandlung von Merge-Konflikten

-   Strategien zur Konfliktlösung:
    -   Analysiere die Konflikte und verstehe die Ursachen, bevor du mit der Lösung beginnst.
    -   Kommuniziere mit anderen Teammitgliedern, um Konflikte gemeinsam zu lösen.
-   Vermeidung von Merge-Konflikten durch regelmäßiges Zusammenführen von Branches:
    -   Integriere Änderungen aus dem Haupt-Branch regelmäßig in Feature-Branches, um Konflikte frühzeitig zu erkennen und zu lösen.
    -   Vermeide lange Phasen isolierter Entwicklung, um die Wahrscheinlichkeit von Konflikten zu reduzieren.

## 5. Abschluss und Ausblick

### 5.1 Zusammenfassung

-   Wichtige Punkte des Workshops nochmals hervorheben:
    -   Versionskontrolle und ihre Bedeutung verstehen.
    -   Git als dezentrales Versionskontrollsystem kennenlernen.
    -   Grundlegende Git-Befehle für die tägliche Arbeit erlernen.
    -   Best Practices für effektive Zusammenarbeit und Konfliktlösung kennenlernen.

### 5.2 Nächste Schritte

-   Ressourcen und weiterführende Informationen für die Teilnehmer bereitstellen:
    -   Cheatsheets und Referenzmaterialien für Git-Befehle und Workflows.
    -   Übungsaufgaben und Projekte zum praktischen Anwenden des Gelernten.
    -   Online-Kurse und Tutorials für fortgeschrittenere Git-Konzepte und -Techniken.

### Nützliche Links

-   Git Cheatsheet:
    -   [Git Cheatsheet von GitHub](https://education.github.com/git-cheat-sheet-education.pdf)
-   Interaktive Git-Tutorials:
    -   [Git Immersion](https://gitimmersion.com/)
    -   Learn Git Branching
-   Übungsaufgaben und Projekte:
    -   [GitHub Learning Lab](https://lab.github.com/)
    -   Git Exercises
-   Weiterführende Ressourcen:
    -   [Pro Git Buch](https://git-scm.com/book/en/v2)
    -   Atlassian Git Tutorials
