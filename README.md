# Lukas Heel

## About Me

Ich studiere Informatik an der Universität Innsbruck und interessiere mich vor allem für sauberen und dokumentierten Code, Algorithmen, Datenstrukturen und mathematische Grundlagen in der Programmierung.

Aktuell arbeite ich hauptsächlich mit Java und C. In Java beschäftige ich mich vor allem mit objektorientiertem Design, Projektstruktur und Testing. In C interessiert mich besonders, wie Speicherverwaltung, Pointer, Threads, Synchronisation und systemnahe Grundlagen praktisch funktionieren.

Mir ist wichtig, nicht nur Code zu schreiben, der irgendwie läuft, sondern nachvollziehbare Lösungen zu bauen: verständliche Struktur, klare Verantwortlichkeiten und Tests, die zeigen, dass die Logik auch in Randfällen funktioniert.

Außerdem habe ich solide Grundlagen in Haskell und Julia. Haskell hilft mir dabei, funktionale Konzepte besser zu verstehen. Julia lerne ich aktuell im Studium und möchte die Sprache später auch für numerische und mathematische Projekte einsetzen.

Meine aktuellen Projekte sind hauptsächlich Lernprojekte, mit denen ich gezielt verschiedene Bereiche vertiefe: Scheduling und Testing in Java mit ExamFlow, Speicherverwaltung in C mit meinem eigenen Memory Allocator und Multithreading sowie Dateiabhängigkeiten mit C_Forge.

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
- JUnit-Tests für Blockdauer, Gesamtlernzeit und Scheduling-Verhalten

Der Fokus liegt für mich hier vor allem auf sauberem Java-Code, objektorientierter Struktur, nachvollziehbarer Logik und Testing. Gerade bei ExamFlow versuche ich, die einzelnen Teile so zu strukturieren, dass sie später gut erweiterbar und testbar bleiben.

---

### my_memory_allocator (C)

`my_memory_allocator` ist ein eigener Speicherallokator in C, der auf `sbrk` basiert. Das Projekt stellt eigene Implementierungen von `malloc`, `calloc`, `realloc` und `free` bereit.

Das Ziel des Projekts ist es, besser zu verstehen, wie dynamische Speicherverwaltung intern funktioniert. Dabei geht es unter anderem darum, Speicherblöcke zu verwalten, freien Speicher wiederzuverwenden und darauf zu achten, dass keine ungültigen Speicherzugriffe entstehen.

Fokusbereiche:

- Heap-Speicher und `sbrk`
- eigene Implementierungen von `malloc`, `calloc`, `realloc` und `free`
- Verwaltung von Speicherblöcken
- Pointer und Pointer-Arithmetik
- Wiederverwendung von freigegebenem Speicher
- Vermeidung von Speicherlecks und Undefined Behavior

Der Memory Allocator ist vor allem ein Lernprojekt, um die Abläufe hinter der normalen Speicherverwaltung besser nachvollziehen zu können.

---

### C_Forge (C)

C_Forge soll später eine vereinfachte Version von `make` werden. Das Ziel ist es, Abhängigkeiten zwischen Dateien zu verwalten und nur die Teile eines Projekts neu auszuführen, die sich seit dem letzten Durchlauf verändert haben.

Aktuell können Dateien als sogenannte Prerequisites registriert werden. Beim Hinzufügen einer Datei wird eine CRC-32-Prüfsumme berechnet und gespeichert. Bei einer späteren Überprüfung wird die Prüfsumme erneut berechnet und mit dem gespeicherten Wert verglichen. Dadurch kann erkannt werden, ob sich der Inhalt einer Datei verändert hat.

Die Überprüfung kann mit einem einzelnen Thread oder mit mehreren Threads ausgeführt werden. Wenn mehrere Threads verfügbar sind, werden die Dateien aufgeteilt und parallel überprüft. Der gemeinsame Speicher wird dabei mit einem Mutex geschützt.

Was aktuell enthalten ist:

- Verwaltung von Prerequisites
- Berechnung von CRC-32-Prüfsummen
- Vergleich von gespeicherten und aktuellen Prüfsummen
- Erkennung von veränderten Dateien
- Verarbeitung mit einem oder mehreren Threads
- Synchronisation mit POSIX-Mutexen
- Fehlerbehandlung über Rückgabewerte
- Aufteilung des Projekts in mehrere Module

Später sollen unter anderem Targets, Abhängigkeitsketten, Konfigurationsdateien und auszuführende Build-Befehle hinzukommen. Außerdem möchte ich Tests für die einzelnen Funktionen, Fehlerfälle und die parallele Verarbeitung ergänzen.

Der Fokus liegt für mich bei diesem Projekt vor allem auf Multithreading, Synchronisation, Dateiverarbeitung und dem Aufbau eines größeren Programms in C.

---

## Tech Stack

### Languages

![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Haskell](https://img.shields.io/badge/Haskell-5D4F85?style=for-the-badge&logo=haskell&logoColor=white)
![Julia](https://img.shields.io/badge/Julia-9558B2?style=for-the-badge&logo=julia&logoColor=white)

### Tools / Environment

![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Bash](https://img.shields.io/badge/Bash-121011?style=for-the-badge&logo=gnu-bash&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GCC](https://img.shields.io/badge/GCC-663399?style=for-the-badge&logo=gnu&logoColor=white)
![IntelliJ IDEA](https://img.shields.io/badge/IntelliJ-000000?style=for-the-badge&logo=intellij-idea&logoColor=white)
![VS Code](https://img.shields.io/badge/VSCode-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white)

---

## Interests

- sauberer und dokumentierter Code
- Algorithmen und Datenstrukturen
- mathematische Grundlagen in der Programmierung
- Low-Level-Programmierung
- Speicherverwaltung
- Pointer und dynamische Datenstrukturen
- Betriebssystemgrundlagen
- Multithreading und Synchronisation
- C und systemnahe Programmierung
- Java, objektorientiertes Design und Testing
- numerische Simulationen

---

Aktuell suche ich nach Praktikums- oder Werkstudentenstellen im Bereich Softwareentwicklung.

---

## Contact

- Email: [lukas.heel@outlook.at](mailto:lukas.heel@outlook.at)
- GitHub: [https://github.com/Lugmaner](https://github.com/Lugmaner)
- LinkedIn: https://linkedin.com/in/lukas-heel
