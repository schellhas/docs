Exam
====

Aufgabe 1 (Architektur, 8 Punkte)
---------------------------------

Nennen Sie für das Mikrokern-Betriebssystem die vier Dienste-Schichten und die vier Schichten des Kernbereichs (Infrastrukturbereich). Geben Sie für jede der Schichten mindestens einen Dienst an, den diese für die darüber liegende Schicht bereitstellt.

.. image:: exam1.img



Aufgabe 2 (Gerätebetrieb, 4 Punkte)
-----------------------------------

Erläutern Sie kurz die Begriffe **Programmed I/O** und **DMA**.



Aufgabe 3 (Prozessumschaltstrategien, 12 Punkte)
------------------------------------------------

Welche der Umschaltstrategien (Scheduling-Verfahren), die in der Vorlesung vorgestellt wurden, sind den nachfolgenden Aufgabenstellungen (Szenarien) sinnvoll zuzuordnen? Begründen Sie Ihre Entscheidung auf Grund der Eigenschaften der jeweiligen Umschaltstrategien.

a. Eine feste Anzahl von Rechenaufträgen, deren Bedienzeiten bekannt sind, sollen so bearbeitet werden, dass die mittlere Antwortzeit minimal ist.
b. Die CPU soll fair unter den Prozessen in einem Mehrbenutzer-Betriebssystem aufgeteilt werden, wobei fair hier bedeutet, dass sich die Antwortzeit proportional zur Bedienzeit verhält.
c. Den Prozessen in einem Betriebssystem für Stapelverarbeitung (Batch-Betrieb) werden Prioritäten der Bearbeitung zugewiesen. Die Abarbeitung der Prozesse soll immer streng nach der zugewiesenen Priorität erfolgen.
d. Beliebige Rechenaufträge, deren Bedienzeiten aber bekannt sind, werden zu unterschiedlichen Zeitpunkten im System erzeugt. Sie sollen so abgearbeitet werden, dass die mittlere Antwortzeit möglichst minimal wird und es zu keinem Verhungern eines Prozesses kommt.



Aufgabe 4 (Prozesse, 10 Punkte)
-------------------------------

For the given state diagram of a microkernel operating system name the state transitions by specifying from which state to which other state the transition is performed. Briefly describe the state transition considering the data structures and the appropriate operations.

.. image:: exam2.img

Please use the following abbreviations to describe the states:

- A - Not existent
- B - Not active
- C - Ready
- D - Running
- E - Waiting (Blocked)



Aufgabe 5 (Prozesswechsel, 10 Punkte)
-------------------------------------

Name at least four occasions that may lead to a process switch.
Discuss for these different events the usefulness to design a scheduling which implements responsiveness and fairness.



Aufgabe 6 (Kommunikation, 10 Punkte)
------------------------------------

How can channel objects be connected (bound) to threads? Name pro and con for every method.



Aufgabe 7 (Thread-Interaktionsmechanismen, 4 Punkte)
----------------------------------------------------

Which parts of a monitor as a mechanism for protecting a critical section of a parallel
program must be provided by the operating system? Are there parts that cannot be
provided by the operating system? Give reasons for you answer.



Aufgabe 8 (Virtueller Speicher, 6 Punkte)
-----------------------------------------

a. In classic variants of virtual memory management, a distinction is made between segments and pages. When does this distinction make sense? Give reasons for you answer.
b. In the ARM architecture, the processes' page tables are located at virtual addresses. What are the advantages of managing page tables at virtual addresses instead of physical addresses in main memory?



Aufgabe 9 (Hauptspeicherverwaltung, 10 Punkte)
----------------------------------------------

Name and describe one strategy for thrashing prevention. The description has to cover the data necessary for the strategy, how the data is collected and the detection of the thrashing situation.



Aufgabe 10 (Verklemmungen, 8 Punkte)
------------------------------------

a. Name all of the four requirements for a deadlock!
b. What’s the difference between deadlock prevention and deadlock avoidance?
c. Name a strategy for deadlock prevention and give reasons which requirement named under a) will not occur!
d. A memory location in the physical address space can be considered to be a resource. What are the circumstances that prevent a deadlock? Give reasons for your answer.



Aufgabe 11 (Gerätebetrieb, 6 Punkte)
------------------------------------

The queue of a hard disc system contains the following requests. Use the given strategies to process the requests. Explain the plan of request processing according to the specified strategies.

The strategies are:

a. FCFS (First-Come-First-Served),
b. SSTF (Shortest-Seek-Time-First),
c. SCAN (Fahrstuhlstrategie/Elevator strategy),
d. SCAN-C (Zyklische Fahrstuhlstrategie/Cyclic Elevator strategy).

The queue contains:

61, 23, 45, 10, 97, 53, 22, 49, 83, 24

The current position of the head (read/write) is 52 and the head is moving upwards.



Aufgabe 12 (Dateisysteme, 9 Punkte)
-----------------------------------

A current challenge related to file systems is to keep them in a consistent state even after the system has crashed.

Name three solutions and describe why they significantly reduce the effort for restoring the consistency of the file system compared to a classic file system.



Aufgabe 13 (Leistungsmodellierung, 3 Punkte)
--------------------------------------------

What is Littles Law?



Zusatzaufgabe (Betriebssystemfunktionen, 2 Zusatzpunkte)
--------------------------------------------------------

The exercises gave you the opportunity to implement an operating system providing the following properties: device management without and with interrupts, interrupt and exception handling, thread management and thread switching including a simple scheduling, separation of the kernel and introduction of a kernel interface, separated process address spaces using the MMU. What task would you go on next? Give reasons for you answer.
