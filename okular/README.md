To make sure that okular opens new pdfs in the same instance and in a new/existing tab, install with devmode.

```bash
sudo snap install --devmode okular
```

To save the settings, first create a snapshot.

```bash
snap save okular
```

Note down the id of the snapshot. Then save the snapshot to a file. Below I save snapshot 60.

```bash
sudo snap export-snapshot 60 $HOME/okular_snapshot
settings="$(git rev-parse --show-toplevel)"
cp $HOME/okular_snapshot "$settings/okular/"
```

Then import snapshot and restore.

```bash
sudo snap import-snapshot okular/okular_snapshot
sudo snap restore 60
```
