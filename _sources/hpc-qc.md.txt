# HPC and HPC-QC

EuroHPC JU describes its quantum computers as "hosted in Europe and tightly coupled to EuroHPC
supercomputers" ([Quantum Computing &
Access](https://www.eurohpc-ju.europa.eu/quantum-technologies/quantum-computing-access_en)). Its
[list of quantum
computers](https://www.eurohpc-ju.europa.eu/eurohpc-quantum-computers/our-quantum-computers_en)
names a hosting supercomputer for each: SuperMUC-NG for Euro-Q-Exa, ALTAIR for Piast-Q and KAROLINA
for VLQ.

Quantum access runs through the same [EuroHPC access portal](https://access.eurohpc-ju.europa.eu/)
as classical HPC time, on monthly cut-offs. The application form asks for classical resources in node hours, while sites often discuss them in GPU hours. See {doc}`qpu-hours`.

## What each site describes

:::::{tabs}
::::{group-tab} Euro-Q-Exa

**LRZ.** EuroHPC JU's list says the system is integrated into the LRZ supercomputer "via a unified
hybrid software environment". LRZ's documentation describes a cluster of its BEAST testbed "used for
hybrid HPCQC workflows", with HPC compute nodes "tightly integrated with the Quantum Server".

Quantum jobs are submitted from the HPC system through the MQSS-Adapter, in a Slurm job script that
requests the QPU (`--gres=qpu:iqm_eqe1:1`). The page notes that HPCQC "is supported by demand", with
access requested from LRZ through its service desk.

The [MQSS Interfaces documentation](https://munich-quantum-software-stack.github.io/MQSS-Interfaces/) describes two access points: the Munich Quantum Portal, and "a high-performance computing (HPC) access point for users working on local or institutional HPC resources".

To get HPCQC system access and submit HPCQC jobs, open: [LRZ: HPCQC System Access and HPCQC Job
Submission via
MQSS-Adapter](https://doku.lrz.de/documentation-hpcqc-system-access-and-hpcqc-job-submission-via-mqss-adapter-2603423874.html)

::::
::::{group-tab} VLQ

**IT4Innovations** lists VLQ as "integrated into the EuroHPC supercomputer
KAROLINA". Its access documentation says the Python environment is installed on the machine you
execute circuits from, which may be a compute node "of any HPC system (LUMI, Karolina, Vega,
Meluxina, etc.), or your desktop, laptop or any other computer of your choice". Submission then goes
through HEAppE, which is a job-submission middleware rather than a quantum service.

For the site's page on the machine, open: [IT4Innovations: VLQ quantum
computer](https://www.it4i.cz/en/infrastructure/vlq-quantum-computer)

For the access documentation, open: [IT4Innovations: VLQ,
Access](https://docs.it4i.cz/en/docs/clusters/vlq/access)

::::
::::{group-tab} Piast-Q

**PCSS** states that the quantum computer "is integrated with a classical supercomputing
system at PCSS to enhance hybrid quantum-classical computing approaches". What the hybrid route
needs is in {doc}`onboarding`.

For the site's page on the machine, open: [PCSS: PIAST-Q](https://quantum.psnc.pl/en/piast-q/)
::::
:::::

(reaching-lrz-hpcqc)=

## Reaching LRZ's HPC-QC system

[LRZ's
page](https://doku.lrz.de/documentation-hpcqc-system-access-and-hpcqc-job-submission-via-mqss-adapter-2603423874.html)
describes BEAST as "an HPC testbed system at LRZ for researching and testing emerging technologies",
with a cluster called Wolpertinger "used for hybrid HPCQC workflows". Access is on request, as noted
above. The login node "is not public", so you log in to a gateway first.

1. **Configure SSH:** this follows the SSH configuration LRZ documents, in `~/.ssh/config`:

   ```text
   Host qclogin
       HostName qclogin.srv.lrz.de
       User <username>
       ServerAliveInterval 90

   Host beast-login
       HostName login.beast.lrz.de
       User <username>
       ProxyJump qclogin
       ServerAliveInterval 90
   ```
2. **Install your public key on both hosts**: `ssh-copy-id qclogin`,
   then `ssh-copy-id beast-login`.
3. **Log in** with one command: `ssh beast-login`.
4. **To inspect the partition and your jobs:** `sinfo -p wolpy` and `squeue -u $USER`. The `wolpy` partition listed both GPUs and QPUs as Slurm generic resources.

## Further reading

Papers on HPC-QC integration from LRZ and its Munich Quantum Software Stack partners. The first and
the last concern a 20-qubit system at LRZ.

- Mansfield et al., "First Practical Experiences Integrating Quantum Computers with HPC Resources: A
  Case Study With a 20-qubit Superconducting Quantum Computer",
  [arXiv:2509.12949](https://arxiv.org/abs/2509.12949), 2025: reports the integration of a
  superconducting 20-qubit quantum computer into the HPC infrastructure at LRZ, and the lessons
  drawn.
- Burgholzer et al., "The Munich Quantum Software Stack: Connecting End Users, Integrating Diverse
  Quantum Technologies, Accelerating HPC", [arXiv:2509.02674](https://arxiv.org/abs/2509.02674),
  2025: describes the stack, including front-end adapters, an HPC-integrated scheduler, a compiler
  and the Quantum Device Management Interface (QDMI).
- Burgholzer et al., "Practical HPCQC Integration with QDMI: A Real-Hardware Case Study with IQM
  Systems", [arXiv:2604.19869](https://arxiv.org/abs/2604.19869), 2026: a case study of HPCQC
  integration through QDMI on real hardware.
- Farooqi et al., "Enabling Hybrid HPCQC Workflows with a Heterogeneous Software Stack",
  [arXiv:2608.14827](https://arxiv.org/abs/2608.14827), 2026: describes hybrid workflows in which
  Slurm exposes QPUs as generic resources and the MQSS compiles and dispatches the circuits.
