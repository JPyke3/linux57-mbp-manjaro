# Maintainer: Philip Müller <philm[at]manjaro[dot]org>
# Maintainer: Bernhard Landauer <bernhard[at]manjaro[dot]org>
# Maintainer: Helmut Stult <helmut[at]manjaro[dot]org>

# Arch credits:
# Tobias Powalowski <tpowa@archlinux.org>
# Thomas Baechler <thomas@archlinux.org>

# Cloud Server
_server=cpx51

pkgbase=linux59-mbp
pkgname=('linux59-mbp' 'linux59-mbp-headers' 'linux59-mbp-docs')
_kernelname=-MANJARO-mbp
_basekernel=5.9
_basever=59
_rc=rc8
_commit=549738f15da0e5a00275977623be199fbbf7df50
_shortcommit=${_rc}.d1004.g${_commit:0:7}
_pkgver=${_basekernel}${_shortcommit}
pkgver=5.9rc8.d1004.g549738f
pkgrel=1
arch=('x86_64')
url="http://www.kernel.org/"
license=('GPL2')
makedepends=('bc'
    'docbook-xsl'
    'elfutils'
    'git'
    'inetutils'
    'kmod'
    'xmlto')
options=('!strip')
source=(#"https://www.kernel.org/pub/linux/kernel/v5.x/linux-${_basekernel}.tar.xz"
        #"https://www.kernel.org/pub/linux/kernel/v5.x/patch-${pkgver}.xz"
        "linux-${_pkgver}.zip::https://codeload.github.com/torvalds/linux/zip/$_commit"
        # the main kernel config files
        'config' 'config.anbox'
        # ARCH Patches
        '0001-ZEN-Add-sysctl-and-CONFIG-to-disallow-unprivileged-CLONE_NEWUSER.patch'
        # MANJARO Patches
        '0101-i2c-nuvoton-nc677x-hwmon-driver.patch'
        '0102-iomap-iomap_bmap-should-accept-unwritten-maps.patch'
        '0104-revert-xhci-Add-support-for-Renesas-controller-with-memory.patch'
        '0201-apparmor-patch-to-provide-compatibility-with-v2-net-rules.patch'
        '0202-apparmor-af_unix-mediation.patch'
        '0203-apparmor-fix-use-after-free-in-sk_peer_label.patch'
        '0204-apparmor-fix-apparmor-mediating-locking-non-fs-unix-sockets.patch'

        # Lenovo + AMD
        '0302-lenovo-wmi2.patch'
        # Temp Fixes

        # Bootsplash
        '0401-revert-fbcon-remove-now-unusued-softback_lines-cursor-argument.patch'
        '0402-revert-fbcon-remove-soft-scrollback-code.patch'
        '0501-bootsplash.patch'
        '0502-bootsplash.patch'
        '0503-bootsplash.patch'
        '0504-bootsplash.patch'
        '0505-bootsplash.patch'
        '0506-bootsplash.patch'
        '0507-bootsplash.patch'
        '0508-bootsplash.patch'
        '0509-bootsplash.patch'
        '0510-bootsplash.patch'
        '0511-bootsplash.patch'
        '0512-bootsplash.patch'
        '0513-bootsplash.gitpatch'
        
        #mbp
        '0001-drm-amd-display-Force-link_rate-as-LINK_RATE_RBR2-fo.patch'
        '0002-applesmc-convert-static-structures-to-drvdata.patch'
        '0003-applesmc-make-io-port-base-addr-dynamic.patch'
        '0004-applesmc-switch-to-acpi_device-from-platform.patch'
        '0005-applesmc-key-interface-wrappers.patch'
        '0006-applesmc-basic-mmio-interface-implementation.patch'
        '0007-applesmc-fan-support-on-T2-Macs.patch'
        '0008-T2-MacBook-Trackpad-Patches.patch'
        '0009-T2-MacBook-keyboard-backlight-patches.patch'
        '0010-brcmfmac-move-brcmf_mp_device-into-its-own-header.patch'
        '0011-brcmfmac-Add-ability-to-manually-specify-FW-rambase-.patch'
        '0012-media-uvcvideo-Add-support-for-Apple-T2-attached-iSi.patch'
        '0013-drm-i915-fbdev-Discard-BIOS-framebuffers-exceeding-h.patch'
        '0014-T2-MacBook-Wifi-Patches.patch')
sha256sums=('9ea92b8c6d9cd632defe06de10919fa1943760bd61b2c1d1ff4fd4672dbd5e17'
            '471bbfc37a3112197a288cf88bdba4cf44adf4e8788a2ad539ecceeb9b7c19d0'
            'fc896e5b00fad732d937bfb7b0db41922ecdb3a488bc1c1b91b201e028eed866'
            '986f8d802f37b72a54256f0ab84da83cb229388d58c0b6750f7c770818a18421'
            '7823d7488f42bc4ed7dfae6d1014dbde679d8b862c9a3697a39ba0dae5918978'
            '95745075edd597caa92b369cfbcd11a04c9e3c88c0c987c70114924e1e01df5c'
            '14fff25b581a0a8281a3419abd54d3bd200ede0374e685799da804f941c50f79'
            '98202b8ad70d02d86603294bae967874fa7b18704b5c7b867568b0fd33a08921'
            '5cbbf3db9ea3205e9b89fe3049bea6dd626181db0cb0dc461e4cf5a400c68dd6'
            'c7dbec875d0c1d6782c037a1dcefff2e5bdb5fc9dffac1beea07dd8c1bdef1d7'
            '77746aea71ffb06c685e7769b49c78e29af9b2e28209cd245e95d9cbb0dba3c9'
            '1d58ef2991c625f6f0eb33b4cb8303932f53f1c4694e42bae24c9cd36d2ad013'
            '2b11905b63b05b25807dd64757c779da74dd4c37e36d3f7a46485b1ee5a9d326'
            '37a221c12b40122167b0a30b5a9f2fc99e2aeb94e4db58a719c2b30171c5aeb5'
            '59202940d4f12bad23c194a530edc900e066866c9945e39748484a6545af96de'
            'e096b127a5208f56d368d2cb938933454d7200d70c86b763aa22c38e0ddb8717'
            '8c1c880f2caa9c7ae43281a35410203887ea8eae750fe8d360d0c8bf80fcc6e0'
            '1144d51e5eb980fceeec16004f3645ed04a60fac9e0c7cf88a15c5c1e7a4b89e'
            'dd4b69def2efacf4a6c442202ad5cb93d492c03886d7c61de87696e5a83e2846'
            '028b07f0c954f70ca37237b62e04103e81f7c658bb8bd65d7d3c2ace301297dc'
            'c8b0cb231659d33c3cfaed4b1f8d7c8305ab170bdd4c77fce85270d7b6a68000'
            '8dbb5ab3cb99e48d97d4e2f2e3df5d0de66f3721b4f7fd94a708089f53245c77'
            'a7aefeacf22c600fafd9e040a985a913643095db7272c296b77a0a651c6a140a'
            'e9f22cbb542591087d2d66dc6dc912b1434330ba3cd13d2df741d869a2c31e89'
            '27471eee564ca3149dd271b0817719b5565a9594dc4d884fe3dc51a5f03832bc'
            '60e295601e4fb33d9bf65f198c54c7eb07c0d1e91e2ad1e0dd6cd6e142cb266d'
            '035ea4b2a7621054f4560471f45336b981538a40172d8f17285910d4e0e0b3ef'
            'fe6c6a886f3c1a94d3ed1c279f158f65faef804e14aabb77dca0d015ce798cd3'
            '19026205d1e01d7d36625357ac7dcdd5c1f6d9f8e76480c380749046fe9c9b92'
            'b688a33d8c122ef4f3c03a638919782cb7f2b5e7723f299fe6c7f86413bb7bb0'
            '32d83d547b1ea6ec84e3218ca5e0775cc262d2ce31861c516e8d87c2d06ac955'
            'cc9c047be0b99f76ee4be32117b13c96d827e5d6c7f21e68ea61cf80255f8e6d'
            'eea8b20e2b547fff0cdd5e7c86c5b0bf951c82610172df8b03f3495be219aa28'
            '51d91c2f469b1b81ee5d307b5e8b56e332322bf6c3aafa874787d4a9eaf7fe16'
            'd6e32a67499b8d58474af71d14d4730c8dca7bd76809553f1fb8df33893adc16'
            'e88a1be70594453b07d7c763499bc74685f95b89446241587045d12d2fc95d34'
            '2c89f80eea0a72280a18f8ec14e9d63728b15f95852aa8995951a656f5c08741'
            '16a79c62a1a744bd04a35258e08c30572ac6cd7dc7f36c102088f2caafa907a0'
            '736733271c0e622bdd1a58ea08ffb1229eecba46b64851f326b96ea90c3eb560'
            '976f354be437879956fec61304dbc59202bf5fbc9a496f2a4e79bf9563e5350b'
            'd46d435975d3bcc915558a2f9c8d61cdb6bad31b50a46f605e257aa0a8a35d65')

pkgver() {
  printf '%s' "${_pkgver}"
}

prepare() {
  mv "${srcdir}/linux-${_commit}" "${srcdir}/linux-${_basekernel}"
  cd "${srcdir}/linux-${_basekernel}"

  # add upstream patch
#  msg "add upstream patch"
#  patch -p1 -i "${srcdir}/patch-${pkgver}"

  local src
  for src in "${source[@]}"; do
      src="${src%%::*}"
      src="${src##*/}"
      [[ $src = *.patch ]] || continue
      msg2 "Applying patch: $src..."
      patch -Np1 < "../$src"
  done

  msg2 "0513-bootsplash"
  git apply -p1 < "${srcdir}/0513-bootsplash.gitpatch"

  msg2 "add config.anbox to config"
  cat "${srcdir}/config" > ./.config
  cat "${srcdir}/config.anbox" >> ./.config

  if [ "${_kernelname}" != "" ]; then
    sed -i "s|CONFIG_LOCALVERSION=.*|CONFIG_LOCALVERSION=\"${_kernelname}\"|g" ./.config
    sed -i "s|CONFIG_LOCALVERSION_AUTO=.*|CONFIG_LOCALVERSION_AUTO=n|" ./.config
  fi

  msg "set extraversion to pkgrel"
  sed -ri "s|^(EXTRAVERSION =).*|\1 -${pkgrel}|" Makefile

  # set patchlevel to 9
  sed -ri "s|^(PATCHLEVEL =).*|\1 9|" Makefile

  msg "don't run depmod on 'make install'"
  # We'll do this ourselves in packaging
  sed -i '2iexit 0' scripts/depmod.sh

  msg "get kernel version"
  make prepare

  # load configuration
  # Configure the kernel. Replace the line below with one of your choice.
  #make menuconfig # CLI menu for configuration
  #make nconfig # new CLI menu for configuration
  #make xconfig # X-based configuration
  #make oldconfig # using old config from previous kernel version
  # ... or manually edit .config

  msg "rewrite configuration"
  yes "" | make config >/dev/null
}

build() {
  cd "${srcdir}/linux-${_basekernel}"

  msg "build"
  make ${MAKEFLAGS} LOCALVERSION= bzImage modules
}

package_linux59-mbp() {
  pkgdesc="The ${pkgbase/linux/Linux} kernel and modules"
  depends=('coreutils' 'linux-firmware' 'kmod' 'mkinitcpio>=27')
  optdepends=('crda: to set the correct wireless channels of your country')
  provides=("linux=${pkgver}" VIRTUALBOX-GUEST-MODULES WIREGUARD-MODULE)

  cd "${srcdir}/linux-${_basekernel}"

  KARCH=x86

  # get kernel version
  _kernver="$(make LOCALVERSION= kernelrelease)"

  mkdir -p "${pkgdir}"/{boot,usr/lib/modules}
  make LOCALVERSION= INSTALL_MOD_PATH="${pkgdir}/usr" INSTALL_MOD_STRIP=1 modules_install

  # systemd expects to find the kernel here to allow hibernation
  # https://github.com/systemd/systemd/commit/edda44605f06a41fb86b7ab8128dcf99161d2344
  cp arch/$KARCH/boot/bzImage "${pkgdir}/usr/lib/modules/${_kernver}/vmlinuz"

  # Used by mkinitcpio to name the kernel
  echo "${pkgbase}" | install -Dm644 /dev/stdin "${pkgdir}/usr/lib/modules/${_kernver}/pkgbase"
  echo "${_basekernel}-${CARCH}-mbp" | install -Dm644 /dev/stdin "${pkgdir}/usr/lib/modules/${_kernver}/kernelbase"

  # add kernel version
  echo "${pkgver}-${pkgrel}-MANJARO-mbp x64" > "${pkgdir}/boot/${pkgbase}-${CARCH}.kver"

  # make room for external modules
  local _extramodules="extramodules-${_basekernel}${_kernelname:--MANJARO-mbp}"
  ln -s "../${_extramodules}" "${pkgdir}/usr/lib/modules/${_kernver}/extramodules"

  # add real version for building modules and running depmod from hook
  echo "${_kernver}" |
    install -Dm644 /dev/stdin "${pkgdir}/usr/lib/modules/${_extramodules}/version"

  # remove build and source links
  rm "${pkgdir}"/usr/lib/modules/${_kernver}/{source,build}

  # now we call depmod...
  depmod -b "${pkgdir}/usr" -F System.map "${_kernver}"

  # add vmlinux
  install -Dt "${pkgdir}/usr/lib/modules/${_kernver}/build" -m644 vmlinux
}

package_linux59-mbp-headers() {
  pkgdesc="Header files and scripts for building modules for ${pkgbase/linux/Linux} kernel"
  provides=("linux-headers=$pkgver")

  cd "${srcdir}/linux-${_basekernel}"
  local _builddir="${pkgdir}/usr/lib/modules/${_kernver}/build"

  install -Dt "${_builddir}" -m644 Makefile .config Module.symvers
  install -Dt "${_builddir}/kernel" -m644 kernel/Makefile

  mkdir "${_builddir}/.tmp_versions"

  cp -t "${_builddir}" -a include scripts

  install -Dt "${_builddir}/arch/${KARCH}" -m644 "arch/${KARCH}/Makefile"
  install -Dt "${_builddir}/arch/${KARCH}/kernel" -m644 "arch/${KARCH}/kernel/asm-offsets.s"
  #install -Dt "${_builddir}/arch/${KARCH}/kernel" -m644 "arch/${KARCH}/kernel/macros.s"

  cp -t "${_builddir}/arch/${KARCH}" -a "arch/${KARCH}/include"

  install -Dt "${_builddir}/drivers/md" -m644 drivers/md/*.h
  install -Dt "${_builddir}/net/mac80211" -m644 net/mac80211/*.h

  # http://bugs.archlinux.org/task/13146
  install -Dt "${_builddir}/drivers/media/i2c" -m644 drivers/media/i2c/msp3400-driver.h

  # http://bugs.archlinux.org/task/20402
  install -Dt "${_builddir}/drivers/media/usb/dvb-usb" -m644 drivers/media/usb/dvb-usb/*.h
  install -Dt "${_builddir}/drivers/media/dvb-frontends" -m644 drivers/media/dvb-frontends/*.h
  install -Dt "${_builddir}/drivers/media/tuners" -m644 drivers/media/tuners/*.h

  # add xfs and shmem for aufs building
  mkdir -p "${_builddir}"/{fs/xfs,mm}

  # copy in Kconfig files
  find . -name Kconfig\* -exec install -Dm644 {} "${_builddir}/{}" \;

  # add objtool for external module building and enabled VALIDATION_STACK option
  install -Dt "${_builddir}/tools/objtool" tools/objtool/objtool

  # remove unneeded architectures
  local _arch
  for _arch in "${_builddir}"/arch/*/; do
    [[ ${_arch} == */x86/ ]] && continue
    rm -r "${_arch}"
  done

  # remove files already in linux-docs package
  rm -r "${_builddir}/Documentation"

  # Fix permissions
  chmod -R u=rwX,go=rX "${_builddir}"

  # strip scripts directory
  local _binary _strip
  while read -rd '' _binary; do
    case "$(file -bi "${_binary}")" in
      *application/x-sharedlib*)  _strip="${STRIP_SHARED}"   ;; # Libraries (.so)
      *application/x-archive*)    _strip="${STRIP_STATIC}"   ;; # Libraries (.a)
      *application/x-executable*) _strip="${STRIP_BINARIES}" ;; # Binaries
      *) continue ;;
    esac
    /usr/bin/strip ${_strip} "${_binary}"
  done < <(find "${_builddir}/scripts" -type f -perm -u+w -print0 2>/dev/null)
}

package_linux59-mbp-docs() {
  pkgdesc="Documentation for the $pkgdesc kernel"

  cd "${srcdir}/linux-${_basekernel}"
  local builddir="$pkgdir/usr/lib/modules/$(<version)/build"

  echo "Installing documentation..."
  local src dst
  while read -rd '' src; do
    dst="${src#Documentation/}"
    dst="$builddir/Documentation/${dst#output/}"
    install -Dm644 "$src" "$dst"
  done < <(find Documentation -name '.*' -prune -o ! -type d -print0)

  echo "Adding symlink..."
  mkdir -p "$pkgdir/usr/share/doc"
  ln -sr "$builddir/Documentation" "$pkgdir/usr/share/doc/$pkgbase"
}
