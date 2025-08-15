include $(TOPDIR)/rules.mk

PKG_NAME:=syslog-fc
PKG_VERSION:=0.9.5
PKG_RELEASE:=0

PKG_MAINTAINER:=William <gw826943555@qq.com>
PKG_LICENSE:=WTFPL

PKG_SOURCE_URL:=https://github.com/namedun/syslog_fc.git
PKG_SOURCE_PROTO:=git
PKG_SOURCE_VERSION:=873ae0a6224e9b2829507966545be2e438f3a9d4
PKG_MIRROR_HASH:=95584af73f1997c36774cbd1772859ecfb5a535631b3730eb195a41454d241fa

PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/syslog-fc
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=A powerful syslog file converter
  URL:=https://github.com/namedun/syslog_fc
endef

define Package/syslog-fc/description
  The syslog-fc is designed to convert syslog files to various other text formats, 
  such as CSV, HTML or JSON
endef

define Package/syslog-fc/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/syslog_fc $(1)/usr/bin/syslog_fc
endef

$(eval $(call BuildPackage,syslog-fc))