![Maven build](https://github.com/jeanjerome/archetypes-mixture/workflows/Java%20CI%20with%20Maven/badge.svg?branch=develop)
[![GitHub release](https://img.shields.io/github/release/jeanjerome/archetypes-mixture.svg?style=flat-square)](https://github.com/jeanjerome/archetypes-mixture)

# archetypes-mixture
How to generate different kinds of application architectures without maintaining redundant archetypes code?

Well, start to define one archetype per application layer and mixe them as you want in a multi-module project. Even more, adjust the taste with your favorite flavors like springbooting, microservices or authentication and you'll get a sophisticated and easy to maintain developer stack.

All of this can be done with simple Maven commands and its Maven archetype plugin and Velocity template engine.

!!! This is (only) a POC demonstrating the feasibility of such solutions not a multi-architecture archetype able to generate all kind of applications... sorry for that !!!

## How to test it?

### 1. Build and install the archetypes
Run the bash script (on Windows, just run the included commands) `mvn-install-local.sh`.
This will build 1 POM (`archetype-bundles`) and 3 Maven Archetypes (`archetype-parent`, `archetype-client`, `archetype-server`) and install them to your local Maven repository (`~/.m2/repository`)

### 2. (Optional) Generate the archetypes' sites documentation
Run the bash script (on Windows, just run the included commands) `mvn-site.sh`.

### 3. Generate your app
Run the bash script `mvn-generate-app.sh` (or the included commands).
This will create a fully functional app composed of the 3 previous built archetypes.

## What does this demonstrate?

1. You can apply different Maven archetypes on the same project (even multi-module ones) runnig the portable command `mvn:generate` several times.

1. Velocity templates lets add customization when executing Maven archetypes.

1. You can split an archetype in multiple parts, each one dedicated to a tier (angular, api, service, dao,...) or a functionality (security, microservice, Springboot, DDD, container,...).

## Disclaimer

1. This is a basic demo yet!

1. More complex cases have to be tested to prove real efficiency in such solution mostly on functionalities!
