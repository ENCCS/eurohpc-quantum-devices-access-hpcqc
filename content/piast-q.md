# A few details on Piast-Q

- A broker API with an API key in a header.
- You send the native gate list directly, and two conventions catch everyone: angles are in units of
  pi, and there must be exactly one measurement, at the end.
- Plan depth against coherence, not against your time budget.
- Two limits: 200 shots per job, and at most four concurrent connections to the machine.
- Exceeding the connection limit returns an error while the job itself completes fine.
- For the site's page on the machine, open: [PCSS: PIAST-Q](https://quantum.psnc.pl/en/piast-q/)
