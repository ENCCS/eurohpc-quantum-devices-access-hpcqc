# A few details on Euro-Q-Exa

- A REST API with a bearer token.
- Circuits go as OpenQASM and the site transpiles.
- A two-qubit entangling circuit at 100 shots returned:

```text
{'11': 48, '00': 47, '01': 5}
```

- You create the API token in the [Munich Quantum Portal](https://portal.quantum.lrz.de/) yourself.
- Check your account's expiry date against your allocation period.

- Superconducting, on a square lattice of 54 qubits.
- The native gates are `r` and `cz`, but the site transpiles, so you can send an abstract circuit
  and the site maps it for you.
- Unless a job sets `no_modify`, the site compiles it: the portal's FAQ says the MQSS pipeline
  transpiles and optimises circuits automatically before execution.
- To run on qubits of your choice, compile locally for the live layout and send with `no_modify`, as
  the MQSS training material shows. The MQSS adapter guide says `no_modify` skips the transpilation
  at the site and sends the circuit as it is.
- To see what ran, open the job's page in the Munich Quantum Portal: the Executed Circuit section
  shows the compiled circuit.
- Times in REST results and on the portal's job pages carry no zone, and the job pages mark them GMT,
  but they appear to be local time in Germany. Convert them before you compare them with UTC.
- EuroHPC time on Euro-Q-Exa is billed in wall-clock QPU seconds, not in LRZ's equivalent
  qubit-seconds.
- LRZ defines a unit for its quantum systems, the equivalent qubit-second; see {doc}`qpu-hours`.
- For LRZ's definition of the unit, open: [LRZ: Definition of the computing unit for the LRZ Quantum
  Systems](https://doku.lrz.de/definition-of-the-computing-unit-for-the-lrz-quantum-systems-1898715012.html)
- A job may hold at most 3 million shots times gates, summed over the circuits in a batch (LRZ).

## Official pages

- For the HPC-QC route, open: [LRZ: HPCQC System Access and HPCQC Job Submission via
  MQSS-Adapter](https://doku.lrz.de/documentation-hpcqc-system-access-and-hpcqc-job-submission-via-mqss-adapter-2603423874.html)
- For the acknowledgement wording, open: [LRZ: Acknowledgement
  formulations](https://doku.lrz.de/acknowledgement-formulations-2495480854.html)
- For LRZ's article on calibration, open: [LRZ: Quantum computing: Using AI for
  Calibration](https://www.lrz.de/en/research/research-projects/detail/calibration-of-quantum-computing)
