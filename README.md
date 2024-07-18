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

# Activate the hooks
pre-commit install
```