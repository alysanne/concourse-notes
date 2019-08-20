# Concourse 101 🚀

## Getting started

To start a local version of Concourse for testing purposes:

1. Download or clone the repository with the test files and the initial docker file with a containerised concourse instance:

```
$ wget https://raw.githubusercontent.com/starkandwayne/concourse-tutorial/master/docker-compose.yml
```

2. Start the docker container with the concourse instance:

```
$ docker-compose up -d
```

3. The instance will be available in http://127.0.0.1:8080/


## Login in the CLI

The first step to be able to access your concourse instance via CLI is to login. We do this by using `fly login` and providing the URL of our instance.

The `login` command will attempt to login to a specified target (provided with the `-t` or `--target` flag). If the target doesn't exist it will create it and save it linked to the provided URL.

```
$ fly -t my-concourse login --concourse-url https://ci.my-concourse-instance.com
```


## Syncing the fly version

The version of `fly` that you use should be in sync with the version of concourse used by the instance. To check and update we can use the `fly sync` command:

```
$ fly -t my-concourse sync
```
