# Quick Reference

## The three machines

| | Euro-Q-Exa | Piast-Q | VLQ |
|---|---|---|---|
| Site | LRZ, Germany | PCSS, Poland | IT4Innovations, Czechia |
| Technology | Superconducting | Trapped ion | Superconducting |
| Qubits available | 53 of 54 | 20 | 23 of 24, on the calibration set we ran against |
| Connectivity | Lattice, 170 coupled pairs | All to all | Star, through one resonator |
| Native gates | `r`, `cz` | `RZ`, `R`, `RXX` | `prx`, `cz`, `move` |
| Who transpiles | The site | You | You |
| Authentication | Bearer token from a portal | API key header | Federated identity token |
| Credential lifetime | Token: no expiry shown in the portal | | Access token lasts six hours |
| Time is billed in | Equivalent qubit-seconds | Device time, including ion loading | Device execution time |
| Access shape | One REST call | One REST call | Two jobs |
| Page | {doc}`euro-q-exa` | {doc}`piast-q` | {doc}`vlq` |

(official-links)=

## Links, by task

A dash means this lesson lists no official page for that cell.

| Task | EuroHPC JU | LRZ, Euro-Q-Exa | PCSS, Piast-Q | IT4Innovations, VLQ |
|---|---|---|---|---|
| Apply | •&nbsp;[User Portal](https://access.eurohpc-ju.europa.eu/)<br>•&nbsp;[Call for proposals for Quantum Access Pilot Mode](https://www.eurohpc-ju.europa.eu/eurohpc-ju-call-proposals-quantum-access-pilot-mode_en) | - | - | - |
| Policy | •&nbsp;[Supercomputers Access Policy and FAQ](https://www.eurohpc-ju.europa.eu/supercomputers/supercomputers-access-policy-and-faq_en) | - | - | - |
| Machines | •&nbsp;[Quantum Computing & Access](https://www.eurohpc-ju.europa.eu/quantum-technologies/quantum-computing-access_en)<br>•&nbsp;[Our Quantum Computers](https://www.eurohpc-ju.europa.eu/eurohpc-quantum-computers/our-quantum-computers_en) | - | •&nbsp;[PIAST-Q](https://quantum.psnc.pl/en/piast-q/) | •&nbsp;[VLQ quantum computer](https://www.it4i.cz/en/infrastructure/vlq-quantum-computer) |
| Accounts | - | •&nbsp;[IDM-Portal 2](https://idmportal2.lrz.de/)<br>•&nbsp;[Munich Quantum Portal](https://portal.quantum.lrz.de/) | - | •&nbsp;[VLQ, Access](https://docs.it4i.cz/en/docs/clusters/vlq/access)<br>•&nbsp;[LEXIS portal](https://portal.lexis.tech)<br>•&nbsp;[LEXIS login guide](https://docs.lexis.tech/user_interfaces/howto_register.html) |
| Submit jobs | - | - | - | •&nbsp;[VLQ, Access](https://docs.it4i.cz/en/docs/clusters/vlq/access) |
| HPC-QC jobs | - | •&nbsp;[HPCQC System Access and HPCQC Job Submission via MQSS-Adapter](https://doku.lrz.de/documentation-hpcqc-system-access-and-hpcqc-job-submission-via-mqss-adapter-2603423874.html)<br>•&nbsp;[MQSS Interfaces Documentation](https://munich-quantum-software-stack.github.io/MQSS-Interfaces/) | - | - |
| Time counted | - | •&nbsp;[Definition of the computing unit for the LRZ Quantum Systems](https://doku.lrz.de/definition-of-the-computing-unit-for-the-lrz-quantum-systems-1898715012.html) | - | •&nbsp;[Estimating Consumption on VLQ](https://docs.it4i.cz/en/docs/clusters/vlq/vlq-consumption-guide) |
| Calibration | - | - | - | •&nbsp;[VLQ Calibration API](https://extranet.it4i.cz/vlq-calibration/) |
| Acknowledge | - | •&nbsp;[Acknowledgement formulations](https://doku.lrz.de/acknowledgement-formulations-2495480854.html) | - | •&nbsp;[Acknowledgments in publications](https://www.it4i.cz/en/for-users/acknowledgments-in-publications) |

For the SSH steps to LRZ's HPC-QC system, see {ref}`reaching-lrz-hpcqc`.
