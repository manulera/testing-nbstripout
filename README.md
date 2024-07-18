# nbstripout docs

A simple repository on how to add `nbstripout` as a hook to repository, using poetry as a dependency manager.

```bash
# Create a new poetry project from the root directory
poetry init

# Go to pyproject.toml and in [tool.poetry] add package-mode = false if this is not a package

# Add dependencies
poetry add ipykernel

# You might want these as dev dependencies
poetry add -G dev pre-commit nbstripout

# Add the hook as seen in the .pre-commit-config.yaml file

# Activate the hooks
pre-commit install
```

## Extra: make jupyter notebooks save often

I personally always forget to save my notebooks, so I normally change the settings of vscode to autosave. You can do so by going to settings and changing the `files.autoSave` to `afterDelay` and `files.autoSaveDelay` to `1000`. As far as I know there is no way to save on execution of cell, which would be ideal.
