You can use AStyle ([Artistic Style](http://astyle.sourceforge.net/)) source code indenter to
help you auto format your source code. It will for sure not correct all your coding styles but
for sure will eliminate most of them. You can download AStyle from [this location](http://astyle.sourceforge.net/)
or install via `apt-get`:
```sh
sudo apt-get install astyle
```

To format your file you can execute below command:
```sh
astyle -A1s2pDHk3W3j --suffix=none *.c
```
or recursively
```sh
astyle -A1s2pDHk3W3j --recursive --suffix=none *.c
```

Install Git pre-commit hook to check C/C++ source file format
```sh
mkdir astyle-hook && cd astyle-hook/
wget https://raw.githubusercontent.com/scps950707/astyle-hook/master/pre-commit.hook && chmod +x pre-commit.hook
cd ../.git/hooks/
ln -sf ../../astyle-hook/pre-commit.hook pre-commit
```

Astyle Details

- Bracket Style Options
[--style=allman / --style=bsd / --style=break / -A1](http://astyle.sourceforge.net/astyle.html#_style=allman)
- Tab Options
[--indent=spaces / --indent=spaces=# / -s#](http://astyle.sourceforge.net/astyle.html#_indent=spaces)
- Padding Options
[--pad-oper / -p](http://astyle.sourceforge.net/astyle.html#_pad-oper)
[--pad-paren-in / -D](http://astyle.sourceforge.net/astyle.html#_pad-paren-in)
[--pad-header / -H](http://astyle.sourceforge.net/astyle.html#_pad-header)
[--align-pointer=name   / -k3](http://astyle.sourceforge.net/astyle.html#_align-pointer)
[--align-reference=name   / -W3](http://astyle.sourceforge.net/astyle.html#_align-reference)
[--add-brackets / -j](http://astyle.sourceforge.net/astyle.html#_add-brackets)
