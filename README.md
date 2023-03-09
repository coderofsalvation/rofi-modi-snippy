# rofi-modi-snippy

A modi to use with [rofi](https://github.com/davatorium/rofi). It presents a
list of snippy-compatible snippets (keys) and simulate a user keyboard input of a
corresponding value.

# Dependencies

- xdotool

# Installation

1. Clone the repo.
1. create the directory `~/.snippy` and put snippetfiles in there
1. Start `rofi` as follows:

      rofi -show snip -modi snip:/path/to/snippy

(it can be combined with other `modi`s, separated by commas)

# Features 

Snippets are strings of text, which are written with `xdotool` in the window
with focus. Snippets starting by *cmd* are passed through `eval` and the written
string is the result of the evaluation. See the `cmddate` and `cmdepoch`
examples.

* multiline support (though slow, hence MAXLINES=15 by default)
* evaluates shellscript inside snippets (`$(ls -la | grep foo)` e.g.)
* snippy-compatible: see [snippy.sh](https://bbs.archlinux.org/viewtopic.php?id=71938&p=2) and [snippy](https://github.com/tseemann/snippy)

