opera-developer-fedora
======================
### How to Create RPM for Fedora

# Create the following folders
mkdir -p ~/rpmbuild/SOURCES

# download stable .deb package file from Opera homepage to ~/rpmbuild/SOURCES
http://opera.com

# download libssl .deb package file from Ubuntu repository to ~/rpmbuild/SOURCES
Check http://packages.ubuntu.com/trusty-updates/libssl1.0.0

# build rpm package
rpmbuild -bb opera-developer.spec

# install rpm
yum install ~/rpmbuild/RPMS/x86_64/opera-*.x86_64.rpm

# start to use opera stable
Just click icon or

$ /usr/bin/opera

