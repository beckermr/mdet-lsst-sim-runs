# mdet-lsst-sim-runs

my configs and runs for the LSST sims


## Getting Going

### 1 - Make your conda env

You can create the environment via

```bash
conda env create -f environment.yml
```

### 2 - Download and Unpack the Data

TODO

### 3 - Optional: Get Notebooks Going at NERSC

TL;DR

```bash
conda activate mdet-lsst-sims
python -m ipykernel install --user --name mdet-lsst-sims --display-name mdet-lsst-sims
```

Put this in `~/.local/share/jupyter/kernels/mdet-lsst-sims/kernel.json`

```
{
 "argv": [
  "{resource_dir}/kernel-helper.sh",
  "-f",
  "{connection_file}"
 ],
 "display_name": "mdet-lsst-sims",
 "language": "python"
}
```

Put this in `~/.local/share/jupyter/kernels/mdet-lsst-sims/kernel-helper.sh`

```
#!/bin/bash -l

conda activate mdet-lsst-sims
exec python -m ipykernel_launcher "$@"
```
and execute

```bash
chmod u+x ~/.local/share/jupyter/kernels/mdet-lsst-sims/kernel-helper.sh
```

See the [NERSC documentation](https://docs.nersc.gov/services/jupyter/#conda-environments-as-kernels) for more details.
