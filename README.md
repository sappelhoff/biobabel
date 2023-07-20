

# What is this

Many different file formats exist for physiology signals such as cardiac (ECG, PPG) or respiratory data. Many packages exist in Python to read these formats but they load into different data structures. This package is a wrapper of sorts for already existing tools providing a unified easy-to-use interface.



# Installation

```
python -m pip install 'biobabel @ git+https://github.com/florisvanvugt/biobabel'
```

# Usage


Simple usage example in Python:

```
import biobabel
bio = biobabel.load('filename.txt')
bio.print()
bio.plot()
bio.save('new_filename.hdf5')
```

More complete overview of functionality in [Jupyter notebook](https://github.com/florisvanvugt/biobabel/blob/main/tests/Usage.ipynb).


# Requirements


# Physiology dialects

Currently supported dialects are:
* hdphysio5 thanks to [hdphysio5](https://github.com/florisvanvugt/hdphysio5)
* labstreaminglayer (LSL) XDF (rudimentary) thanks to [pyxdf](https://pypi.org/project/pyxdf/)
* BioPAC Acknowledge (acq) thanks to [bioread](https://pypi.org/project/bioread/)
* opensignals ("OpenSignals (r)evolution" thanks to [opensignalsreader](https://github.com/PGomes92/opensignalsreader)
* Brams-Bio-Box (custom)
* TeensyECG (custom)

Wish-list:
* EDF
* Biosemi BDF https://pypi.org/project/pybdf/


# Development

Install locally:

```
pip install .
```

and editable:

```
pip install -e .
```



Create wheels with:

```
python3 -m build
```


