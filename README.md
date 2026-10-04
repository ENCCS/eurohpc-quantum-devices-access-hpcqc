# EuroHPC JU HPC-QC and quantum devices access in practice

An ENCCS lesson on EuroHPC quantum access as it works in practice: applying, onboarding at each
hosting site, and getting a circuit onto each of three machines (Euro-Q-Exa at LRZ, Piast-Q at PCSS,
VLQ at IT4Innovations).

Published address: https://enccs.github.io/eurohpc-quantum-devices-access-hpcqc/ Repository: https://github.com/ENCCS/eurohpc-quantum-devices-access-hpcqc

## Quick commands

```console
# build the lesson and open it
pixi run -e docs lesson && open lesson/_build/html/index.html

# a clean build
rm -rf lesson/_build && pixi run -e docs lesson
```
