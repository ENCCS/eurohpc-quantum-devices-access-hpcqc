# The machines: differences and a few details

The three machines are genuinely different, in ways that change what a circuit even looks like. Please check the following table for details, and the white paper on [Zenodo](https://doi.org/10.5281/zenodo.17862354).

| | Euro-Q-Exa | VLQ | Piast-Q |
|---|---|---|---|
| Technology | Superconducting | Superconducting | Trapped ion |
| Qubits available | 53 of 54 | 23 of 24, on the calibration set | 20 |
| Connectivity | Lattice, 170 coupled pairs | Star, through one resonator | All to all |
| Native gates | `r`, `cz` | `prx`, `cz`, `move` | `RZ`, `R`, `RXX` |
| What you send | An abstract circuit; the site maps it | Native gates, mapped to physical qubits | Native gates, mapped to physical qubits |
| Authentication | Bearer token from a portal | Federated identity token | API key header |
| Time is billed in | Equivalent qubit-seconds | Device execution time | Device time, including ion loading |
| Access shape | One REST call | Two jobs | One REST call |

The row that matters most is *what you send*. On Euro-Q-Exa you can send an abstract circuit and
the site maps it for you. On the other two you must send native gates, already mapped to physical
qubits. The same Bell pair is three different objects.

:::{note}
The billing row is expanded in {doc}`qpu-hours`. How the machines sit alongside classical HPC is in
{doc}`hpc-qc`.
:::

## What you send, and where

```{figure} _static/routes.drawio.png
:alt: Block diagram with three lanes, one per machine. Euro-Q-Exa, superconducting lattice, an abstract circuit in OpenQASM, one REST call with a bearer token, the site transpiles, then the machine. VLQ, superconducting star, job 1 initialises the backend, the native, mapped circuit is staged as a file into job 2, job 2 executes, then the machine. Piast-Q, trapped ions, a native gate list with angles in units of pi, one REST call with an API key header, the site broker, then the machine.
:width: 100%

What you send and where you send it, for each of the three machines.
```

:::{note}
**The star topology.** On VLQ every two-qubit gate locus is (qubit, resonator); there is no
qubit-to-qubit coupling at all. An entangling operation between two qubits is a MOVE of one qubit's
state into the resonator, a CZ between the resonator and the other qubit, and a MOVE back. Since
that site does not transpile for you, the MOVEs have to be in the circuit you send, whether you
write them or a compiler inserts them. Any depth estimate you carried over from a lattice machine
will not hold.

For the design, see [the IQM Star paper](https://arxiv.org/abs/2503.10903) and IQM's
[MOVE gate](https://docs.meetiqm.com/iqm-client/api/iqm.qiskit_iqm.move_gate.MoveGate.html).
:::

## Official pages

- [EuroHPC JU: Our Quantum
  Computers](https://www.eurohpc-ju.europa.eu/eurohpc-quantum-computers/our-quantum-computers_en)
- [PCSS: PIAST-Q](https://quantum.psnc.pl/en/piast-q/)
- [IT4Innovations: VLQ quantum computer](https://www.it4i.cz/en/infrastructure/vlq-quantum-computer)
- [IQM: documentation](https://docs.iqm.tech/), and the
  [IQM client](https://docs.iqm.tech/iqm-client/)
- [AQT: ARNICA public API documentation](https://arnica.aqt.eu/api/v1/docs)
