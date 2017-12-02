# go-webview
A simple Go GUI application using the github.com/zserge/webview

It is not recommended to use go run (although it works perfectly fine on Linux). Use go build instead:

```
# Linux
$ go build -o webview-example && ./go-webview
```
```
# MacOS uses app bundles for GUI apps
$ mkdir -p webview.app/Contents/MacOS
$ go build -o webview.app/Contents/MacOS/webview
$ open webview.app # Or click on the app in Finder
```
```
# Windows requires special linker flags for GUI apps.
# It's also recommended to use TDM-GCC-64 compiler for CGo.
# http://tdm-gcc.tdragon.net/download
$ go build -ldflags="-H windowsgui" -o go-webview.exe
$ go-webview.exe
```