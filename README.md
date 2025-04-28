# targetDART Containers

Build the targetDART runtime and ExaHyPE application as follows:

```bash
docker build -f Dockerfile.base -t targetdart/base .
docker build -f Dockerfile.spack -t targetdart/spack .
docker build -f Dockerfile.runtime -t targetdart/runtime .
docker build -f Dockerfile.exahype -t targetdart/exahype .
```

Per default the ExaHyPE image builds the application in its baseline configuration. Amend the ExaHyPE Dockerfile according to the artifact description to enable support for the targetDART runtime.

Execute the simulation as follows:

```bash
docker run --rm --gpus=all --privileged targetdart/exahype
```
