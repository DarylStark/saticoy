# Saticoy

Saticoy is a personal project of Daryl Stark. The software will be a containerized micro-service architecture that is deployable to the cloud. By using GitHub Actions as CI/CD tool, the software will be tested, published and deployed automatically. This repository contains the details about the project, but doesn't contain any source code.

# Code repositories

Each microservice will be a in a separate repository, hosted on GitHub. It is possible that multiple microservices use a library that is shared. These libraries will be in a separate repository too. Development tools, like CI/CD pipelines and repository templates will be in separate repositories on GitHub too.

## Repository naming convention

Each repository for Saticoy will be named using a naming convention. This convention makes sure that the name of the repository gives a clear indication of what the repository is used for. The name of a repository has a few fields:

`saticoy-<type>-<specific-type>-<short description>`

The following fields are used

-   `saticoy`: each repository name will start with the word `saticoy` to make it clear that the repository is a part of the Saticoy project.
-   `<type>`: the type inidicates what kind of software is created within this repository. It is always three letters and can be any of these:
    -   `svc`: a microservice. The repository contains the code for the microservice and a `Dockerfile` or `Containerfile` to create a containerimage for the microservice.
    -   `lib`: a library that can be used by other Saticoy microservices. This can be a library to interact with specific database services, for instance.
-   `<specific-type>`: the specific type is a two letter identifier that specifies the subtype:
    -   If the `type` is `svc`, this can be:
        -   `fe`: front-end service
        -   `be`: back-end service
    -   If the `type` is `lib`, this indicates the programming language for the library:
        -   `py`: Python library
        -   `ts`: TypeScript library
-   `<short-description>`: a short description of the repository software in lowercase separated by dashes. For example: `authentication-manager`.