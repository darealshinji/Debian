include ../../mk/include.mk

deps           = wget
bin            = boarding-party.jar
icon           = boarding-party.png
cleanfiles     = $(icon)
distcleanfiles = $(bin)
srcfiles       = $(bin) $(icon) ../../mk/make-icons.sh

# mirror1: https://www.dropbox.com/s/3tlmdo1xk644jfu/boarding-party.jar
# mirror2: https://drive.google.com/file/d/0BxClEVSW8QykQkc4V0dqVjVUTUE/view?usp=sharing

download:
	@ $(call download,$(bin),http://www.intrrpt.com/downloads/boarding-party.jar)
	@ $(call download,$(icon),http://fs2.directupload.net/images/150127/3c9odqol.png)
	@ $(call verifysha256,$(bin),6c7fdc04102ee6f66bb5b6a2d7176ccbddd089b00e99b522f781dbd5ff7fcb82)
	@ $(call verifysha256,$(icon),08e95ee64866bb51e3aff0e486bdde84deba01268ab6f7d5559319cc5ea7739c)

