# SPDX-License-Identifier: MIT
#
# Copyright (C) 2023-2025 openwrt-addons-packages

include $(TOPDIR)/rules.mk

PKG_NAME:=openwrt_addons_keyring
PKG_VERSION:=1.0
PKG_RELEASE:=1

PKG_MAINTAINER:=Richard Smith <rtsmith134@gmail.com>
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=License

PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
  SECTION:=base
  CATEGORY:=Base system
  TITLE:=openwrt_addons_keyring Developer Keyring
  PKGARCH:=all
endef

define Package/$(PKG_NAME)/description
  The keyring for openwrt_addons.
endef

Build/Compile=

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/etc/opkg/keys/
	$(INSTALL_DATA) $(CURDIR)/usign/4865CBF36A4437CE $(1)/etc/opkg/keys/
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
