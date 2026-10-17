# "QPU hours" on the devices

::::::{tabs}
:::::{group-tab} Euro-Q-Exa

**Euro-Q-Exa** bills in equivalent qubit-seconds: wall-clock time on the device, scaled by qubit
count and by one-qubit gate time. The formula is as follows:

```{math}
\mathrm{eqs}(S) = t \times n(S) \times \frac{T_{1qg}(\text{Q-Exa})}{T_{1qg}(S)}
```

- {math}`t`: wall-clock time on the QPU.
- {math}`n(S)`: number of qubits in system {math}`S`.
- {math}`T_{1qg}(S)`: one-qubit gate time of {math}`S`; Q-Exa is the reference system.

- For LRZ's definition of the unit, open: [LRZ: Definition of the computing unit for the LRZ Quantum Systems](https://doku.lrz.de/definition-of-the-computing-unit-for-the-lrz-quantum-systems-1898715012.html)

:::::
:::::{group-tab} VLQ

**VLQ** bills device execution time, measured between execution start and end on the hardware
itself. Classical overhead, staging and result handling fall outside the meter, so a slow client
costs you nothing.

IT4Innovations publish the billing formula, the per-shot cost, a minimum charge of 0.9 seconds per job, worked
examples, and an explicit statement that queue latency is not billed. Their own figures imply a
useful rule: below roughly 2,250 shots you pay the floor anyway, so submit few large jobs rather
than many small ones.

The formula is as follows:

```{math}
\text{billed time [s]} = N_\text{jobs} \times \max\left(N_\text{shots} \times c,\; 0.9\right)
```

- {math}`N_\text{jobs}`, {math}`N_\text{shots}`: number of jobs, and shots per job.
- {math}`c`: cost per shot, 400 µs as the worst case, or 350 µs plus the actual circuit time.
- 0.9 s: the minimum charge per job.

- To estimate consumption on VLQ, open: [IT4Innovations: Estimating Consumption on
  VLQ](https://docs.it4i.cz/en/docs/clusters/vlq/vlq-consumption-guide)

:::::
:::::{group-tab} Piast-Q

**Piast-Q** bills device time, which the site defines as time on the machine including ion loading
and re-initialisation, and excluding queue wait, network round-trips and time your client spends
waiting.

:::::
::::::

Classical resources are in node hours, as we are all used to. Sites could discuss them in GPU hours.
