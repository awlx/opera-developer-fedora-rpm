opera-stable-fedora
======================
### How to Create RPM for Fedora

# Create the following folders
mkdir -p ~/rpmbuild/SOURCES

# Download latest .deb via opera.com
cd ~/rpmbuild/SOURCES
wget http://operasoftware.pc.cdn.bitgravity.com/pub/opera/desktop/31.0.1889.99/linux/opera-stable_31.0.1889.99_amd64.deb 

# Download libssl .deb file from Ubuntu repository
cd ~/rpmbuild/SOURCES
wget http://mirrors.kernel.org/ubuntu/pool/main/o/openssl/libssl1.0.0_1.0.1f-1ubuntu2.7_amd64.deb

# Build rpm package
rpmbuild -bb opera-stable.spec

# Install rpm
yum install ~/rpmbuild/RPMS/x86_64/opera-*.x86_64.rpm

# Use Opera Stable
Just click icon or

$ /usr/bin/opera

# Works for Fedora 20,Fedora 21 and Fedora 22
