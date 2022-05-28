# hkgfinder <img src="img/logo.png" align="right" width="120"/>

[![License: GPL v3](https://img.shields.io/badge/License-MIT-blue.svg)](https://www.gnu.org/licenses/MIT)


## Find housekeeping genes in prokaryotic (meta)genomes


### Introduction



### Installation

You will have first to install [Prodigal](https://github.com/hyattpd/Prodigal) and [HMMER 3](https://hmmer.org) to be able to run hkgfinder.


#### Install from source

```bash
# Download hkgfinder development version
git clone https://github.com/Ebedthan/hkgfinder.git hkgfinder

# Navigate to directory
cd hkgfinder

# Install with poetry: see https://python-poetry.org
poetry install --no-dev

# Enter the Python virtual environment with
poetry shell

# Test hkgfinder is correctly installed
hkgfinder -h
```

If you do not want to go into the virtual environment just do:

```bash
poetry run hkgfinder -h
```

## Test

* Type `hkgfinder -h` and it should output something like:

```
usage: hkgfinder [options] [<FILE>]

optional arguments:
  -o [FILE]      output result to FILE [stdout]
  -g             activate genome mode [false]
  -m             activate metagenome mode [false]
  --faa FILE     output matched proteins sequences to FILE
  --fna FILE     output matched DNA sequences to FILE
  -t INT         number of threads [1]
  -q             decrease program verbosity
  -v, --version  show program's version number and exit
  -h, --help     show this help message and exit
```


## Invoking hkgfinder

```
hkgfinder --faa housekeeping.faa --fna housekeeping.fna file.fa.gz
```

  
## Bugs

Submit problems or requests to the [Issue Tracker](https://github.com/Ebedthan/hkgfinder/issues).


## Dependencies

### Mandatory

* [**Prodigal**](https://github.com/sib-swiss/pftools3)  
  Used for protein-coding gene prediction.    
  *Hyatt, D., Chen, GL., LoCascio, P.F. et al. Prodigal: prokaryotic gene recognition and translation initiation site identification. BMC Bioinformatics 11, 119 (2010). https://doi.org/10.1186/1471-2105-11-119*

* [**HMMER 3**](https://hmmer.org)  
  Used for HMM profile prediction.   
  *Eddy SR, Accelerated Profile HMM Searches. PLOS Computational Biology 2011, 10.1371/journal.pcbi.1002195*


## Licence

[MIT](https://github.com/Ebedthan/hkgfinder/blob/main/LICENSE).


## Author

* [Anicet Ebou](https://orcid.org/0000-0003-4005-177X)

