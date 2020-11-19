# Build of Firefox-ESR for Lliurex

# Introduction

Firefox-ESR for Lliurex it's a customized version of firefox-esr that allows to coexist with firefox as a separate app. It has it's own icon and display and app name.

# Building

Download the desired version of firefox-esr from https://archive.mozilla.org/pub/firefox/releases/

Create a build dir and uncompress the firefox-esr sources

Clone the devtools from subversion: svn co https://svn.lliurex.net/xenial/devtools in tmpdir

If you're attempting to build the i686 version then follow the instructions from method 2 in https://developer.mozilla.org/en-US/docs/Mozilla/Developer_guide/Build_Instructions/Compiling_32-bit_Firefox_on_a_Linux_64-bit_OS

Go to the firefox-esr builddir and execute the firefox-configurator you cloned from subversion:
tmpdir/devtools/firefox_customizer/firefox_customizer.sh [amd64|i686]

Follow the instructions on screen

When finished copy the content of builddir/obj-firefox-[amd64|i686]/dist/firefoxESR to the appropiate svn folder of firefox-esr
Update the project and proceed with svn-buildpackage
