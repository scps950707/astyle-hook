You can use AStyle ([Artistic Style](http://astyle.sourceforge.net/)) source code indenter to
help you auto format your source code. It will for sure not correct all your coding styles but
for sure will eliminate most of them. You can download AStyle from [this location](http://astyle.sourceforge.net/)
or install via `apt-get`:
```sh
sudo apt-get install astyle
```

To format your file you can execute below command:
```sh
astyle -s2A1k3W3jD --suffix=none *.c
```
or
```sh
astyle -s2A1xlk3W3jD --suffix=none *.cpp
```

Install Git pre-commit hook to check C/C++ source file format
```sh
cd .git/hooks/
ln -sf ../../astyle-hook/pre-commit.hook pre-commit
```