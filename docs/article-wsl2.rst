*******************
Run ELBE under WSL2
*******************

As of Windows 11 version 24H2 ELBE can be used with the Windows Subsystem for
Linux 2.

Prerequisite
============
Install Debian through Microsoft Store. As of December 2024 Debian bookworm
is installed.

Installing ELBE
===============
1. Get a root shell
   
::

   $ sudo /bin/bash

Install the repository key to a known place:

::

   # apt install elbe-archive-keyring || wget -O /usr/share/keyrings/elbe-archive-keyring.gpg http://debian.linutronix.de/elbe/elbe-repo.pub.gpg

Add the following content to the file ``/etc/apt/sources.list``

::

   # echo "deb [signed-by=/usr/share/keyrings/elbe-archive-keyring.gpg] http://debian.linutronix.de/elbe bookworm main" >> /etc/apt/sources.list

Then run:

::

   # apt update
   # apt install elbe

ELBE is now installed and can be used. Please continue with
:ref:`create-initvm`.
