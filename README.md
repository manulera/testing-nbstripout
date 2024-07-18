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

# Include the custom_nbstripout.sh file in the root directory
# Make sure to make it executable
chmod +x custom_nbstripout.sh

# Activate the hooks
pre-commit install
```