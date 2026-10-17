# A few details on Euro-Q-Exa

- A REST API with a bearer token.
- Circuits go as OpenQASM and the site transpiles.
- A two-qubit entangling circuit at 100 shots returned:

```text
{'11': 48, '00': 47, '01': 5}
```

- You create the API token in the [Munich Quantum Portal](https://portal.quantum.lrz.de/) yourself.
- Check your account's expiry date against your allocation period.

- Superconducting, on a lattice with 170 coupled pairs, and 53 of 54 qubits available.
- The native gates are `r` and `cz`, but the site transpiles, so you can send an abstract circuit
  and the site maps it for you.
- Time is billed in equivalent qubit-seconds; see {doc}`qpu-hours`.
- For LRZ's definition of the unit, open: [LRZ: Definition of the computing unit for the LRZ Quantum
  Systems](https://doku.lrz.de/definition-of-the-computing-unit-for-the-lrz-quantum-systems-1898715012.html)

## Official pages

- For the HPC-QC route, open: [LRZ: HPCQC System Access and HPCQC Job Submission via
  MQSS-Adapter](https://doku.lrz.de/documentation-hpcqc-system-access-and-hpcqc-job-submission-via-mqss-adapter-2603423874.html)
- For the acknowledgement wording, open: [LRZ: Acknowledgement
  formulations](https://doku.lrz.de/acknowledgement-formulations-2495480854.html)
