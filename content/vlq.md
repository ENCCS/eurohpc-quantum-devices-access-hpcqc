# A few details on VLQ

- Submission goes through HEAppE, and a circuit takes two jobs, because the service builds the
  backend object on its own side:
  1. an initialisation job on a short queue, which produces the backend description, and
  2. an execution job on a longer queue, which consumes that description and runs your circuit.
- Your circuit is staged as an OpenQASM file into the job's working directory between creating the
  job and submitting it.
- To follow the site's access steps, open: [IT4Innovations: VLQ,
  Access](https://docs.it4i.cz/en/docs/clusters/vlq/access)

- The circuit must already be native and mapped.

- Read the architecture from the machine.
- Calibration moves, so read it at submission time.
- For the calibration data, open: [IT4Innovations: VLQ Calibration
  API](https://extranet.it4i.cz/vlq-calibration/)
- The machine status (QPU, control software, scheduler) and the current calibration set are public,
  with no login needed. For both, open: [IT4Innovations: VLQ, Calibration and
  Health](https://docs.it4i.cz/en/docs/clusters/vlq/calibration_health)

- Authentication is a federated identity token.
- The access token lasts six hours.
- You get the token through a LEXIS login: the client opens or prints a link, and you log in in a
  browser, as IT4Innovations' access page shows.
- Install the client version that IT4Innovations' access page shows. The client's public code
  checks its version against the server's and refuses a different major or minor version.

## Official pages

- For the site's page on the machine, open: [IT4Innovations: VLQ quantum
  computer](https://www.it4i.cz/en/infrastructure/vlq-quantum-computer)
- For the acknowledgement wording, open: [IT4Innovations: Acknowledgments in
  publications](https://www.it4i.cz/en/for-users/acknowledgments-in-publications)
- To read how to log in to LEXIS, open: [LEXIS Platform: LEXIS Platform
  Login](https://docs.lexis.tech/user_interfaces/howto_register.html)
