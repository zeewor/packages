#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=liborcania
PKG_VERSION:=2.1.0
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/babelouest/orcania/tar.gz/v$(PKG_VERSION)?
PKG_HASH:=a83f01968ae3e68fecfb2f7029f886902718c65315008223784d2d023da515bb

PKG_MAINTAINER:=Toni Uhlig <matzeton@googlemail.com>
PKG_LICENSE:=LGPL-2.1-or-later
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)/orcania-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1
CMAKE_INSTALL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/liborcania
  SECTION:=libs
  CATEGORY:=Libraries
  TITLE:=Functionality required by libulfius.
  URL:=https://github.com/babelouest/orcania
  PROVIDES:=liborcania
endef

define Package/liborcania/description
  Potluck with different functions for different purposes that can be shared among C programs.
endef

define Package/liborcania/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/liborcania.so.* \
		$(1)/usr/lib/
endef

$(eval $(call BuildPackage,liborcania))
