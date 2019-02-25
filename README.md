I confirmed with Xubuntu 18.04LTS.

Original docs.: https://github.com/dbason/crystalhd/edit/master/README.md

# Requiremets
    sudo apt-get install checkinstall
     git
     autoconf
     pbuilder 
     dh-make 
     quilt 
     git-buildpackage 
     yasm 
     zlib1g-dev 
     libzip-dev 
     libx11-dev 
     libxv-dev 
     vstream-client-dev 
     libgtk2.0-dev 
     libpulse-dev 
     libxxf86dga-dev 
     python-appindicator 
     libelf-dev


# Installation
    git clone https://github.com/dbason/crystalhd.git

    cd crystalhd/driver/linux
    autoconf
    ./configure
    make -j2
    sudo make install


    cd ../../linux_lib/libcrystalhd/
    make -j2
    sudo make install 
    sudo modprobe crystalhd
    lsmod
    dmesg | grep crystalhd


# After kernel update

Reinstall the driver.

    cd crystalhd/driver/linux
    sudo make install
