Assignments
===========

Assignment 1
------------

Vorhandene Betriebssystementwürfe können grob in zwei Klassen eingeteilt werden:

- die Makrokernarchitektur,
- die Mikrokernarchitektur.

Diskutieren Sie beide Architekturansätze unter Zuhilfenahme mindestens folgender Quellen:

- J. Liedtke, Toward real μ-kernels, Communications of the ACM, 39(9):70--77, September 1996 https://citeseerx.ist.psu.edu/pdf/64f7ffba964343a3fc91f870672459b619988d6c
- C. Maeda, B.N. Bershad, Networking performance for microkernels, Proceedings of Third Workshop on Workstation Operating Systems, 13:154 – 159, April 1992 https://citeseerx.ist.psu.edu/pdf/4d5811e818391a007616b1ae881b1738d643e630

Answer
~~~~~~

Assignment 2
------------

Wann ist es sinnvoll, nebenläufige Programmteile mit Hilfe von Threads anstatt Prozessen (heavyweight processes) zu implementieren?

Welche Vorteile bieten User-Level-Threads gegenüber den Kernel-Level-Threads? Gibt es auch Nachteile?

Welche Vorteile und Nachteile gibt es, wenn man Thread-Kontrollblöcke (TCB) als Skalare, in Arrays, Listen, Bäumen oder invertierten Tabellen speichert?

In welchem Adressraum (Prozess-Eigner, Dienste-Prozess, BS-Kern) wird ein TCB gespeichert?

Answer
~~~~~~

Assignment 3
------------

Grenzen Sie die folgenden Begriffe auf Grund der Vorlesung gegeneinander ab:

- gegenseitiger Ausschluss
- Signalisierung
- Synchronisation
- Koordination
- Kommunikation
- Kooperation

Gehen Sie bei Ihrer Diskussion insbesondere auf die Teilnehmer und ihre Beziehung
zueinander ein.

Answer
~~~~~~

Assignment 4
------------

Im Allgemeinen sind an Kommunikationsobjekten Nachrichten unterschiedlicher Länge zugelassen.

1. Welche Auswirkungen hat dies auf die Daten des Kommunikationsobjekts? Bei welchen Varianten der Nachrichtenübergabe hat dies weitere Auswirkungen, und bei welchen hat dies sonst keine weiteren Auswirkungen?
2. Welche Probleme können aus der Sicht der Kommunikationspartner auftreten, wenn Nachrichten unterschiedlicher Länge zugelassen sind? Schlagen Sie geeignete Lösungen vor!

Answer
~~~~~~

Assignment 5
------------

Erläutern Sie die Begriffe:

- memory mapped I/O,
- DMA (direct memory access) und
- polling.

Gegeben sei nun ein Prozessor mit einer Taktfrequenz von 200 MHz. Eine Polling-Operation benötige 400 Taktzyklen. Berechnen Sie die prozentuale CPU-Auslastung durch das Polling für die folgenden Geräte. Bei 2 und 3 ist dabei die Abfragerate so zu wählen, dass keine Daten verloren gehen.

1. Maus mit einer Abfragerate von 30/sec,
2. Diskettenlaufwerk: Datentransfer in 16-bit-Wörtern mit einer Datenrate von 50 KB/sec,
3. Plattengerät, das die Daten in 32-bit-Wörtern mit einer Rate von 2 MB/sec transportiert.

(Hinweis: Wie viele Taktzyklen gibt es pro Sekunde? Wie viele Taktzyklen werden für eine Abtastrate von 30/sec benötigt? Was für einer Abtastrate entsprechen 50 KB/sec bei 16-bit-Wörtern?)

Für das Plattengerät soll jetzt DMA eingesetzt werden. Wir nehmen an, dass für das Initialisieren des DMA 4000 Takte, für eine Interrupt-Behandlung 2000 Takte benötigt werden und dass per DMA 4 KB transportiert werden. Das Plattengerät sei ununterbrochen aktiv. Zugriffskonflikte am Bus zwischen Prozessor und DMA-Steuereinheit werden ignoriert.

Wie hoch ist nun die prozentuale Belastung des Prozessors? (Hinweise: Wie viele DMA-Transfers pro Sekunde sind bei 2 MB/sec und 4 KB Transfergröße notwendig?)

Answer
~~~~~~

Assignment 6
------------

Um die in der Vorlesung beschriebenen Auswahlstrategien der Speicherzuteilung zu implementieren, muss eine Liste der freien Speicherstücke verwaltet werden. Wie lange dauert die durchschnittliche Suche bei den drei beschriebenen Strategien First-Fit, Next-Fit und Best-Fit?

Answer
~~~~~~

Assignment 7
------------

Auf einem PC läuft eine Anwendung zur Wiedergabe von Musik. Die Musikdateien liegen auf der lokalen Festplatte. Die Wiedergabe wird in unregelmäßigen Momenten unterbrochen, sodass der Musikgenuss sehr eingeschränkt ist. Wie gehen Sie zur Problembehebung vor? Begründen Sie kurz die einzelnen Schritte.

Answer
~~~~~~
