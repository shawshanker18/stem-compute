# stem-compute

Compute runner for a private project. This repository holds **workflows only, never code**:
each job clones the private repositories read-only, runs one case, prints nothing from the code,
and uploads its results encrypted with the project's public key.

| workflow | what |
|---|---|
| `car.yml` | the farm: one job per case of a batch |
| `ci.yml` | the test suites and the golden-car rebuild |
| `capacity.yml` | measures how many jobs this account runs at once |
| `image.yml` | builds the OpenFOAM + Python container image (no project code) |

Triggers are `workflow_dispatch` only. Created and updated by `compute/setup_compute_repos.py`
in the private `part3-simulation` repository. Ask the owner before deleting it.
