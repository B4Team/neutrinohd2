based on opennhd2-[r64](https://code.google.com/p/neutrinohd2/source/detail?r=64).12 from scp

# MAKE: #
for oe-alliance:
##  ##
cd /(oe-alliance-path)/build-enviroment/meta-oe-alliance
##  ##
svn co http://neutrinohd2.googlecode.com/svn/branches/recipes-neutrino recipes-neutrino
##  ##
cd (oe-alliance-path)/build-enviroment/builds/(DISTRO)/(MACHINE)
##  ##
for openpli3.0:
##  ##
cd (openpli30-path)/openpli-oe-core/meta-openpli
##  ##
svn co http://neutrinohd2.googlecode.com/svn/branches/recipes-neutrino recipes-neutrino
##  ##
cd (openpli30-path)/openpli-oe-core/build-(MACHINE)
##  ##
. ./env.source
##  ##
bitbake neutrino
##  ##
result can be found here:
##  ##
for oe-alliance:
##  ##
(oe-alliance-path)/build-enviroment/builds/(DISTRO/(MACHINE)/tmp/deploy/ipk/mips32el/neutrino\_svn(svnrevision)-[r64](https://code.google.com/p/neutrinohd2/source/detail?r=64).12\_mips32el.ipk
##  ##
for openpli3.0:
##  ##
(openpli30-path)/openpli-oe-core/build-MACHINE/tmp/deploy/ipk/mips32el/neutrino\_svn(svnrevision)-[r64](https://code.google.com/p/neutrinohd2/source/detail?r=64).12\_mips32el.ipk

# INSTALL: #
- copy neutrino\_svn(actuall svn rev)-[r64](https://code.google.com/p/neutrinohd2/source/detail?r=64).12\_mips32el.ipk to /tmp
##  ##
opkg install /tmp/neutrino\_svn(actuall svn rev)-[r64](https://code.google.com/p/neutrinohd2/source/detail?r=64).12\_mips32el.ipk
##  ##
-librtmp:
copy librtmp0\_2.4+git484+df6c518-r1\_mips32el.ipk to /tmp
##  ##
opkg update && opkg install --force-overwrite /tmp/librtmp0\_2.4+git484+df6c518-r1\_mips32el.ipk[/code]
##  ##
for quick test, kill enigma2:
##  ##
init 2
##  ##
start neutrino
##  ##
neutrino &

# CAUTION: #
be sure that is enought place in flash;-)