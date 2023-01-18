# wazo-python-sqlalchemy-continuum-packaging

Debian packaging for [python-sqlalchemy-continuum](https://github.com/kvesteri/sqlalchemy-continuum.git) used in Wazo.

## Upgrading

To upgrade python-sqlalchemy-continuum

* Update the version number in the `VERSION` file
* Update the changelog using `dch -i` to the matching version

## Building Locally

To build on a test environment before submitting a change to production the following procedure can be used.

```sh
make -f debian/rules get-orig-source
tar -xvf ../wazo-python-sqlalchemy-continuum-packaging_*.orig.tar.gz  --strip 1
dpkg-buildpackage -us -uc
```
The `.deb` will be located in the parent directory.
