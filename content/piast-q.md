# A few details on Piast-Q

- A broker API with an API key in a header.
- You send the native gate list directly, and two conventions catch everyone: angles are in units of
  pi, and there must be exactly one measurement, at the end.
- Plan depth against coherence, not against your time budget.
- Two limits: 200 shots per job, and a limit on concurrent connections. PCSS's troubleshooting text
  names the answer `HTTP error 429 response: max connections reached` but gives no number, so keep
  one connection open at a time.
- For the site's page on the machine, open: [PCSS: PIAST-Q](https://quantum.psnc.pl/en/piast-q/)
