# zload

## Synopsis
zsh plugin to load functions as an autoloading function.

## How to set up

### Manually install

Put zload and _zload files somewhere in your $fpath and add the following line to your .zshrc:

```
autoload -Uz zload
```

#### For example

```
# download all files
% cd /path/to/dir
% git clone https://github.com/mollifier/zload.git
```

And add the following lines to your .zshrc:

```
fpath=(/path/to/dir/zload(N-/) $fpath)

autoload -Uz zload
```

### Installing using Antigen
If you use [Antigen](https://github.com/zsh-users/antigen), add the following line to your .zshrc:

```
antigen bundle mollifier/zload
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

