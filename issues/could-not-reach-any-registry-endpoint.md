---
layout: doc
sublayout: issue
title: Could not reach any registry endpoint
reviewed: 2017-04-27T00:00:00-04:00
frontpage: True
---

Attempting to pull a docker image results in an error like the following:

```
$ docker pull quay.io/coreos/etcd
Pulling repository quay.io/coreos/etcd
Could not reach any registry endpoint
```

### You are attempting to pull a non-existant tag (probably "latest")

While the error message is extremely cryptic, you are likely attempting to pull a tag that does not exist.
If you do not specify a tag, newer versions of docker will attempt to pull the "latest" tag regardless of its existance.
