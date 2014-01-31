#
# Copyright (C) 2012 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=alfred-json
PKG_VERSION:=0.1
PKG_RELEASE:=1

PKG_SOURCE:=v$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/tcatm/alfred-json/archive/
PKG_MD5SUM:=a4074e5f4d4f5a9faadfa3db94942222

include $(INCLUDE_DIR)/package.mk

define Package/alfred-json
  SECTION:=utils
  CATEGORY:=Utilities
  DEPENDS:=+jansson +libc +librt
  TITLE:=ALFRED JSON client
  URL:=https://github.com/tcatm/alfred-json
endef

define Package/alfred-json/install
	$(INSTALL_DIR) $(1)/usr/bin
	cp -fpR  $(PKG_BUILD_DIR)/alfred-json $(1)/usr/bin/
endef

$(eval $(call BuildPackage,alfred-json))
