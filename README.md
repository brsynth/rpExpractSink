# rpextractsink

[![Anaconda-Server Badge](https://anaconda.org/brsynth/test/badges/latest_release_date.svg)](https://anaconda.org/brsynth/test) ![Test](https://github.com/brsynth/test/workflows/Test/badge.svg) [![Anaconda-Server Badge](https://anaconda.org/brsynth/test/badges/version.svg)](https://anaconda.org/brsynth/test)

RetroPath2 sink generator

## Input

Required:
* **input_sbml**: (string) Path to the input SBML file

Optional:
* **--remove_dead_end**: (boolean, default: True) Perform FVA evaluation to remove dead end metabolites
* **--compartment_id**: (string, default: MNXC3) Specify the compartment from which to extract the sink molecules. The default are for MetaNetX files

## Output

* **output_sbml**: (string) Path to the output csv file


## Install
### From pip
```sh
[sudo] python -m pip install rpextractsink
```
### From Conda
```sh
[sudo] conda install -c brsynth -c conda-forge -c bioconda rpextractsink
```

## Use

### Function call from Python code
```python
from rpextractsink import rpextractsink

sink = rpExtractSink(input_sbml, output_sink)
sink.genSink()
```

If parameters from CLI have to be parsed, the function `build_args_parser` is available:
```python
from rpextractsink import build_args_parser

parser = buildparser()
params = parser.parse_args()
```

### Run from CLI
```sh
python -m rpextractsink <input_sbml> <output_sink> [--compartment_id COMPARTMENT_ID] [--remove_dead_end REMOVE_DEAD_END]
```


## Authors

* **Melchior du Lac**
* Thomas Duigou, Joan Hérisson

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
