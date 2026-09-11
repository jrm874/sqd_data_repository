This is a data repository for the paper titled:



[**Chemistry Beyond the Scale of Exact Diagonalization on a Quantum-Centric Supercomputer.**](https://arxiv.org/abs/2405.05068)

This repository contains for all molecules considered in the study:

- Energy approximations (and exact when possible) obtained from classical many-body methods: ``/classical_reference_methods``.

- The electronic integrals for all molecules considered in ``fcidump`` format [link](https://pyscf.org/_modules/pyscf/tools/fcidump.html).

- The raw experiment data and results in ``/experiments``:
    - Raw dictionaries of samples together with a python script to lead them: ``/experiments/{molecule name}/experiment_data.zip``.
    - Energies (and variances when available) obtained from the quantum experiments using sqd: ``/experiments/{molecule name}/sqd_hardware_energetics``.
    - Template script to generate the ``qiskit`` circuits run on the experiments. The circuits were generated using the python package [ffsim](https://github.com/qiskit-community/ffsim).
    - Energies obtained by running SQD on samples obtained from the uniform distribution: ``/experiments/{molecule name}/sqd_on_uniform_distribution``.


- Numerics on noiseless performance of SQD: ``/numerics``
 
The SQD implementation can be found in the python package [qiskit-addon-sqd](https://docs.quantum.ibm.com/guides/qiskit-addons-sqd). It is an open source project version-controlled on [GitHub](https://github.com/Qiskit/qiskit-addon-sqd). In the manuscript we used the ``0.1.0`` version of the package. Note that all versions of the package are available on both [GitHub](https://github.com/Qiskit/qiskit-addon-sqd) and [PyPI](https://pypi.org/simple/qiskit-addon-sqd/). 

This [tutorial](https://github.com/Qiskit/qiskit-addon-sqd/blob/main/docs/tutorials/01_chemistry_hamiltonian.ipynb) implements the same SQD workflow as in the manuscript.

Note: The bond distances for the N2 molecule are given in fractions of 1.0975135 Angstroms. So to convert the units given here to Angstroms, multiply by 1.0975135.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.15324153.svg)](https://doi.org/10.5281/zenodo.15324153)
