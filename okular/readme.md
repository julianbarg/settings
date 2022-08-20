To make sure that okular opens new pdfs in the same instance and in a new/existing tab, install with devmode.

```bash
sudo snap install --devmode okular
```

To save the settings

```bash
settings="$(git rev-parse --show-toplevel)"
cp $HOME/.config/okularpartrc "${settings}/okular"
```
