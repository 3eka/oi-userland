#
# This file and its contents are supplied under the terms of the
# Common Development and Distribution License ("CDDL"), version 1.0.
# You may only use this file in accordance with the terms of version
# 1.0 of the CDDL.
#
# A full copy of the text of the CDDL should have accompanied this
# source.  A copy of the CDDL is also available via the Internet at
# http://www.illumos.org/license/CDDL.
#

#
# Copyright 2013 Alexander Pyhalov.  All rights reserved.
#

include ../../make-rules/shared-macros.mk

COMPONENT_NAME= libsigc++

COMPONENT_VERSION= 2.2.11
COMPONENT_SUMMARY= Libsigc++ - a library that implements a typesafe callback system for standard C++ (g++ - compiled)
COMPONENT_SRC= $(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE= $(COMPONENT_SRC).tar.xz
COMPONENT_ARCHIVE_HASH= \
  sha256:9834045f74f56752c2c6b3cdc195c30ab8314ad22dc8e626d6f67f940f1e4957
COMPONENT_ARCHIVE_URL= \
  http://ftp.gnome.org/pub/GNOME/sources/libsigc++/2.2/$(COMPONENT_ARCHIVE)
COMPONENT_PROJECT_URL = http://libsigc.sourceforge.net

include ../../make-rules/prep.mk
include ../../make-rules/configure.mk
include ../../make-rules/ips.mk

# Missing files in build dir for configure without this.
COMPONENT_PRE_CONFIGURE_ACTION =        ($(CLONEY) $(SOURCE_DIR) $(@D))  

CONFIGURE_OPTIONS+= --sysconfdir=$(ETCDIR)
CONFIGURE_OPTIONS +=	MAKE=$(GMAKE)

build: $(BUILD_32_and_64)

install: $(INSTALL_32_and_64)
