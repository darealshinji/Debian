include ../../mk/include.mk

deps           = wget
bin            = crayon_release_demo.tgz
distcleanfiles = $(bin)
srcfiles       = $(bin) ../../mk/make-icons.sh

download:
	@ $(call download,$(bin),http://crayonphysics.com/downloads/crayon_release55demo_hotfix.tar.gz)
	@ $(call verifysha256,$(bin),ea3a129eaf2a49d4c23cfcce7ccac4815da3569fd974ac130be765cca748d1ad)

