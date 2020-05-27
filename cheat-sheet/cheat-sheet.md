Cheat-Sheet
===========

Voraussetzungen
---------------

### 0890

Meld installieren

```
$ sudo apt-get install meld
```

### 0900

Gitg installieren

```
$ sudo apt-get install gitg
```

### 0910

Lokaler Clone - URL kommt von oben rechts!

```
$ git clone git@github.com:(deinFork)/git-rebase-training-advanced.git
```

Ablauf
------

### Vorbereitungen

#### 1010

Stelle sicher, dass alle Änderungen am zentralen Repo bei Dir lokal verfügbar sind!

```
$ git fetch --all -p
Fordere an von origin
```

#### 1020

Visualisiere die Situation

```
$ gitg master origin/master experiment origin/experiment
```

![images/start.png](../images/start.png)

### Durchführung

#### 1110

Branch "experiment" auschecken

```
$ git checkout experiment
```

#### 1120

Branch "experiment" aktualisieren

```
$ git pull --rebase
```

#### 1130

Rebase durchführen

```
$ git rebase master
```

#### 1140

Sichten

```
$ gitg master experiment
$ git status
```

#### 1150

Ergebnis "veröffentlichen"

```
$ git push ...
```

Nachkontrolle
-------------

#### 1210

Visualisiere die Situation

```
$ gitg master origin/master experiment origin/experiment
```

