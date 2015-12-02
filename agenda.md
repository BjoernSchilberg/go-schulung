#Go Schulung

Ziel: Zeigen wie echte Anwendungen mit go gebaut werden.

#Tag1

##Einführung

* Effective Go
    * <https://golang.org/doc/effective_go.html>

* How to Write Go Code
    * <https://golang.org/doc/code.html>

* The Go Programming Language Specification
    * <https://golang.org/ref/spec>

##Buchempfehlung

* The Go Programming Language (Alan A. A. Donovan · Brian W. Kernighan)
    * <http://www.gopl.io/>

##Umgebung einrichten/Setup

* Wie wird der Compiler eingerichtet.
* Wie steht es um Editoren?
* Wie steht es um IDEs?


##Getting Started

* <https://golang.org/doc/install>
    * siehe [umgebung_einrichten.md](umgebung_einrichten.md)


##Beispiele aus "A Tour of GO"

* <https://tour.golang.org>


##Beispiele aus "A Tour of GO" auf dem realen Setup durchführen

* Themen: Concurrency (Channels/Select)
* Übung: Equivalent Binary Trees
    * <https://tour.golang.org/concurrency/7>
    * <https://tour.golang.org/concurrency/8>
 
 
##Tooling

Quelle: Profiling & Optimizing in Go / Brad Fitzpatrick

* <https://www.youtube.com/watch?v=xxDZuPEgbBU>
* <https://github.com/bradfitz/talk-yapc-asia-2015/blob/master/talk.md>
* <https://goo.gl/PYpNXT>


###Themen

* Wie bekomme ich Daten von a nach b.
* Detektion einer Data Race.
* Debugging (delve, gdb, ogle)
* CPU Profiling
* memory & garbage profiling
* Contention (block) profiling
* go test
* go Lint
* go Vet


#Tag2


##Lernen an realen Beispielen

Ziel: Typische Wiederverwendbare Muster mit Fokus auf Webandwendungen identifizieren.


###Beispiele

* <https://bitbucket.org/s_l_teichmann/pointstream>
* <https://bitbucket.org/s_l_teichmann/intests>
* <https://bitbucket.org/s_l_teichmann/mtsatellite>


##Übungen

* Beispiele erweitern und verbessern.


##Optionale Themen


###Einbinden von externen Bibliotheken

Am Beispiel von <http://www.gorillatoolkit.org/pkg/mux>


###context-Bibliothek

Themen: Requests, Global state über den Request definieren. Time-Out.

* <https://godoc.org/golang.org/x/net/context>

Die context-Bibliothek ist Geeignet für produktiven Code mit mehreren 1000 Clients.


###Debugging 

* Was sind Kernprobleme beim Debugging?
* Welche Lösungen gibt es?


### Versionierung

* <http://www.gonuts.io>
* <https://github.com/tools/godep>
* <http://getgb.io>

####Themen

* Abhängigkeiten zu einen bestimmten Zeitpunkt einfrieren.
* Wie kann garantiert werden, das meine Projekte nicht durch Upstream-Aktivitäten unbrauchbar werden.
* Abhängigkeiten zu unzuverlässigen github und bitbucket-Projekte minieren.
* Wie können System aufgebaut werden, welche diese Invarianten garantieren.

Weitere Infos:

* <https://github.com/golang/go/wiki/PackageManagementTools>

###Erfolg von GO
Go hat innerhalb von kurzer Zeit zu einem der größeren Community-Projekte der
freien Software Szene entwickelt (bspw. bei den Bibliotheken). 

Repositories werden mit Bordmitteln von go direkt unterstützt.  Ohne einen
großen Suchindex wie pip (Python) oder npm (nodejs) dazwischen.

Jeder der im sich ein im Netz verfügbares Repository anlegen kann, kann sofort
contributieren. Ohne Gedanken zu Themen wie Maintainership, bzw. Maintianership
innerhalb einer Linux-Distribution.


###Cross compiling
Einfach bei nativem go.

Sobald externe Dinge wie sqlite dazu kommen, wird Cross compiling schwierig, da
ein entsprechender Cross Compiler für die externen nicht nativen
go-Abhängigkeiten benötigt wird und für die entsprechende Zielarchitektur
verfügbar sein muss. 

* <https://bitbucket.org/s_l_teichmann/pointstream>
* <https://bitbucket.org/s_l_teichmann/zday>
