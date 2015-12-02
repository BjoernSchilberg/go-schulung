#Editoren und IDEs

Richtig eingerichtete Editoren und IDEs sind wichtig und reduzieren das "Frusterlebnis" mit go ungemein.

##vim-go


##Go for Visual Studio Code

* https://www.visualstudio.com/de-de/products/code-vs.aspx
* https://github.com/microsoft/vscode-go

This extension adds rich language support for the Go language to VS Code, including:

* Colorization
* Completion Lists (using `gocode`)
* Snippets
* Quick Info (using `godef`)
* Goto Definition (using `godef`)
* Find References (using `go-find-references`)
* File outline (using `go-outline`)
* Rename (using `gorename`)
* Build-on-save (using `go build` and `go test`)
* Format (using `goreturns` or `goimports` or `gofmt`)
* [_partially implemented_] Debugging (using `delve`)


### Integrated Go-Tools

The extension uses the following tools, installed in the current GOPATH.  If
any tools are missing, you will see an "Analysis Tools Missing" warning in the
bottom right corner of the editor.  Clicking it will offer to install the
missing tools for you. 

* gocode: `go get -u -v github.com/nsf/gocode`
* godef: `go get -u -v github.com/rogpeppe/godef`
* golint: `go get -u -v github.com/golang/lint/golint`
* go-find-references: `go get -u -v github.com/lukehoban/go-find-references`
* go-outline: `go get -u -v github.com/lukehoban/go-outline`
* goreturns: `go get -u -v sourcegraph.com/sqs/goreturns`
* gorename: `go get -u -v golang.org/x/tools/cmd/gorename`


And for debugging:

* delve: Follow the instructions at https://github.com/derekparker/delve/wiki/Building.

### Missing

* godoc?
* golang.org/x/tools/cmd/oracle


##Atom Editor

* https://atom.io/
* https://atom.io/packages/go-plus
* https://github.com/joefitzgerald/go-plus (Pivotal)


## Overview

This package adds extra Atom functionality for the go language:

* Autocomplete using `gocode` (you _must_ have the `autocomplete-plus` package activated for this to work)
* Formatting source using `gofmt`, `goimports`, or `goreturns`
* Code quality inspection using `go vet`
* Linting using `golint`
* Syntax checking using `go build` and `go test`
* Display of test coverage using `go test -coverprofile`
* Go to definition using `godef`

### Planned Features

The following features will be added soon:

* `godoc` integration ([#12](https://github.com/joefitzgerald/go-plus/issues/12))
* `gb` support
* go `vendor experiment` support
* `gorename` integration ([#174](https://github.com/joefitzgerald/go-plus/issues/174))
* ... and others: https://github.com/joefitzgerald/go-plus/issues

###Missing Features

* golang.org/x/tools/cmd/oracle

###Weitere

* https://atom.io/packages/go-rename
* https://github.com/jstemmer/gotags

###Querlesen

* http://marcio.io/2015/07/supercharging-atom-editor-for-go-development/


##Sublime Text
* http://www.sublimetext.com

###sublime-build
* https://github.com/golang/sublime-build (official Sublime Text package)

Nur "Build"-Unterstützung:
* https://github.com/golang/sublime-build/blob/master/docs/commands.md

* "build": executes go build -v
* "run": executes go run -v {current_filename}
* "test": executes go test -v
* "install": executes go install -v
* "clean": executes go clean -v
* "cross_compile": executes go build -v with GOOS and GOARCH set

###GoSublime
Für Sublime2 und Sublime3. Veraltet? Letzter Commit am 06.12.2014.
* https://github.com/DisposaBoy/GoSublime 

###GoTools
Nur für Sublime3. Alpha-Status.
* https://github.com/ironcladlou/GoTools

go get -u -v github.com/nsf/gocode
go get -u -v github.com/rogpeppe/godef
go get -u -v golang.org/x/tools/cmd/goimports
go get -u -v golang.org/x/tools/cmd/oracle
go get -u -v golang.org/x/tools/cmd/gorename

##IntelliJ IDEA
* https://www.jetbrains.com/idea/
* https://github.com/go-lang-plugin-org/go-lang-idea-plugin
* http://munchpress.com/how-to-install-golang-idea-plugin-for-intellij-14-1-x/

Einrichtung könnte einfacher sein.

##Eclipse
* https://github.com/GoClipse/goclipse

Scheinbar nur Unterstützung für Syntax-Highlighting und Einrückungen.


##Beobachtung

Für die meisten IDE's wird eine vorhande Go-Umbgebung mit den entsprechenden Werkzeuge vorrausgesetzt.

* godoc
* gofmt
* gocode: `go get -u -v github.com/nsf/gocode`
* godef: `go get -u -v github.com/rogpeppe/godef`
* goimports: `go get -u -v golang.org/x/tools/cmd/goimports`
* golint: `go get -u -v github.com/golang/lint/golint`
* go-find-references: `go get -u -v github.com/lukehoban/go-find-references`
* go-outline: `go get -u -v github.com/lukehoban/go-outline`
* goreturns: `go get -u -v sourcegraph.com/sqs/goreturns`
* gorename: `go get -u -v golang.org/x/tools/cmd/gorename`
* oracle: `go get -u -v golang.org/x/tools/cmd/oracle`
* Debugging
  * delve: Follow the instructions at https://github.com/derekparker/delve/wiki/Building.


##Fazit

* Die Go-Community empfiehlt den Einsatz von IntelliJ IDEA (mit Fokus auf Debugging mittels delve) und Sublime.
* Atom und Visual Studio Code sehen ebenfalls brauchbar aus.
* Richtig Spaß macht es mit vim-go.
