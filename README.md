![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/master/images/samples/01-ordinary-prompt.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/master/images/samples/02-bang.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/master/images/samples/03-useful-information.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/master/images/samples/04-untracked-files.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/master/images/samples/06-rm-commit.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/master/images/samples/06-tris-colors.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/master/images/samples/07-tracking-branches.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/master/images/samples/08-push-rebase-and-remote-branch-names.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/master/images/samples/09-you-can-push.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/master/images/samples/10-you-are-behind-fast-forward.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/master/images/samples/11-diverged.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/master/images/samples/12-detached.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/master/images/samples/13-stash-and-tag.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/master/images/samples/14-action-in-progress.jpg)


![alt tag](https://raw.github.com/arialdomartini/oh-my-git-gh-pages/gh-pages/images/shut-up.gif)


# Installation
## <a name="install-the-font"></a>The Font

oh-my-git is shipped with 3 themes. The one showed above is called [oppa-lana-style](https://github.com/arialdomartini/oh-my-git-themes/blob/oppa-lana-style/oppa-lana-style.zsh-theme). It's based on the [Awesome-Terminal-Fonts](https://github.com/gabrielelana/awesome-terminal-fonts) by [@gabrielelana](https://github.com/gabrielelana). The screenshots above use the font [Source Code Pro](https://github.com/adobe/Source-Code-Pro) by Adobe patched to include additional glyphs from [Powerline](https://github.com/powerline/powerline) and from Awesome-Terminal-Fonts .

You can [download](https://github.com/gabrielelana/awesome-terminal-fonts/tree/patching-strategy/patched) the fonts freely.

Install one of the fonts, or apply the Awesome-Terminal-Fonts [fallback strategy](https://github.com/gabrielelana/awesome-terminal-fonts/blob/master/README.md#patching-vs-fallback).
Then, configure your terminal to use it.

## Bash

One liner for OS X:

    cd ~ && git clone https://github.com/arialdomartini/oh-my-git.git && echo source $HOME/oh-my-git/prompt.sh >> .profile

One liner for Ubuntu:

    cd ~ && git clone https://github.com/arialdomartini/oh-my-git.git && echo source $HOME/oh-my-git/prompt.sh >> .bashrc

Then, set your Terminal font to any of the Awesome-Terminal-Fonts or use the fallback strategy.

You can also edit oh-my-git, change the symbols used and choose whatever font you like.

## Manual installation

Fork the repo and git clone it in your home directory.

Then add

    source $HOME/oh-my-git/prompt.sh

to the bash startup file (`~/.profile` on Mac, `~/.bashrc` on Linux)

If you prefer to keep oh-my-git repository in a different directory, just modify the startup file accordingly to the chosen position

    source /wherever-you-want/oh-my-git/prompt.sh

## zsh

With antigen installed, just add

    antigen-bundle arialdomartini/oh-my-git
    antigen theme arialdomartini/oh-my-git-themes oppa-lana-style

to your `.zshrc` file.

[`oh-my-git-themes`](https://github.com/arialdomartini/oh-my-git-themes) still includes the old 2 themes [arialdo-granzestyle](https://github.com/arialdomartini/oh-my-git-themes/blob/master/arialdo-granzestyle.zsh-theme)  (which is inspired to the great [Granze theme](https://github.com/Granze/G-zsh-theme-2)) by [@granze](https://github.com/granze), and [arialdo-pathinline](https://github.com/arialdomartini/oh-my-git-themes/blob/master/arialdo-pathinline.zsh-theme). If you want to use them, edit accordingly your ```.zshrc``` file.

## How to install antigen

[antigen](https://github.com/zsh-users/antigen) is a plugin manager for `zsh`.
Installing antigen is straightforward:

    cd ~ && git clone https://github.com/zsh-users/antigen.git .antigen 

Then, edit your `.zshrc` file including

    source "$HOME/.antigen/antigen.zsh"

    antigen-bundle arialdomartini/oh-my-git
    antigen theme arialdomartini/oh-my-git-themes oppa-lana-style

    antigen-apply

I also strongly suggest to include

    antigen-use oh-my-zsh
    antigen-bundle git
    antigen-bundle zsh-users/zsh-syntax-highlighting
    antigen-bundle zsh-users/zsh-history-substring-search

which are optional, but very cool. It's important to include those lines before ```antigen-apply```. You could take [this zsh configuration file](https://github.com/arialdomartini/dotfiles/blob/69e5ff22726181cc4f6ace37157ef53155f773b8/.zshrc) as a reference.

When you restart zsh, antigen will download and install all that's needed.

# Disabling oh-my-git
oh-my-git can be disabled on a per-repository basis. Just add a

    [oh-my-git]
    enabled = false

in the `.git/config` file of a repo to revert to the original prompt for that particular repo. This could be handy when working with very huge repository, when the git commands invoked by oh-my-git can slow down the prompt.

# Troubleshooting

**Q**: "Help, I installed oh-my-git but this is what I see:"

![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/master/images/samples/bad-font.png)

**A**: It's likely that you forgot to [install the font](#install-the-font).



**Q**: "I don't want to install a new font!"

**A**: "No prob. You may select [another theme](https://github.com/arialdomartini/oh-my-git-themes), or you can customize symbols. Take a look to the [prompt.sh](https://github.com/arialdomartini/oh-my-git/blob/master/prompt.sh) file. It contains a list of pre-defined symbols, similar to:

    # Symbols
    : ${omg_is_a_git_repo_symbol:='❤'}
    : ${omg_has_untracked_files_symbol:='∿'}
    : ${omg_has_adds_symbol:='+'}
    : ${omg_has_deletions_symbol:='-'}
    : ${omg_has_modifications_symbol:='✎'}

Those are just default values. If you wish to use another glyph for untracked file, just define a

    omg_has_untracked_files_symbol="whatever"

in your shell startup file.

# Known bugs and limitations

* git v1.8.4 or newer is required
* It works weird on brand new repositories, before the first commit
* It has been tested on Mac and Ubuntu only. I never managed to make it work on Cygwin
* Depending on the theme selected, you need an unicode font (like Sauce Code Pro, Menlo or Monaco on Mac OS X, or Monospace on Ubuntu; on Windows, with Cygwin, a good choice is [Meslo](https://github.com/andreberg/Meslo-Font) by [André Berg](https://github.com/andreberg), but I didn't tested the ooppa-lana-style theme)
* If the Terminal uses a clear background color, in Bash you need to change the colors defined in [prompt.sh](https://github.com/arialdomartini/oh-my-git/blob/oppa-lana-style/prompt.sh). The zsh version is not affected by this problem.
