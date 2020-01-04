<h1 align="center">8 factor app</h1>
<h5 align="center">Adapted from <a href="https://www.12factor.net" target="_blank">Heroku's 12factor</a></h5>


## I. Test

Create test case for code under development, try [tdd](https://martinfowler.com/bliki/TestDrivenDevelopment.html) as maximum as you can.

> Always test your code.

## II. Codebase

One codebase tracked in revision control, many deploys [more here](https://12factor.net/codebase)

> Always use git for your code/scripts/snippets and push to skore's github.

## III. Dependencies

Explicitly declare and isolate dependencies [more here](https://12factor.net/dependencies)

> Use [tilde dependencies](https://docs.npmjs.com/cli/update.html#tilde-dependencies)(`~`) on npm

## IV. Config

Store config in the environment [more here](https://12factor.net/config)

> Use [.env](https://github.com/motdotla/dotenv) to avoid leaks on sensitive application configs and separate them by our environments (**dev**, **staging**, **prod**)

## V. Backing services

Treat backing services as attached resources [more here](https://12factor.net/backing-services)

> Code should not be changed depending on environment, config value yes.

## VI. Build, release, run

Strictly separate build and run stages [more here](https://12factor.net/build-release-run)

> Always separate this processes. Testing, validation, rollback and scaling becomes easier.

## VII. Dev/prod parity

Keep development, staging, and production as similar as possible [more here](https://12factor.net/dev-prod-parity)

> Always have this three environments.

## VIII. Logs

Treat logs as event streams [more here](https://12factor.net/logs)

> Always send logs to our logstash
