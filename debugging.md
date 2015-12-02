#Debugging

* Es gibt keine integrierte/keine geschlossene Debugging Lösung.
* Kernproblem von go und debugging sind die go-routinen.

##delve

* https://github.com/derekparker/delve/
  * https://github.com/derekparker/delve/wiki/Building

* Beste Lösung.
* Nicht Offiziell.
* Integrierte Lösung für Intellij Idea verfügbar.
* Windows-Unterstützung in Arbeit.
  * https://github.com/derekparker/delve/issues/198 (Meta-Ticket)
  * https://github.com/derekparker/delve/pull/276 (Windows-Port vom selben Entwickler wie das Visual Studio Code-Plugin)


##ogle 

* https://github.com/golang/debug
* Fazit: Nicht nutzbar

##godebug

* https://github.com/mailgun/godebug

Instrumentierungswerkzeug. Bevor das Programm in go übersetzt wird, durchläuft
es einen Generator, welcher den Code mit println-Statements versieht.

##gdb

* https://golang.org/doc/gdb

* Eine go-rountine kann im Laufe ihres Leben in mehreren Threads leben.
* gdb ist dafür nicht nutzbar.
* Problem ist nicht der gdb selbst sondern die python-Schnittstelle von gdb.
* python ist nicht in der Lage das Verhalten von go-routinen nach zu vollziehen.
* Der Kontext geht verloren.

###Hilfmittel im Umgang mit gdb
```
runtime.GOMAXPROCS(1)
```  

* Damit keine echte Multi-Core Nebenläufigkeit mehr vorhanden.
* Läuft damit nur noch auf einem Thread.
* Dann funktioniert gdb.

##Empfehlung

* Es ist ein klassisches Dilemma, introspektiv zur Laufzeit in ein Programm hinein  schauen zu wollen. 
* Am Besten ist es den Code von Anfang an so instrumentieren, das der Code sagt war er glaubt zu tun.
 
* Bedeutet: Mit relativen vielen log-Ausgaben ein Bild davon zu bekommen wie das Programm überhaupt läuft.
* Damit anhand des "Logs" einen Plan davon entwickelt werden kann was überhaupt schief läuft.
 
* Ist eine Frage der Art und Weise des Arbeitens.
* Die Entwickler von Go sind von der alten Schule und glauben eher an println debugging.
 
* Daher ist dieser Blick, wenn man aus der IDE-Welt kommt, eher gewöhnungsbedürftig.
