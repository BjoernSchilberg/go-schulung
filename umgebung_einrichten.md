#Getting Started

* <https://golang.org/doc/install>


##Git und Mercurial installieren

```
sudo apt-get install git mercurial
```


##Official binary distributions herunterladen

```
curl -O https://storage.googleapis.com/golang/go1.5.1.linux-amd64.tar.gz
```


##Integrität überprüfen

```
echo "46eecd290d8803887dec718c691cc243f2175fe0  go1.5.1.linux-amd64.tar.gz" | sha1sum -c -
```


##Entpacken nach /usr/local

```
sudo tar -C /usr/local -xzf go1.5.1.linux-amd64.tar.gz 
```

Hinweis: Es ist nicht nötig es systemweit zu installieren. Es wird hier der offziellen Dokumentation gefolgt.


##PATH environment variable setzen

```
echo "export PATH=$PATH:/usr/local/go/bin" > $HOME/.profile
source $HOME/.profile
```


##Installation testen

```
mkdir $HOME/work
export GOPATH=$HOME/work
mkdir -p $HOME/work/src/github.com/bjoernschilberg/hello
```


##hello.go erstellen

```go
package main

import "fmt"

func main() {
    fmt.Printf("hello, world\n")
}
```


##hello.go kompilieren und ausführen

```
cd $HOME/work
go install github.com/bjoernschilberg/hello
$GOPATH/bin/hello
```


##Verzeichnisstruktur/Code Organisation 

* <https://golang.org/doc/code.html>

```
work/
work/bin
work/bin/hello
work/src
work/src/github.com
work/src/github.com/bjoernschilberg
work/src/github.com/bjoernschilberg/hello
work/src/github.com/bjoernschilberg/hello/hello.go
```
