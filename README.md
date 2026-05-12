# Matthias' dotfiles

Matthias Grüter's dotfiles, managed with `chezmoi`.

## chezmoi

This repository is managed by [chezmoi](https://chezmoi.io). To set up a new machine, run:


### Bootstrapping a new machine

Install chezmoi and bitwarden-cli before bootstrapping.

```sh
chezmoi init --apply --ssh mattgruter
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

### Tasks

List files that are managed by chezmoi:

```sh
chezmoi managed
```

List files that neither managed nor ignored by chezmoi

```sh
chezmoi unmanaged
```

Pull latest updates and apply

```sh
chezmoi updat
```
