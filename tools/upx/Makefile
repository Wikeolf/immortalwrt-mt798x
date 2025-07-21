#
# Copyright (C) 2011-2013 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#
include $(TOPDIR)/rules.mk

PKG_NAME:=upx
PKG_VERSION:=5.0.2

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-src.tar.xz
PKG_SOURCE_URL:=https://github.com/upx/upx/releases/download/v$(PKG_VERSION)
PKG_MD5SUM:=209b219bbcfa58c249ffe6eba3c244e0910fa8be792b5521e4daf938167f05cc

HOST_BUILD_DIR:=$(BUILD_DIR_HOST)/$(PKG_NAME)-$(PKG_VERSION)-src

include $(INCLUDE_DIR)/host-build.mk

define Host/Compile
	$(call Host/Compile/Default,build/release)
endef

define Host/Install
	$(CP) $(HOST_BUILD_DIR)/build/release/upx $(STAGING_DIR_HOST)/bin/upx
endef

define Host/Clean
	rm -f $(STAGING_DIR_HOST)/bin/upx
endef

$(eval $(call HostBuild))