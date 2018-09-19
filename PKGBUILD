# Maintainer: Jan Boelsche <jan@lagomorph.de>

pkgname='minimal-desktop-environment'
pkgver=1.11
pkgrel=1
pkgdesc="Tools for a local admin"
packager='Jan Boelsche'
arch=('any')
license=('GPL')
groups=()
depends=(
  'background'
  'dconf'
  'minimal-x'
  'gnome-terminal'
  'gedit'

  #### Members of group xfce4

  'exo'	            # Extensions to Xfce by os-cillation
  'garcon'	        # Implementation of the freedesktop.org menu specification
  'gtk-xfce-engine'	# Xfce Gtk+-2.0 engine and themes
  'thunar'	        # Modern file manager for Xfce
  'thunar-volman'	  # Automatic management of removeable devices in Thunar
  'tumbler'	        # D-Bus service for applications to request thumbnails
  'xfce4-appfinder'	# An application finder for Xfce
  'xfce4-panel'	    # Panel for the Xfce desktop environment
  'xfce4-power-manager'	# Power manager for Xfce desktop
  'xfce4-session'	  # A session manager for Xfce
  'xfce4-settings'	# Settings manager for xfce
  #'xfce4-terminal'	# A modern terminal emulator primarily for the Xfce desktop environment
  'xfconf'	        # A simple client-server configuration storage and query system
  'xfdesktop'	      # A desktop manager for Xfce
  'xfwm4'	          # Xfce window manager
  'xfwm4-themes'	  # A set of additional themes for the Xfce window manager

  ####
)

source=(
  'gedit.dconf'
  'gnome-terminal.dconf'
  'user'
  'desktop-settings.tar.xz'
)

sha256sums=('aef169a4954dcf6ca329c5134bb2f311f59955c609221a02b291800a34cebc1b'
            'a8751849c226069bc59aa54c5fba7319cc65434ef6b38165e98e3d6a318b22cf'
            'f86c65bb83cc86cc9db1598f19197cf7c1533920980d7806bfd73da5cd5c3f5a'
            '44548821dfea8501cd78a3f29cf98fc083eb0a7a0c88fa217e3f2c778cb30af9')

install=${pkgname}.install

package () {
  install -Dm 644 -t "${pkgdir}/etc/dconf/db/default.d" gedit.dconf gnome-terminal.dconf 
  install -Dm 644 -t "${pkgdir}/etc/dconf/profile" user

  mkdir -p "${pkgdir}/home/local-admin/"
  cp -ra .local .gnome .config "${pkgdir}/home/local-admin/"
}
