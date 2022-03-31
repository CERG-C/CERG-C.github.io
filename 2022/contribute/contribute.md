# Install and update this doc

mkpdfs-mkdocs
pip install weasyprint==52.5
pip install mkdocs-encryptcontent-plugin

pip install mike


## Deploy

From the root of the `CERG-C.github.io` repository, run from the terminal:

```
mkdocs gh-deploy --force --remote-branch main --config-file mkdocs.yml
```