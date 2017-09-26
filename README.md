Electrum-XSH - lightweight SHIELD client
------------------------------------------------
![Electrum-XSH](https://raw.githubusercontent.com/ShieldCoin/electrum-XSH/master/electrumlogo.png)

[![Build Status](https://travis-ci.org/ShieldCoin/electrum-XSH.svg?branch=master)](https://travis-ci.org/ShieldCoin/electrum-XSH)

Licence: GNU GPL v3

Authors: sunerok, bitspill & whit3water

Language: Python

Homepage: http://electrum-SHIELD.xyz/

To get started, download the release, unzip, and click electrum-XSH.exe

don't forget to copy your randomly generated seedphrase, this will act as your private key.

they are not stored on our servers, so please don't lose them!



1.a) GETTING STARTED WITH UBUNTU/LINUX
------------------
sudo apt-get install git pyqt4-dev-tools python-pip python-dev python-slowaes

sudo pip install pyasn1 pyasn1-modules pbkdf2 tlslite qrcode

git clone https://github.com/ShieldCoin/electrum-XSH && cd electrum-XSH

pyrcc4 icons.qrc -o gui/qt/icons_rc.py

sudo python setup.py install

To run Electrum from this directory, just do:
---------------------------------------------
  ./electrum-XSH

To start Electrum from your web browser, see
--------------------------------------------
http://electrum-SHIELD.xyz/SHIELD_URIs.html

To update your copy of the electrum client:
-------------------------------------------
cd electrum-SHIELD

git pull

sudo python setup.py install

1.b) GETTING STARTED WITH WINDOWS
------------------

-download this repo as a zip and extract it to where you would like it to run from. 
https://github.com/ShieldCoin/electrum-XSH/archive/master.zip

-download python 2.7 for windows here: https://www.python.org/ftp/python/2.7.10/python-2.7.10.msi

-download Microsoft Visual C++ Compiler for Python 2.7 here: http://www.microsoft.com/en-us/download/confirmation.aspx?id=44266

-download python qt4: http://sourceforge.net/projects/pyqt/files/PyQt4/PyQt-4.11.3/PyQt4-4.11.3-gpl-Py2.7-Qt4.8.6-x64.exe

-then in ms visual studio command prompt, go into the directory electrum-XSH:

pyrcc4 icons.qrc -o gui/qt/icons_rc.py

py -m pip install pip pyasn1 pyasn1-modules pbkdf2 tlslite qrcode ecdsa ltc_scrypt

py setup.py install

py electrum-XSH



2. HOW OFFICIAL PACKAGES ARE CREATED
------------------------------------

python mki18n.py

pyrcc4 icons.qrc -o gui/qt/icons_rc.py

python setup.py sdist --format=zip,gztar

On Mac OS X:

  # On port based installs
  
  sudo python setup-release.py py2app

  # On brew installs
  
  ARCHFLAGS="-arch i386 -arch x86_64" sudo python setup-release.py py2app --includes sip

  sudo hdiutil create -fs HFS+ -volname "Electrum-XSH" -srcfolder dist/Electrum-XSH.app dist/electrum-XSH-VERSION-macosx.dmg
  
  alternate official build method:
  
On Linux:

python setup.py sdist --format=gztar
  
On Windows:

export VERSION=2.0.0

pyinstaller windows.spec

zip -r dist/SHIELD-electrum-$VERSION-win.zip dist/SHIELD-electrum.exe

On Mac OS X:

export VERSION=2.0.0

pyinstaller macosx.spec

sudo hdiutil create -fs HFS+ -volname "SHIELD Electrum" -srcfolder "dist/SHIELD Electrum.app" dist/SHIELD-electrum-$VERSION-mac.dmg

SHIELD Electrum Server List:
===========================
electrum-SHIELD.xyz

electrum-XSH.stream

[![Visit our IRC Chat!](https://kiwiirc.com/buttons/irc.freenode.net/SHIELD.png)](https://kiwiirc.com/client/irc.freenode.net/?nick=XSH|?&theme=cli#SHIELD)
