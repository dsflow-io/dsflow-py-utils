# dsflow python utils

## Create Python package:

http://python-packaging.readthedocs.io/en/latest/minimal.html

```
dsflow-py-utils/
    dsflow_py_utils/
        __init__.py
        help.py
    setup.py
```

`__init__.py`

```
from .help import help

```

`text.py`

```
def help():
    return (u'Wenn ist das Nunst\u00fcck git und Slotermeyer? Ja! ... '
            u'Beiherhund das Oder die Flipperwaldt gersput.')
```

`setup.py`

``` python
from setuptools import setup

setup(name='dsflow-py-utils',
      version='0.1',
      description='The funniest joke in the world',
      url='http://github.com/dsflow-io/dsflow-py-utils',
      author='Pierre-Marie Leveque',
      author_email='pm@dsflow.io',
      license='MIT',
      packages=['dsflow_py_utils'],
      zip_safe=False)
```


## Install python package

```
dsflow_py_utils = {git = "git@github.com:dsflow-io/dsflow-py-utils.git", editable = true}
```

OR

```
pip install -e git://github.com/{ username }/{ reponame }.git@{ tag name }#egg={ desired egg name }
```

then

```
>>> import dsflow_py_utils
>>> print dsflow_py_utils.help()
```