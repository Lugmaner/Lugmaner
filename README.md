# Lukas Heel

## About Me

Ich studiere Informatik an der Universität Innsbruck und interessiere mich vor allem für sauberen, gut getesteten Code, Algorithmen, Datenstrukturen und mathematische Grundlagen in der Programmierung.

Mich interessiert besonders, wie Software unter der Oberfläche funktioniert: Speicherverwaltung, Betriebssystemgrundlagen, einfache Systemnähe und generell die Frage, warum ein Programm nicht nur läuft, sondern korrekt und nachvollziehbar aufgebaut ist.

Aktuell arbeite ich vor allem mit Java und C. In beiden Sprachen fühle ich mich gut bis sehr gut zurecht, wobei Java bei mir aktuell stärker in Richtung objektorientiertes Design und Testing geht, während C für mich vor allem spannend ist, um Speicher, Datenstrukturen und low-level Grundlagen besser zu verstehen.

Außerdem habe ich solide Grundlagen in Haskell und Julia. Haskell hilft mir dabei, funktionale Konzepte besser zu verstehen, und Julia lerne ich gerade im Studium. Langfristig möchte ich Julia auch für numerische Projekte einsetzen, zum Beispiel für eine überarbeitete Version meiner Rocket Flight Simulation.

---

## Projects

### ExamFlow (Java)

ExamFlow ist ein Java-Projekt, mit dem automatisch Lernblöcke für Prüfungen geplant werden sollen. Die Grundidee ist, dass Prüfungen, Deadlines, Lernaufwand und bereits belegte Zeitfenster berücksichtigt werden und daraus ein realistischer Lernplan entsteht.

Der aktuelle Kern ist ein `GreedyScheduler`, der Prüfungen nach Deadline sortiert und versucht, passende Lernblöcke vor dem jeweiligen Prüfungstermin einzuplanen. Dabei werden fixe Termine, Tagesgrenzen, Session-Länge und Pausen berücksichtigt. Wenn keine gültige Planung möglich ist, wird eine eigene Exception geworfen.

Was aktuell enthalten ist:

- `GreedyScheduler` als konkrete Implementierung einer Scheduling-Strategie
- Modelle wie `Exam`, `StudyBlock`, `TimeSlot` und `FixedAppointment`
- Interfaces wie `SchedulingStrategy` und `Schedulable`
- eigene Fehlerbehandlung mit `FailedToScheduleExamException`
- erste Struktur für CLI und Export
- JUnit-Tests für Blockdauer, Gesamtlernzeit und Scheduling-Verhalten

Der Fokus liegt für mich hier vor allem auf sauberem Java-Code, objektorientierter Struktur, nachvollziehbarer Logik und Testing. Gerade bei ExamFlow versuche ich, nicht nur „irgendwie“ eine Lösung zu bauen, sondern die einzelnen Teile so zu strukturieren, dass sie später gut erweiterbar und testbar bleiben.

---

### Rocket Flight Simulation (C, später eventuell Julia)

Die Rocket Flight Simulation ist ein kleines physikbasiertes Simulationsprojekt in C. Es geht um einen vertikalen Raketenflug mit Schub, Gravitation, Luftwiderstand, Treibstoffverbrauch und einem einfachen Atmosphärenmodell.

Das Projekt ist für mich vor allem interessant, weil hier Mathematik, Physik und Programmierung direkt zusammenkommen. Die Simulation arbeitet zeitdiskret und berechnet Schritt für Schritt Werte wie Geschwindigkeit, Höhe, Masse, Luftdichte und Widerstand.

Langfristig möchte ich das Projekt eventuell in Julia neu oder erweitert umsetzen. Julia lerne ich gerade im Studium, und ich möchte die Sprache später gezielt für numerische Simulationen und mathematischere Projekte verwenden.

---

### Password Manager (C, gemeinsam mit einem Kollegen)

Der Password Manager ist ein Übungsprojekt in C, das ich gemeinsam mit einem Kollegen angefangen habe. Das Projekt ist nicht für echten produktiven Einsatz gedacht und verwendet keine sichere Verschlüsselung. Der Zweck war eher, mehr praktische Erfahrung mit C zu sammeln.

Mein Fokus lag dabei auf der internen Struktur, dynamischen Datenstrukturen und sauberem Speicher-Management. Besonders wichtig war für mich, klarer zu verstehen, wem Speicher gehört, wann etwas freigegeben werden muss und wie man typische Fehler in C vermeidet.

Mein Teil:

- `database.c / database.h`
- `entry.c / entry.h`

Fokusbereiche:

- Heap-Speicher
- dynamische Datenstrukturen
- klare Speicher-Ownership
- sauberes Freigeben von Speicher
- Vermeidung von Undefined Behavior

---

## Tech Stack

### Languages

![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Haskell](https://img.shields.io/badge/Haskell-5D4F85?style=for-the-badge&logo=haskell&logoColor=white)
![Julia](https://img.shields.io/badge/Julia-9558B2?style=for-the-badge&logo=julia&logoColor=white)

### Tools / Environment

![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Bash](https://img.shields.io/badge/Bash-121011?style=for-the-badge&logo=gnu-bash&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![IntelliJ IDEA](https://img.shields.io/badge/IntelliJ-000000?style=for-the-badge&logo=intellij-idea&logoColor=white)
![VS Code](https://img.shields.io/badge/VSCode-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white)

---

## Interests

- sauberer und gut getesteter Code
- Algorithmen und Datenstrukturen
- mathematische Grundlagen in der Programmierung
- low-level Programmierung
- Speicherverwaltung
- Betriebssystemgrundlagen
- C und systemnahe Programmierung
- Java, objektorientiertes Design und Testing
- numerische Simulationen
- Julia für mathematische und technische Anwendungen

---

## Contact

- Email: [lukas.heel@outlook.at](mailto:lukas.heel@outlook.at)
- GitHub: [https://github.com/Lugmaner](https://github.com/Lugmaner)
