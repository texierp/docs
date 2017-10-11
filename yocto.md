Yocto/OE
========

# DNF


## Côté HOST
```console
$: bitbake package-index
$: cd tmp/deploy/rpm
$: python -m SimpleHTTPServer
```

## Côté TARGET

```console
$: mkdir -p /etc/yum.repos.d
$: vi /etc/yum.repos.d/<machine>.repo
```

Il faut éditer le fichier, exemple:


```
[warp7]
name=WaRP7 repo
baseurl=http://<host ip addr or hostname>:8000
enabled=1
metadata_expire=0
gpgcheck=0
```
