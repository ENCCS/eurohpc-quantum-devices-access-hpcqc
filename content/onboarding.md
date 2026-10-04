# Onboarding

Once you are granted access, and at the time of writing, onboarding takes a separate process for each device you applied for. Yet as mentioned in the access page, there is one application and one portal. The diagram below shows the onboarding process so far for three of the devices.

:::{note}
These steps may change going forward, as the hosting sites update their procedures. Check each
site's official documentation for the current process. Keep an eye on
[my-eurohpc.eu](https://my-eurohpc.eu/) for updates on access methods, and follow
[ENCCS on LinkedIn](https://www.linkedin.com/company/enccs) for further updates.
:::

```{figure} _static/onboarding.drawio.png
:alt: Block diagram. One application in the EuroHPC access portal leads to a technical assessment, one per hosting site, and then to an award, one per machine. From the award, three separate onboarding paths lead to a first circuit. LRZ, Euro-Q-Exa, export-control declaration signed by every team member, account, Munich Quantum Portal, API token created in the portal. PCSS, Piast-Q, API key issued. IT4Innovations, VLQ, MyAccessID registration, access to a LEXIS project, resource assigned to the project.
:width: 100%

One application, then an award and a separate onboarding for every machine.
```

## Details per site/machine

:::::{tabs}
::::{group-tab} Euro-Q-Exa

**LRZ, [Euro-Q-Exa](https://www.lrz.de/en/news/detail/first-european-quantum-computer-for-germany-euro-q-exa-starts-operation-at-lrz).** A signed export-control declaration goes back to the site, after which you receive an
account and can log into the [Munich Quantum Portal](https://portal.quantum.lrz.de/). You then
create an API token in the portal yourself.

Two things to watch at LRZ. First, the export-control declaration is signed and returned by every
team member named on the proposal, not just the applicant, so each of them has to be prompted.
Second, check your account's expiry date against your allocation period.

- To manage your LRZ account and password, open: [LRZ: IDM-Portal 2](https://idmportal2.lrz.de/)
- To log in, open: [LRZ: Munich Quantum Portal](https://portal.quantum.lrz.de/)
- For the HPC-QC use case, open: [LRZ: HPCQC System Access and HPCQC Job Submission via
  MQSS-Adapter](https://doku.lrz.de/documentation-hpcqc-system-access-and-hpcqc-job-submission-via-mqss-adapter-2603423874.html)


::::
::::{group-tab} VLQ

**IT4Innovations, [VLQ](https://www.it4i.cz/en/infrastructure/vlq-quantum-computer).** You register with MyAccessID, then request access to a named
project in the LEXIS platform, and the site assigns a resource to that project. Submission then goes
through HEAppE, which is a job-submission middleware. Keep three identifiers apart: your LEXIS project short name, the resource name, and the project as the submission middleware knows it.

- To follow the site's access steps, open: [IT4Innovations: VLQ,
  Access](https://docs.it4i.cz/en/docs/clusters/vlq/access)
- To log in to LEXIS, open: [LEXIS Platform: portal](https://portal.lexis.tech)
- To read how to log in to LEXIS, open: [LEXIS Platform: LEXIS Platform
  Login](https://docs.lexis.tech/user_interfaces/howto_register.html)

::::
::::{group-tab} Piast-Q

**PCSS, [Piast-Q](https://quantum.psnc.pl/en/piast-q/).** The simplest to onboard of the three: you are issued an API key and you use it. So far, no account, no portal and no forms are needed for direct submission. The hybrid route, which couples to classical resources at the same site, additionally needs an institution account and a VPN certificate.

::::
:::::
