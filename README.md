# Poetry-Compatible Triton

This is a poetry-compatible version of triton_pre_mlir

- First we had to fork triton, to generate a pyproject.toml: https://github.com/richgong/triton/tree/triton_pre_mlir
```
cd python/
pip install dephell[full]
dephell deps convert --from=setup.py --to=pyproject.toml
```
- Because poetry doesn't support installing from a Git repo's subdirs, we had to copy-paste `triton/python` into this new repo.
- Then you install like this: `poetry add triton-pre-mlir@git+https://github.com/richgong/triton.git`
