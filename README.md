# Basilisk -- Continuous Benchmarking for Triplestores

Triplestores -- the database backend of knowledge graphs -- are typically developed in long iterations and are bench-marked -- if at all -- only in a very late stage of such an iteration. Benchmarking and evaluation of benchmarking results are typically done manually and binds developer's time. Thus, performance regressions are found very late or never.  

With Basilisk we started to develop a continuous benchmarking platform for triplestore which hooks into github and docker image registries.  

On events like pull requests or newly published versions of triplestores, a benchmarking suite is run automatically.  

The first version of [Basilisk](https://github.com/dice-group/Basilisk), [Basilisk Frontend](https://github.com/dice-group/basilisk-frontend) is already implemented. It is based on the benchmarking tool [IGUANA](https://github.com/dice-group/IGUANA) and Docker. (It requires triple stores to be dockerized).  

The thesis task is to:  
1. describe and review the software architecture  
2. deploy Basilisk and its frontend on a publicly available VM  
3. benchmark 2 versions of [Tentris](https://github.com/dice-group/tentris), via a github hook) and one version from another triple store (via a docker image registry, e.g. [https://hub.docker.com/r/ontotext/graphdb/](https://hub.docker.com/r/ontotext/graphdb/) or [https://hub.docker.com/r/openlink/virtuoso-opensource-7](https://hub.docker.com/r/openlink/virtuoso-opensource-7)).  
4. fix critical bugs in 1.-3. and document non-critical 
