# Niprov
## Neurohackweek 2016
Jasper J.F. van den Bosch

Slides at neurohackweek.github.com/

Setup python environment
```shell
virtualenv env
source env/bin/activate
pip install -U pip
```

Download sample data
```shell
wget https://github.com/ilogue/niprov/archive/master.zip
unzip master.zip
cd niprov-master
```

Install Niprov
```shell
pip install niprov
```

Optional packages
```shell
pip install -r optional.txt # pydicom nibabel mne matplotlib
```

Why niprov?

What is provenance?

Manually too much, instead track along 

Commandline API

```shell
provenance -h
provenance discover ./testdata
provenance export
provenance export --file testdata/parrec/T1.PAR
provenance record "parrec2nii testdata/parrec/T1.PAR" --parent testdata/parrec/T1.PAR --new T1.nii
provenance record "mcflirt -in T1.nii -out T1_reg.nii.gz"
provenance export --file T1_reg.nii.gz
```

Python API
```python
from niprov import ProvenanceContext
provenance = ProvenanceContext()


Data storage
```shell
cp niprov.cfg ~/niprov.cfg
gedit ~/niprov.cfg
```

```shell
provenance serve
```







