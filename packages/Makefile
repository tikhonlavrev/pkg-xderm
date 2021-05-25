include $(TOPDIR)/rules.mk

PKG_NAME:=xderm
PKG_VERSION=$(GIT_COMMIT_DATE)-$(GIT_COMMIT_TSTAMP)
GIT_COMMIT_DATE:=$(shell git log -n 1 --pretty=%ad --date=short . )
GIT_COMMIT_TSTAMP:=$(shell git log -n 1 --pretty=%at . )

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
  SUBMENU:=Captive Portals
  SECTION:=net
  CATEGORY:=Network
  MAINTAINER:=Adi Subagja <adisubagjaa@gmail.com>
  TITLE:=Captive portal with vouchers.
  DEPENDS:=+php7 +php7-cgi +php7-mod-session +php7-mod-gmp +php7-mod-gettext +php7-mod-iconv +php7-mod-json +php7-mod-pcntl
  PKGARCH:=all
endef

define Package/$(PKG_NAME)/description
	Captive Portal for routers that want to share their Internet connection via vouchers.
endef

define Build/Compile
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/
	$(CP) ./files/* $(1)/
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
