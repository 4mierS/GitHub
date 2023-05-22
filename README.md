# GitHub

Ein Repository, in den alle meine Notizen über Git-Kommandos stehen. Quellen aus: Git - Projektverwaltung für Entwickler und DevOps-Teams

**Ich nutze ein Windows 11 Betriebssystem. Die Befehle können auf anderen Betriebssystemen abweichen.**

---

**Inhaltsverzeichnis**

|     |                   |
| :-- | :---------------- |
| 1.  | Terminal          |
| 2.  | Begrifflichkeiten |

|      |                        |
| :--- | :--------------------- |
| 3.   | **Allgemeine Befehle** |
| 3.1. | Verzeichnis            |
|      |                        |
| 3.2. | Klonen                 |
|      |                        |
| 3.3. | Dateien hinzufügen     |
| 3.4. | Commit                 |
| 3.5. | Push                   |
| 3.6. | Pull                   |
| 3.7. | Remote                 |
| 3.8. | Status                 |

|      |                   |
| :--- | :---------------- |
| 4.   | **Branch**        |
| 4.1. | Branches anzeigen |
| 4.2. | Branch erstellen  |
| 4.3. | Branch löschen    |
| 4.4. | Branch wechseln   |

|       |                         |
| :---- | :---------------------- |
| 5.    | **Merge**               |
|       |                         |
| 5.1   | Merge                   |
| 5.1.1 | Fast-forward-Prinzip    |
| 5.1.2 | 3-Way-Prinzip           |
|       |                         |
| 5.2.  | Merge Konflikt          |
| 5.3.  | Merge Abbrechen         |
| 5.4.  | Merge rückgängig machen |

|     |                   |
| :-- | :---------------- |
|     | Zustände/ Objekte |
|     | Commit Undo       |

---

## 1. Terminal

### 1.1. Download Git

Auf einem Windows Betriebssystem muss man das Setup-Programm [downloaden](https://git-scm.com/download) und installieren. In dieser Installation wird nicht nur das Git-Kommando installiert sondern auch das Git Bash.

### 1.2. Terminal

Es gibt verschiedene Terminal um Git zu nutzen. Die bekanntesten sind:

- [Git Bash](https://gitforwindows.org/) ist ein Terminal für Windows. Es ist ein Kommandozeilen-Tool, das auf Unix-ähnlichen Betriebssystemen wie Linux und macOS ausgeführt wird. Es ist ein Tool, das die Verwendung von Git vereinfacht, indem es eine Befehlszeilenschnittstelle (CLI) bereitstellt, die die Verwendung von Git-Befehlen ermöglicht.

- [PowerShell](https://docs.microsoft.com/de-de/powershell/scripting/overview?view=powershell-7.1) ist ein Terminal für Windows. Es ist ein Tool, das die Verwendung von Git vereinfacht, indem es eine Befehlszeilenschnittstelle (CLI) bereitstellt, die die Verwendung von Git-Befehlen ermöglicht. Es ist eine Alternative zu Git Bash. Um PowerShell nutzen zu wollen, muss man das Git-Kommando bereits installiert haben.

- [CMD.exe](https://de.wikipedia.org/wiki/Cmd.exe) (**Nicht empfohlen**) ist ein Kommandozeileninterpreter für Windows. Es ist ein Tool, indem man auch Git nutzen kann, indem es eine Befehlszeilenschnittstelle (CLI) bereitstellt, die die Verwendung von Git-Befehlen ermöglicht. Es ist eine Alternative zu Git Bash.

- [Windows Terminal](https://www.microsoft.com/de-de/p/windows-terminal/9n0dx20hk701?activetab=pivot:overviewtab) ist ein Terminal für Windows. Es ist ein Tool, das die Verwendung von Git vereinfacht, indem es eine Befehlszeilenschnittstelle (CLI) bereitstellt, die die Verwendung von Git-Befehlen ermöglicht. Es ist eine Alternative zu Git Bash.

## 2. Begrifflichkeiten

Branch:

- Ein Branch ist ein Zweig, der von einem Commit abzweigt. Es ist eine Art Kopie des Commits.

Commit:

- Ein Commit ist ein Zustand des Projektes. Es ist eine Art Schnappschuss des Projektes. Es ist ein Objekt, das aus dem Index und dem Verzeichnisbaum besteht.

Repository:

- Ein Repository ist ein Speicherort für ein Projekt. Es ist ein Objekt, das aus dem Verzeichnisbaum besteht.

Remote:

- Ein Remote ist ein entfernter Speicherort für ein Projekt. Es ist ein Objekt, das aus dem Verzeichnisbaum besteht.

Lokal:

- Ein Lokal ist ein lokaler Speicherort für ein Projekt. Es ist ein Objekt, das aus dem Verzeichnisbaum besteht.

Stage-Bereich:

- Der Stage-Bereich ist eine Art Zwischenspeicher. Es ist ein Objekt, das aus dem Index besteht.

Fork:

- Ein Fork ist eine Kopie eines Repositorys. Es ist ein Objekt, das aus dem Verzeichnisbaum besteht.

---

## 3. Allgemeine Befehle

|      | Befehl                             |        |
| :--- | :--------------------------------- | :----- |
| 3.1. | Verzeichnis öffnen                 | cd     |
|      | Inhalt des Verzeichnis             | ls     |
| 3.2. | Repository aud den Rechner ziehen  | clone  |
|      | Repository initialisieren          | init   |
| 3.3. | Datei in Stage-Bereich hinzufügen  | add    |
| 3.4. | Zwischenstand speichern            | commit |
| 3.5. | Zwischenstand auf den Server laden | push   |
| 3.6. | Zwischenstand vom Server laden     | pull   |
| 3.7. | Remote hinzufügen                  | remote |
| 3.8. | Status anzeigen                    | status |

### 3.1. Verzeichnis

- `pwd` (print working directory) zeigt das aktuelle Verzeichnis an.
- `cd` (change directory) wechselt das Verzeichnis.
- `ls` (list) zeigt die Dateien und Verzeichnisse an.

### 3.2. Klonen

1. `git clone <URL>` lädt ein Repository herunter. Es wird ein Verzeichnis erstellt, das den Namen des Repositorys trägt. In diesem Verzeichnis befindet sich das Repository. Man kann mit `git clone <URL> <Verzeichnisname>` dem Repository einen anderen Namen geben.
2. Nach dem klonen muss man mit `cd <Verzeichnisname>` in das Verzeichnis wechseln und initialisieren. Dies macht man mit `git init`.
3. Als nächstes alle Dateien mit `git add .` hinzufügen.

### 3.3. Dateien hinzufügen

- `git add <Dateiname>` fügt eine Datei in den Stage-Bereich hinzu.
- `git add .` fügt alle Dateien in den Stage-Bereich hinzu.

### 3.4. Commit

- `git commit -m "<Nachricht>"` speichert den aktuellen Zustand des Projektes. Die Nachricht ist eine Beschreibung des Zustandes.
  Es kann sein, dass man den Befehel `git commit -a -m "<Nachricht>"` nutzen muss. Dieser Befehl fügt alle Dateien in den Stage-Bereich hinzu und speichert den Zustand.
- `git commit --amend -m "<Nachricht>"` ändert den letzten Commit. Die Nachricht ist eine Beschreibung des Zustandes.

**Hinweis**: Beim erstellen einer neuen Dateien muss immer erst `git add` ausgeführt werden.

### 3.5. Push

- `git push` lädt den aktuellen Zustand des Projektes auf den Server.

### 3.6. Pull

- `git pull` lädt den aktuellen Zustand des Projektes vom Server.
- `git pull` ist eine Kombination aus `git fetch` und `git merge`.

### 3.7. Remote

- `git remote add <Name> <URL>` fügt einen Remote hinzu. Der Name ist der Name des Remotes. Die URL ist die URL des Remotes.
- `git remote -v` zeigt alle Remotes an.

### 3.8. Status

- `git status` zeigt den Status des Projektes an.

## 4 Branches

### 4.1. Branch anzeigen

- `git branch` zeigt alle Branches an.

### 4.2. Branch erstellen

- `git branch <Name>` erstellt einen Branch.

### 4.3. Branch löschen

- `git branch -d <Name>` löscht einen Branch.

### 4.4. Branch wechseln

- `git checkout <Name>` wechselt den Branch.

**Tipp**: Mit `git checkout -b <Name>` kann man einen Branch erstellen und wechseln.

### Binärdateien

- Binärdateien sind Dateien, die nicht aus Text bestehen. Beispiele sind Bilder, Videos, Audiodateien, etc.
- Binärdateien können nicht mit `git diff` verglichen werden.
- Binärdateien können nicht mit `git merge` zusammengeführt werden. Es kann zu Konflikten kommen. Daher kann man mit dem Befehl `git checkout --theirs --<Binärdatei>` oder `git checkout --ours <Binärdatei>` auswählen, welche Datei behalten werden soll.
  Somit kann man dann mit `git add <Binärdatei>` die Datei in den Stage-Bereich hinzufügen und mit `git commit -m "<Nachricht>"` den Zustand speichern.

---

## 5. Merge

### 5.1. Merge

- `git merge <Name>` fügt den Branch in den aktuellen Branch ein.

---

![Git](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e0/Git-logo.svg/1280px-Git-logo.svg.png)
