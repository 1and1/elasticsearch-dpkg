elasticsearch-dpkg
==================

elasticsearch dpkg packaging for debian.

The official elasticsearch configuration files are supplied and only adjusted to the correct paths.

Create source packages step by step:

```
git clone https://github.com/elasticsearch/elasticsearch.git elasticsearch-1.5.1
cd elasticsearch-1.5.1
git checkout v1.5.1
git clone https://github.com/lmenezes/elasticsearch-kopf.git
cd elasticsearch-kopf
git checkout v1.5.0
cd ..
git clone https://github.com/leeadkins/elasticsearch-redis-river.git
cd elasticsearch-redis-river
git checkout v0.0.5
cd ..
tar czf ../elasticsearch_1.5.1.orig.tar.gz ../elasticsearch-1.5.1
git clone https://github.com/1and1/elasticsearch-dpkg.git debian
cd ..
dpkg-source -b elasticsearch-1.5.1
```

Now the binary package can be built with dpkg-buildpackage or pbuilder the usual way.
