![Gazee](/public/images/logo.png)

Gazee is a comic viewer for the web browser.

Read and reach your favorite digital comics from almost any web connected device.

Works great with [Mylar](https://github.com/evilhero/mylar) comic book management, but not needed.

Check out [the Wiki](https://github.com/hubbcaps/gazee/wiki) for detailed instructions on setup if you need them.

Questions can also be asked in the #gazee channel on Freenode

## Features

Recent Comics
![screen01](http://i.imgur.com/4cRYbJP.jpg)

Exposes your sorting structure in a library view
![screen02](http://i.imgur.com/LuJDAAG.jpg)

Download your issue if you have a preferred reader outside of Gazee and read a summary of the issue in line if available with your archive
![screen03](http://i.imgur.com/NcgCQTq.jpg)

Make Gazee yours and change up the color scheme
![screen04](http://i.imgur.com/xCLoowh.jpg)
![screen05](http://i.imgur.com/F5mb0bA.jpg)

Settings overlay to make the comic feel how you want it.
![screen06](http://i.imgur.com/t0NsWMp.jpg)

HTTPS Support

Bookmarks remember where you left off as you read.

Multiple Users and Admins

Much more to come!

## Requirements
* Python 3.6
* CherryPy
* Mako
* xmltodict
* Pillow
* rarfile
* GitPython

Requirements can be installed easily in the setup section below.

#### Unrar Downloads

Unrar needs to be installed and visible in the path of the user Gazee is running under to be able to properly extract all CBRs.

Double check this on Windows, different systems have different requirements for making sure you have unrar visbile in your users path.

[Unrar for Windows](http://www.rarlab.com/rar_add.htm), windows also needs command line accessible Git installed, gone over in the [install guide on the wiki](https://github.com/hubbcaps/gazee/wiki/Windows-Install-Guide)

[Centos](https://www.rpmfind.net/linux/rpm2html/search.php?query=unrar) needs Unrar from RPMFusion, not Offical/EPEL unar application. unar is out of date and will fail with certain types of cbrs and other rar archives.

[Debian](https://packages.debian.org/jessie/unrar)

## Setup

    cd <directory you want to install to>
    git clone https://github.com/hubbcaps/gazee.git
    cd gazee
    sudo pip install -r requirements.txt
    python Gazee.py


Go to http://your-ip:4242

Default user and pass for the web interface is admin/gazee

Proceed to the settings page and change your admin pass, and enter the path to your comic library and optionally your Mylar DB for better comic info extraction.

## Daemonize (Linux only)

You can easily run the program in Daemon mode by using the -d flag

    python Gazee.py -d

### QOL Features on the Roadmap

These are features that will make Gazee better and more up to par in what should be expected of a modern comic reader, but aren't needed for actual usability.

- [ ] Random First Issue of a series in library.
- [ ] OPDS Support.
- [ ] User set image sizes.
- [ ] Notifications on new comics
- [ ] Reports on various stats of your library; number of bad archives, comics without metadata, etc etc
