cfacter-build
=============
## Basics

### Prepare

For S10
```
s10# /opt/csw/bin/pkgutil -y -i git
s10# /opt/csw/bin/pkgutil -y -i tmux  # optional
```

For s11
```
s11# pkg install git
```

#### Checkout
```
git clone https://github.com/puppetlabs/cfacter-build
```


### Prepare
```
cd cfacter-build
sudo gmake prepare
```

### Build it
```
gmake build
```

### Now for sparc
```
gmake build arch=sparc
```

The cfacter gets built in `./build/<arch>/cfacter-<ver>`

## Intermediate

### Uninstall all we installed
```
sudo gmake uninstall
```
### Return to the check-out state
```
gmake clobber
```

I typically invoke `sudo gmake uninstall prepare; gmake clobber` to start anew.
