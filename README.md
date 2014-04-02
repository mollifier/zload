# zload

## Synopsis
zsh plugin to load functions as an autoloading function.

## How to set up
Put zload and _zload files somewhere in your $fpath and add this line to your .zshrc:

```
autoload -Uz zload
```

## Usage

```
% zload [-a|-d] FILE...
```

Load <var>FILEs</var> as an autoloading function.
zload can load autoloading function or zsh completion files as input file

When -a option is specified, from then on come to reload functions automatically. -d option stops this feature.

## Options
* `-a` enable auto reload
* `-d` disable auto reload
* `-h` display help and exit

## Examples

```
# Load myfunc and _myfunc.
% zload myfunc _myfunc

# Now we can call myfunc even if it isn't in fpath.
% myfunc

# Load myfunc again and enable auto reload.
% zload -a myfunc

# edit myfunc
# ...
# Changes are applied immediately if auto reload is enabled.
% myfunc

# Disable auto reload.
% zload -d

# Enable auto reload.
% zload -a
```

