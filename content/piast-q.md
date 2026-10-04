# A few details on Piast-Q

- A broker API with an API key in a header.
- You send the native gate list directly, and two conventions catch everyone: angles are in units of
  pi, and there must be exactly one measurement, at the end.

- A 200-shot job takes between about 60 and 145 seconds, most of it ion cooling rather than gates.
- Fixed overhead dominates to at least a couple of hundred gates, with a real depth cost beyond that,
  so in time terms job count is the scarce resource, the opposite of the intuition most people bring
  from superconducting hardware.

- Plan depth against coherence, not against your time budget.

- Two limits: 200 shots per job, and at most four concurrent connections to the machine.
- Exceeding the connection limit returns an error while the job itself completes fine.

- Piast-Q publishes quality windows, hours during which the machine is calibrated for user work.
- Results outside them are provisional.

- For the site's page on the machine, open: [PCSS: PIAST-Q](https://quantum.psnc.pl/en/piast-q/)
