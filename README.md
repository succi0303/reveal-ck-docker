# reveal-ck-docker

`reveal-ck` is a great command-line tool that helps creating reveal.js presentation.

- [reveal-ck](http://jedcn.github.io/reveal-ck/)

This docker image is for executing reveal-ck in isorated environment.

## Usage

## Run docker image

Specify `-p 10000:10000` to access the reveal-ck web server.

```bash
$ docker -it --rm -v $(pwd):/usr/src -p 10000:10000 succi0303/reveal-ck bash
```

### Generate slide files (in docker image)

```bash
$ reveal-ck generate
```

### Start web server to show the slide

`-h 0.0.0.0` is required to access from outside of the container.

```bash
$ reveal-ck serve -h 0.0.0.0 # Access http://localhost:10000 in web browser
```
