You can use AStyle ([Artistic Style](http://astyle.sourceforge.net/)) source code indenter to
help you auto format your source code. It will for sure not correct all your coding styles but
for sure will eliminate most of them. You can download AStyle from [this location](http://astyle.sourceforge.net/)
or install via `apt-get`:
```sh
sudo apt-get install astyle
```

To format your file you can execute below command:
```sh
astyle --suffix=none `find . -regex '.*\.[ch]p*p*$'`
```
