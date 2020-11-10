# How to use sphinx-exercise with Jupyter Book

Below are some instructions on how to setup a Jupyter Book example and utilize `sphinx-exercise` extension.

```bash
conda create -n mybook pip
conda activate mybook
pip install -r requirements.txt

jb create mybook
cd mybook
```

Add extension under `_config.yml`:

```yaml
sphinx:
  extra_extensions:
    - sphinx_exercise
```

Now introduce an exercise directive

```{exercise}
This is an exercise directive.
```

Next build the book:

```bash
jb clean .
jb build .
```