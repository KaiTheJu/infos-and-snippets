# Arbeit mit Git

`Git` ist ein leistungsfähiges Versionskontroll-System, welches besonders gut beim Programmieren eingesetzt werden kann.
Gerade bei Zusammenarbeit von mehreren ProgrammiererInnen ist ein Versionskontroll-System unabdingbar, da so mehrere Personen
unabhängig am gleichen Projekt arbeiten können. Es bietet aber auch für einzelne ProgrammiererInnen viele Vorteile. 
Zum Beispiel lassen sich Änderungen an den Teilen des Projekts schnell inspizieren, modifizieren oder rückgängig machen.
Ausserdem kann an verschiedenen Projekt-Features unabhängig gearbeitet werden.

Jedes Programmierprojekt wird in einem `Repository` abgelegt. Dies ist ein virtueller Speicher, welches aus der Kollektion 
der Dateien des Projekts und Metadata zur Versionskontrolle besteht. Jede substanzielle Code-Änderung 
wird in einem `Commit` zur Projekt-Geschichte hinzugefügt und mit einer Überschrift betitelt.
`Github` ist ein internet-basierter Dienst zum Einsatz von `Git`. Beginnt man `Github` zu verwenden, sind einige Konfigurationsschritte nötig,
die im folgenden [Video](https://www.youtube.com/watch?v=kHkQnuYzwoo) erklärt werden. Eine weitere empfehlenswerte Einstellung lautet:
```
git config --global pull.rebase true
```
## Projekt-Geschichte

Die Projekt-Geschichte lässt sich mittels 
```
git log
```
anzeigen. Zum Beispiel sieht die Projekt-Geschichte zum infos-and-snippets Repository momentan wie folgt aus:

![grafik](https://user-images.githubusercontent.com/40485433/131213722-0036b625-5480-4bc8-9c74-214081c4cc6d.png)

Es ist daraus also ersichtlich, wer wann welche Commits gemacht hat und was damit bezweckt werden sollte.

## Aktueller Zustand

Der aktuelle Zustand des Git Repositories lässt sich mittels
```
git log
```
anzeigen. Hier wird ersichtlich, ob es geänderte Dateien gibt, ob diese bereits für einen neuen Commit vorgemerkt sind (grün statt rot) und ob gerade ein
"Merge" oder "Rebase" Prozess zur Zusammenführung von Dateien im Gange ist. Ausserdem wird der aktuelle Branch (Zweig) angezeigt, auf welchem gearbeitet wird.

Zum Beispiel zeigt:
```
Auf Branch main
Ihr Branch ist auf demselben Stand wie 'origin/main'.

Änderungen, die nicht zum Commit vorgemerkt sind:
  (benutzen Sie "git add <Datei>...", um die Änderungen zum Commit vorzumerken)
  (benutzen Sie "git restore <Datei>...", um die Änderungen im Arbeitsverzeichnis zu verwerfen)
	geändert:       snippets/loops.py

Unversionierte Dateien:
  (benutzen Sie "git add <Datei>...", um die Änderungen zum Commit vorzumerken)
	other/

keine Änderungen zum Commit vorgemerkt (benutzen Sie "git add" und/oder "git commit -a")
```
an, dass auf dem Hauptzweig `main` gearbeitet wird und dass es eine geänderte Datei `snippets/loops.py` gibt, die mittels `git add snippets/loops.py` 
für einen Commit vorgemerkt werden kann. Auch das Verzeichnis `other/` ist neu und kann hinzugefügt werden.

## Klonen von Repositories

Um ein Repository vom Online-Dienst Github zu klonen, verwendet man den Befehl `git clone`. Bei fremden Repositories empfiehlt sich, diese zuerst 
mittels `Fork` abzuzweigen, so dass man die abgezweigte Variante nicht nur lokal, sondern auch auf Github verändern kann. Ohne Abzweigung 
fehlt die Berechtigung dazu. 

Um etwa das `info-and-snippets` repository zu klonen, gehst du auf [https://github.com/KS-Limmattal/infos-and-snippets](https://github.com/KS-Limmattal/infos-and-snippets)
und klickst rechts oben auf `Fork`. 
Dann tippe im gewünschten Verzeichnis in der Konsole, in welcher du `git` ausführen kannst:
```
git clone https://github.com/KS-Limmattal/infos-and-snippets.git
```
