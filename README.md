elasticsearch-dpkg
==================

elasticsearch dpkg packaging for debian.

The official elasticsearch configuration files are supplied and only adjusted to the correct paths.

Create source packages step by step:

```
git clone https://github.com/elasticsearch/elasticsearch.git elasticsearch-1.0.0.RC1
cd elasticsearch-1.0.0.RC1
git checkout v1.0.0.RC1
tar czf ../elasticsearch_1.0.0.RC1.orig.tar.gz ../elasticsearch-1.0.0.RC1
git clone https://github.com/1and1/elasticsearch-dpkg.git debian
cd ..
dpkg-source -b elasticsearch-1.0.0.RC1
```

Now the binary package can be built with dpkg-buildpackage or pbuilder the usual way.
