SRPM tools for kubernetes
=========================

There is no published kubernetes RPM for RHEL, but the Fedora version
seems to be possible to backport.

golang requirements
-------------------

Fedora ha these packages, which do not seem required for the older
RHEL based golang setup.

     * BuildRequires: go-md2man
     * BuildRequires: go-bindata

Building RPMs
-------------

"make" options include:

  * make getsrc # Download the source tarballs
  * make build # Build with all docs and tests
  * make fastbuild # Build without docs and tests for fast smoke test

  * make # Build full multi-platform versions with mock
  * make install # build and install multi-platform versions in REPOBASEDIR

Run the "make getsrc" command, and run "make build" to build a local RPM under
rpmbuild.

Run "make" to use "mock" to build the default designated RPM's in the
local working directories such as centos-stream+epel-8-x86_6 and centos-stream+epel-9-x86_64.

       	  Nico Kadel-Garcia <nkadelgmail.com>
