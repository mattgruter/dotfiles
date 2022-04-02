# Matthias' dotfiles

Matthias Grüter's dotfiles, managed with `chezmoi`.

## chezmoi

This repository is managed by [chezmoi](https://chezmoi.io). To set up a new machine, run:

```sh
chezmoi init mattgruter
```

### Secrets

Secrets are fetched from Bitwarden. Login and unlock the vault before running `chezmoi`:

```sh
bw login USERNAME
export BW_SESSION=$( bw unlock --raw )
```

If you've sourced this repo's `.zshrc` you can just run

```sh
bwu
```

to easily unlock the vault and set the session variable.
