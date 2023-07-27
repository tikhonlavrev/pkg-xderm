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
  MAINTAINER:=Forked by NCWRT <sayhanzp321@gmail.com>
  TITLE:=Xderm PHP8.
  DEPENDS:=+php8 +php8-cgi +php8-mod-session +php8-mod-gmp +php8-mod-gettext +php8-mod-iconv +php8-mod-pcntl
  PKGARCH:=all
endef

define Package/$(PKG_NAME)/description
	Xderm-Mini Inject Di STB.
endef

define Build/Compile
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/
	$(CP) ./files/* $(1)/
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
