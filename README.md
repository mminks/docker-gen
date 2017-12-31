docker-gen
=====

This is a fork of original [docker-gen](https://github.com/jwilder/docker-gen) which always installs the **latest** version of `docker-gen`.

Additionally it includes latest Alpine `bash` and `cli53`, a command line tool for Amazon Route 53. See https://github.com/barnybug/cli53 for more information on this.

I need it for a special use-case with my infrastructure.

### Installation

This is a ready to run docker image.

Example:
```
$ docker run -d \
   -v /var/run/docker.sock:/tmp/docker.sock:ro \
   -v /tmp/templates:/etc/docker-gen/templates \
   -t mminks/docker-gen -notify-sighup nginx -watch -only-exposed /etc/docker-gen/templates/nginx.tmpl /etc/nginx/conf.d/default.conf
```

### Usage

Please visit Jason's [original repository](https://github.com/jwilder/docker-gen) for detailed usage instructions.