Hardware
--------

Laptop: Lenovo W540 BH
Graphics: NVIDIA Quadro K1100M 2GB
Wireless: Intel 7260BN

Software
--------

Fedora 20 64-bit


Grant user sudo privileges
--------------------------

- su -

> usermod -a -G wheel will

Add an alias for vim
--------------------

vi ~/.bashrc

Add the line:

	alias vi=vim

Update the system
-----------------

> sudo yum update

Install a rpm package
---------------------

> rpm -ihv <rpm_file>

Install a rpm package (downloading any additional dependancies)
---------------------------------------------------------------

> sudo yum --nogpgcheck localinstall <rpm_file>

Add third-party repositories
----------------------------

rpmfusion.org:

su -c 'yum localinstall --nogpgcheck http://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm http://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm'

rpm.livna.org:

su -c "rpm -ivh http://rpm.livna.org/livna-release.rpm"


Software Installation
=====================

Google Chrome
---------------------

- Download the 64-bit rpm

- sudo rpm -ihv google-chrome-stable_current_x86_64.rpm

VirtualBox
----------

- sudo yum install VirtualBox

git
---

-

Sublime Text
------------

> sudo tar xvjf <sublme_text_.tar.bz2> -C /opt/

> sudo ln -s "/opt/Sublime Text 2/sublime_text" /usr/local/bin/sublime-text

> sudo vi /usr/share/applications/sublime-text.desktop

Edit the file so the contents are as follows:

[Desktop Entry]
Name=Sublime Text
Exec=subl %F
MimeType=text/plain;
Terminal=false
Type=Application
Icon=/opt/Sublime\sText\s2/Icon/128x128/sublime_text.png
Categories=Utility;TextEditor;Development;