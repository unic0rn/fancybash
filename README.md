fancybash
================

## About ##

This is a rewrite of [oh-my-git](<https://github.com/arialdomartini/oh-my-git>), with some minor - and some not so minor - differences:

* it is much faster
  * on freebsd, with fresh git repo into which linux kernel was dumped (tar xzf & git add . - over 62k files), fancybash takes on average 2 seconds to display the prompt, versus 9 seconds for oh-my-git (it depends on cpu and disk speed, obviously)
* it displays a little bit more info...
  * ...but it lacks stash support (I'll add it if there'll be interest)
* it's easily themeable
  * like, really easily
* it adapts to the width of the terminal - within some reasonable degree

## Requirements ##

tcl, stty, [one of those fonts](<https://github.com/ryanoasis/nerd-fonts>)

#### Disclaimer ####

Non-monospaced fonts are not supported. I know, smaller icons don't look as nice, but if you'll try using such icons in Vim running in a terminal, you'll understand that monospace is the way to go. Also, with non-monospaced fonts adapting to the terminal width will not work.

## Installation ##

#### bash: ####

Just add this line:
```bash
PROMPT_COMMAND='PS1=`/path/to/fancybash eezoterial`'
```
to your `.bashrc`, where `eezoterial` is the name of the theme.

#### Visual Studio Code: ####

I'm using `bash.bat`:
```bat
@echo off
set VSCODETERM=%cd%
Z:
cd \cygwin\bin
bash.exe --login -i
```

and this snippet in `.bashrc`:
```bash
if [[ -z ${VSCODETERM} ]]; then
    PROMPT_COMMAND='PS1=`/z/devel/fancybash/fancybash eezoterial`'
else
    PROMPT_COMMAND='PS1=`/z/devel/fancybash/fancybash vscode mono`'
    cd `cygpath $VSCODETERM`
fi
```

That way I have full color prompt in mintty and monochrome in Visual Studio Code (since it seems to have trouble with ansi escape codes). Obviously, the path is preserved so choosing current working directory works as supposed.

#### other shells: ####

It should be possible to use it with zsh (and perhaps other shells as well), I just didn't try. If you'll get it working under anything else than bash, let me know and I'll update the readme.

## Themes ##

So far there is one, called eezoterial. It's designed to work with [eezoterial terminal theme](<https://github.com/unic0rn/eezoterial>) (to be precise, with light version only), but since eezoterial palette tries to be compatible with solarized palette, eezoterial theme for fancybash should look just fine if you're using solarized (base16) terminal theme. And yes, I didn't bother checking it.

It doesn't matter though, since creating new themes is really easy. Create a copy of eezoterial theme, open it, have fun.

If you'll want your theme to be added to this repo, send me a pull request with the theme, screenshot and a link to the terminal theme it uses.

## Screenshots ##

eezoterial theme @ [eezoterial terminal theme (light)](<https://github.com/unic0rn/eezoterial>)

![eezoterial](/images/eezoterial.png?raw=true)
