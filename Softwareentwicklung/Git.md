**Git** ist ein verteiltes [[Versionskontrolle|Versionskontrollsystem]], das in der Softwareentwicklung verwendet wird, um Änderungen an Quellcode und anderen Dateien zu verfolgen. Es ermöglicht es mehreren Entwicklern, gleichzeitig an einem Projekt zu arbeiten, Änderungen nachzuverfolgen und gegebenenfalls zu einer früheren Version zurückzukehren. Git ist äußerst populär und wird von vielen Entwicklern und Teams weltweit verwendet.

# Wozu wird Git verwendet?
- **Versionskontrolle**: Git speichert und verfolgt alle Änderungen an Dateien und ermöglicht es, zu einer früheren Version zurückzukehren, wenn Fehler auftreten.
- **Zusammenarbeit**: Git erlaubt es mehreren Entwicklern, parallel an einem Projekt zu arbeiten, ohne dass sich ihre Änderungen gegenseitig überschreiben.
- **Backup**: Mit Git werden Änderungen sicher in einem Repository (lokal und/oder auf einem entfernten Server wie GitHub) gespeichert, sodass ein Verlust von Daten unwahrscheinlicher wird.

# Grundlegende Konzepte
## 1. Repository (Repo)
Ein **Repository** ist eine Sammlung von Dateien und Verzeichnissen, deren Änderungen Git überwacht. Ein Repository kann lokal auf einem Computer oder auf einem entfernten Server wie GitHub oder GitLab gespeichert werden.
## 2. Commit
Ein **Commit** stellt eine Änderung oder eine Gruppe von Änderungen im Repository dar. Jeder Commit wird mit einer eindeutigen ID (Hash) versehen und enthält eine Beschreibung der vorgenommenen Änderungen sowie den Autor der Änderung.
## 3. Branch
Ein **Branch** ist ein separater Entwicklungszweig innerhalb eines Repositories. Die Arbeit an einem Branch beeinflusst nicht den Hauptzweig (häufig **main** oder **master** genannt), bis die Änderungen zusammengeführt werden (siehe **Merge**). Dies ermöglicht das parallele Arbeiten an verschiedenen Features oder Bugfixes.
## 4. Merge
Das **Mergen** ist der Vorgang, bei dem Änderungen aus einem Branch in einen anderen zusammengeführt werden. Beim Merge kann es zu Konflikten kommen, wenn die gleichen Zeilen in einer Datei in beiden Branches geändert wurden, die manuell gelöst werden müssen.
## 5. Clone
Mit **Clone** wird ein Repository von einem entfernten Server auf den lokalen Rechner kopiert. So kann ein Entwickler das Projekt lokal bearbeiten und Änderungen später wieder hochladen.

# Grundlegende Git-Befehle

## 1. `git init`
Initialisiert ein neues lokales Git-Repository.

```bash
git init
```
### 2. `git clone`
Kopiert ein bestehendes Remote-Repository auf den lokalen Computer.

```bash
git clone https://github.com/user/repo.git
```
## 3. `git add`
Fügt neue oder geänderte Dateien zur "Staging Area" hinzu, um sie für den nächsten Commit vorzubereiten.

```bash
git add <dateiname>
```
## 4. `git commit`
Speichert die Änderungen, die sich in der Staging Area befinden, dauerhaft im Repository.

```bash
git commit -m "Beschreibung der Änderung"
```
## 5. `git status`
Zeigt den aktuellen Zustand des Repositories, welche Dateien geändert wurden und welche noch nicht committet wurden.

```bash
git status
```
## 6. `git pull`
Holt die neuesten Änderungen von einem Remote-Repository und integriert sie in das lokale Repository.

```bash
git pull
```
## 7. `git push`
Überträgt lokale Commits in ein Remote-Repository, z. B. auf GitHub

```bash
git push
```

# Branching und Merging
## 1. Branch erstellen
Ein neuer Branch kann mit dem Befehl `git branch` erstellt werden. Dadurch wird ein separater Entwicklungszweig erstellt.

```bash
git branch feature-xyz
```
## 2. Branch wechseln
Mit `git checkout` kann man auf einen anderen Branch wechseln, um dort Änderungen vorzunehmen.

```bash
git checkout feature-xyz
```
## 3. Branch zusammenführen (Merge)
Um die Änderungen eines Branches in einen anderen zu integrieren, wird der Befehl `git merge` verwendet.

```bash
git merge feature-xyz
```

# Remote-Repositories
Git erlaubt die Zusammenarbeit an einem Projekt über entfernte Repositories. GitHub, GitLab und Bitbucket sind Plattformen, die Git-Repositories hosten und Tools zur Zusammenarbeit anbieten.
- **Pull Requests**: Ein Pull Request wird verwendet, um Änderungen vorzuschlagen, die dann von anderen Teammitgliedern überprüft und in den Hauptzweig integriert werden.
- **Issues**: GitHub und GitLab bieten auch Funktionen zum Verwalten von Aufgaben, Bug Reports und Feature-Anfragen.
