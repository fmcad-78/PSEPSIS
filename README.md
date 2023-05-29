This repository contains code for a Sepsis Screening and Management Application
powered by the [MediK language](https://github.com/fmcad-78/medik-semantics)

## Building

1. Use `git submodule update --init --recursive` to fetch relevant dependencies.
2. `./docker-build` to build a docker image with all relevant.
3. `./docker-run` to launch drop into a container with relevant dependencies. In
the container, run `./container-build` to build the medik semantics, and run
both execution/model-checking tests. This may take several minutes to complete.

## Running

1. In the container, run `./psepsis-app` to launch the psepsis application.
2. From a browser, navigate to `http://127.0.0.1:22222` to access the
   main application, and to `http://127.0.0.1:22223` to access an interface
   that to enter mock patient parameters.

