# py-package-starter
Built and distribute your own Python package

#### 1. Create a folder
`hello-package`

#### 2. Create a subfolder and name it with the package name
`hello-package`

#### 3. Create `__init__.py` file inside subfolder

#### 4. Create `[module].py` inside module folder and insert the codes.

#### 5. Create a file `setup.py` in parent folder and paste the following code
```py
from setuptools import setup, find_packages
import codecs
import os

here = os.path.abspath(os.path.dirname(__file__))

with codecs.open(os.path.join(here, "README.md"), encoding="utf-8") as fh:
    long_description = "\n" + fh.read()

VERSION = '0.0.1'
DESCRIPTION = 'Short Description'

# Setting up
setup(
    name = "hello-package",
    version = VERSION,
    author = "Abdul Fathah KA",
    author_email = "fathah@ziqx.in",
    description = DESCRIPTION,
    long_description=long_description,
    long_description_content_type = "text/markdown",
    url = "https://github.com/fathah/py-package-starter",
    classifiers = ["Programming Language :: Python :: 3", "License :: OSI Approved :: MIT License", "Operating System :: OS Independent"],
    keywords=['nlp', 'fathah', 'hello'],
    packages = find_packages()
    )

```

#### 6. Install the package in the same folder and test the package
```sh
pip install .
```
#### 7. Build for distribution
```sh
python setup.py sdist bdist_wheel
```
#### 8. Install `twine`
```sh
pip install twine
```
#### 9. upload the package to `PyPi`
```sh
twine upload dist/*
```
