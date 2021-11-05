# vagrantfiles
Vagrantfiles to setup virtual machines for the OpenIndiana operating system.

See https://www.vagrantup.com for more info on vagrant.

See https://www.openindiana.org/ for info on OpenIndiana.

The tree structure of this repository somewhat tries to follow the FMRI
or oi-userland/components hierarchy.

VAGRANT
-------

There exist packages of Vagrant for various operating systems (Linux etc).

See

 http://docs.openindiana.org/handbook/community/vagrant/index.html

for info on building vagrant on OpenIndiana itself.

It is not necessary to build Vagrant on OI if you only want to run an
OpenIndiana vagrant guest VM on another operating system.

For example you can download an official Vagrant package on Linux,
and use Linux to run OpenIndiana Vagrant guests;

You can also run OI vagrant guest VM's on OpenIndiana itself.

BOXES
-----

The current, official, OI box is:

  $ vagrant box list
  openindiana/hipster (virtualbox, 202109)

AUDIO
-----

By setting the PULSE_SERVER variable in the guest and point it to the host,
you can also play audiofiles in a Vagrant guest VM.

See the PulseAudio X11 Credential Utility ('pax11publish') and 'paprefs' on the host for more information.

By setting PULSE_SERVER="tcp:localhost:24713" and forwarding port 24713 on the
guest to port 4713 on the host, the command 'pactl info' can be used,
to check that you can connect to the pulse server on the host.

