This repository contains code for a Sepsis Screening and Management Application
powered by the [MediK language](https://github.com/fmcad-78/medik-semantics)

## Building

1. Use `git submodule update --init --recursive` to fetch relevant dependencies.
2. `./docker-build` to build a docker image with all relevant.
3. `./docker-run` to launch drop into a container with relevant dependencies. in
the container, run `./container-build` to build the medik semantics, and run
both execution/model-checking tests. This may take several minutes to complete.

## Running


1. In the container, run `./psepsis-app` to launch the psepsis application.
2. Since using real-patient data through sensors is not possible, we rely on
   a simple web-based portal to manually enter simulated data. To access said
   portal, navigate to `http://127.0.0.1:22223` from a web-browser, after
   starting the application (step 1).
3. From a browser, navigate to `http://127.0.0.1:22222` to access the
   main application.

To restart the application:
 1. Close existing tabs from steps 2, 3.
 2. From the container, kill the nodejs server using `pkill node`,
    and re-launch the tabs.


