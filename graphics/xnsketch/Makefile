include ../../include.mk

deps = wget
srcfiles = $(bin)
distcleanfiles = $(bin)
srcpkg = xnsketch
bin = XnSketch-linux.tgz

changelog-msg = New release version
VERSION = $(shell wget -q -O - http://www.xnview.com/en/xnsketch/ | grep -e 'Download <strong>XnSketch' | \
	perl -ne 'printf qq[%s\n], $$1 if m/<strong>([^<]+)<\/strong>/' | cut -d' ' -f2)

download:
	test -f $(bin) || wget "http://download.xnview.com/$(bin)"
	VERSION=$(VERSION); $(changelog-entry)
