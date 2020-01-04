ACLOCAL_AMFLAGS = --install -I m4

SUBDIRS = liblwgeom src

noinst_HEADERS=postgis_config.h \
               postgis_svn_revision.h

EXTRA_DIST = \
    LICENSE \
    README.md

echo-version:
	@echo $(VERSION)

tag:
	cd $(top_srcdir) && git tag v$(VERSION) -a -m 'shp2mysql $(VERSION)'

dist-source: distdir
	mv $(distdir) shp2mysql-source
