[![Flattr this git repo](http://api.flattr.com/button/flattr-badge-large.png)](https://flattr.com/submit/auto?user_id=unic0rn&url=https://github.com/unic0rn/fancybash&title=fancybash&language=&tags=github&category=software)

fancybash
================

#### About ####

This is a rewrite of [oh-my-git](<https://github.com/arialdomartini/oh-my-git>), with some minor - and some not so minor - differences:

* it tries to be faster
* it displays a little bit more info...
* ...but it lacks stash support (I'll add it if there'll be interest)
* it's easily themeable
  * like, really easily

#### Requirements ####

tcl, stty, [one of those fonts](<https://github.com/ryanoasis/nerd-fonts>)

#### Installation ####

## bash:##

Just add this line:
```bash
PROMPT_COMMAND='PS1=`/path/to/fancybash eezoterial`'
```
to your .bashrc, where `eezoterial` is the name of the theme.

## other shells:##

It should be possible to use it with zsh (and perhaps other shells as well), I just didn't try. If you'll get it working under anything else than bash, let me know and I'll update the readme.

#### Themes ####

So far there is one, called eezoterial. It's designed to work with [eezoterial terminal theme](<https://github.com/unic0rn/eezoterial>), but since eezoterial palette tries to be compatible with solarized palette, eezoterial theme for fancybash should look just fine if you're using solarized (base16) terminal theme. And yes, I didn't bother checking it.

It doesn't matter though, since creating new themes is really easy. Create a copy of eezoterial theme, open it, get your mind blown.

#### Screenshots ####

Coming soon.
