include ../../mk/include.mk

deps     = git
builddir = zdoom

download:
	rm -rf $(builddir)
	git clone "https://github.com/rheit/zdoom.git"
	@ latestcommit=$$(git -C $(builddir) log -1 --format=%ci | head -c10 | sed -e 's/-//g'); \
	tagver=$$(git -C $(builddir) describe --abbrev=0 --tags | sed -e 's/g//g; s/\pre/~pre/g'); \
	VERSION="$${tagver}+git$${latestcommit}"; \
	$(changelog-entry)
	rm -rf $(builddir)/.git

