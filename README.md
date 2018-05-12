My Jupyter notebooks
===

cloning this repo
---

##### 1. IHaskell

First clone this IHaskell fork:

```bash
https://github.com/neilrussell6/IHaskell
```

and follow setup instructions.

##### 2. this repo

Then clone this repo into the ``notebooks`` directory of the IHaskell clone:

```bash
cd IHaskell
git clone https://github.com/neilrussell6/jupyter-notebooks-boilerplate notebooks
```

The ``notebooks`` directory in the IHaskell fork is ignored, so you can maintain your notebooks in a separate repo.

usage
---

Follow usage instructions on [IHaskell Fork](https://github.com/neilrussell6/IHaskell).
But mostly you'll just use:

```bash
make serve
```

local notebooks
---

Notebooks created in the ``notebooks_local`` will be git ignored, so use this for tinkering with notebooks that you don't want to commit.

notebook specific dependencies
---

You can install dependencies for you Python 3 notebooks, 
by adding a ``requirements.in`` file to this ``notebooks`` directory,
and running (from the IHaskell repo root):
```bash
make pipcompile
make pipinstall
``` 
Also add the root ``requirements.txt`` as a dependency, like this:
```Make
-r ../requirements.txt
```

This way when you run ``make init`` or ``make pipcompile`` and ``make pipinstall``,
it will install both the root dependencies and those in your ``notebooks/requirements.in``).
