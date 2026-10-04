# EuroHPC JU quantum devices and HPC-QC access in practice

The [EuroHPC Joint Undertaking](https://www.eurohpc-ju.europa.eu/index_en) now offers quantum
computers that you can apply to use and, if your application is granted, use free of charge. This
lesson is a practical guide to getting onboarded and running your first jobs on three of them:
[Euro-Q-Exa](https://www.lrz.de/en/news/detail/first-european-quantum-computer-for-germany-euro-q-exa-starts-operation-at-lrz)
at [LRZ](https://www.lrz.de/en), [Piast-Q](https://quantum.psnc.pl/en/piast-q/) at
[PCSS](https://www.psnc.pl/) and [VLQ](https://www.it4i.cz/en/infrastructure/vlq-quantum-computer)
at [IT4Innovations](https://www.it4i.cz/en).

:::{important}
Always refer to the official documentation for the most up-to-date details. The official pages are
gathered in one table, {ref}`Official links, by task <official-links>`.
:::

:::{seealso}
**Start with the overview.** ENCCS's 2025 white paper, [Quantum Computing in the EuroHPC JU
Ecosystem: A Practical Guide for European SMEs](https://doi.org/10.5281/zenodo.17862354), surveys
the EuroHPC quantum computers. This lesson is the hands-on follow-up for three of them.
:::

:::{prereq}

- Basic familiarity with quantum circuits: qubits, gates, shots, and what a Bell pair is.
- The command line, and enough Python to read a short script.
:::

```{toctree}
:caption: The lesson
:maxdepth: 1

access
onboarding
machines
hpc-qc
euro-q-exa
vlq
piast-q
qpu-hours
```

```{toctree}
:caption: Reference
:maxdepth: 1

quick-reference
```

## Acknowledgement

This work used EuroHPC Joint Undertaking quantum resources awarded under the Quantum Access call, hosted by LRZ, IT4Innovations and PCSS. We thank the support teams at
all three sites.

Each site asks for its own wording, reproduced here as supplied:

> We acknowledge EuroHPC JU for awarding project with ID 22/2026 access to the EuroHPC allocation on
> the Piast-Q trapped-ion quantum computer hosted by the Poznan Supercomputing and Networking Center

> The authors gratefully acknowledge the use of the quantum system Euro-Q-Exa, co-funded by the
> EuroHPC JU, BMFTR (grant 13N16690), and the Bavarian State Ministry of Science and the Arts,
> operated by the Leibniz Supercomputing Centre (LRZ) in Garching, Germany, for providing the
> computational resources for this work.

> This work was supported by the Ministry of Education, Youth and Sports of the Czech Republic
> through the e-INFRA CZ (ID:90254)

- For LRZ's wording, open: [LRZ: Acknowledgement formulations](https://doku.lrz.de/acknowledgement-formulations-2495480854.html)
- For IT4Innovations' wording, open: [IT4Innovations: Acknowledgments in publications](https://www.it4i.cz/en/for-users/acknowledgments-in-publications)

ENCCS is the EuroCC National Competence Centre Sweden, part of the EuroCC 3 project (grant
101306701), with partners Linköping University and RISE Research Institutes of Sweden.

## See also

::::{admonition} Licence
:class: attention

:::{admonition} CC BY-SA for media and pedagogical material
:class: attention dropdown

Copyright © ENCCS contributors. This material is released by ENCCS under the Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0).

**Canonical URL**: <https://creativecommons.org/licenses/by-sa/4.0/>

[See the legal code](https://creativecommons.org/licenses/by-sa/4.0/legalcode.en)

## You are free to

1. **Share**: copy and redistribute the material in any medium or format for any purpose, even commercially.
2. **Adapt**: remix, transform, and build upon the material for any purpose, even commercially.
3. The licensor cannot revoke these freedoms as long as you follow the license terms.

## Under the following terms

1. **Attribution**: You must give [appropriate credit](https://creativecommons.org/licenses/by-sa/4.0/#ref-appropriate-credit) , provide a link to the license, and [indicate if changes were made](https://creativecommons.org/licenses/by-sa/4.0/#ref-indicate-changes) . You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
2. **ShareAlike**: If you remix, transform, or build upon the material, you must distribute your contributions under the [same license](https://creativecommons.org/licenses/by-sa/4.0/#ref-same-license) as the original.
3. **No additional restrictions**: You may not apply legal terms or [technological measures](https://creativecommons.org/licenses/by-sa/4.0/#ref-technological-measures) that legally restrict others from doing anything the license permits.

## Notices

You do not have to comply with the license for elements of the material in the public domain or where your use is permitted by an applicable [exception or limitation](https://creativecommons.org/licenses/by/4.0/deed.en#ref-exception-or-limitation) .

No warranties are given. The license may not give you all of the permissions necessary for your intended use. For example, other rights such as [publicity, privacy, or moral rights](https://creativecommons.org/licenses/by/4.0/deed.en#ref-publicity-privacy-or-moral-rights) may limit how you use the material.

This deed highlights only some of the key features and terms of the actual license. It is not a license and has no legal value. You should carefully review all of the terms and conditions of the actual license before using the licensed material.

:::

:::{admonition} MIT for source code and code snippets
:class: attention dropdown

MIT License

Copyright (c) ENCCS contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

:::

::::
