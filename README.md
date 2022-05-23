# Dotfiles

Setup and managed via [chezmoi](https://www.chezmoi.io/)

[Daily Operation Docs](https://www.chezmoi.io/user-guide/daily-operations/)

## Pull the latest changes from your repo and apply them

You can pull the changes from your repo and apply them in a single command:

`chezmoi update`

## Install chezmoi and your dotfiles on a new machine with a single command

chezmoi's install script can run chezmoi init for you by passing extra arguments to the newly installed chezmoi binary. If your dotfiles repo is github.com/khanhgee/dotfiles then installing chezmoi, running chezmoi init, and running chezmoi apply can be done in a single line of shell:

```
sh -c "$(curl -fsLS chezmoi.io/get)" -- init --apply khanhgee
```

If your dotfiles repo has a different name to dotfiles, or if you host your dotfiles on a different service, then see the reference manual for chezmoi init.

For setting up transitory environments (e.g. short-lived Linux containers) you can install chezmoi, install your dotfiles, and then remove all traces of chezmoi, including the source directory and chezmoi's configuration directory, with a single command:

```
sh -c "$(curl -fsLS chezmoi.io/get)" -- init --one-shot khanhgee
```
