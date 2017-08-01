[![DOI](https://zenodo.org/badge/88288867.svg)](https://zenodo.org/badge/latestdoi/88288867)

![Dugong](https://raw.githubusercontent.com/fabianomenegidio/dugong-bioinformatics/gh-pages/.misc/dugongo.png)

# Dugong - Scientific Linux Container

[Dugong](https://hub.docker.com/r/dugong/dugong) is a powerful workstation platform especially designed for scientific computational analysis, mainly of bioinformatics and computational biology, that can be installed in any computational ecosystem, regardless of the operating system and hardware used. In general terms, it's a [Linux system](https://en.wikipedia.org/wiki/Linux) designed specifically for the development of the [Open Science](https://en.wikipedia.org/wiki/Open_science) concept, based on the reproducibility and replicability of the research.

It's an implementation built under the [MIT license](https://opensource.org/licenses/MIT) using the [Docker platform](https://www.docker.com/), an open-source project that automates the implementation of applications within software containers, providing an additional layer of abstraction and automation of operating system-level virtualization on [Linux](https://en.wikipedia.org/wiki/Linux). [Docker](https://www.docker.com/) uses the [Linux kernel](https://en.wikipedia.org/wiki/Linux_kernel) resource isolation features, such as [cgroups](https://en.wikipedia.org/wiki/Cgroups) and [namespaces](https://en.wikipedia.org/wiki/Linux_namespaces), as well as the file system [AuFS](https://en.wikipedia.org/wiki/Aufs) (advanced multi layered unification filesystem) to allow independent *containers* to run in a single Linux instance, avoiding an overload of initialization and maintenance of virtual machines. The [Dugong project](https://hub.docker.com/r/dugong/dugong) enables efficient creation of reusable containers for bioinformatics data, making the analysis environment and all computational results reproducible by the scientific community.

[Dugong](https://hub.docker.com/r/dugong/dugong) is based on version 16.04 of [Ubuntu Image](https://hub.docker.com/r/_/ubuntu), the only [Docker system](https://www.docker.com/) focused on bioinformatics that provides users with a complete graphical user interface (GUI) [XFCE4](https://xfce.org/), independent of the host, which should facilitate user interaction with different computing ecosystems, as well as the installation and use of different bioinformatics software. For the distribution of bioinformatics software, two large open source projects have been integrated [Dugong](https://hub.docker.com/r/dugong/dugong): [LinuxBrew](http://linuxbrew.sh/) and [BioConda](https://bioconda.github.io/), totaling over **3,500 bioinformatics packages** and their respective dependencies. [Dugong](https://hub.docker.com/r/dugong/dugong) is the only system focused on bioinformatics that offers [Anaconda Navigator](https://docs.continuum.io/anaconda/navigator/), a graphical package manager for [Conda](https://conda.io/docs/) and the [BioConda](https://bioconda.github.io/) repository, allowing the installation of packages and tools through its graphical interface. We also added, as an alternative, the [BioLinux](http://environmentalomics.org/bio-linux/) and [CloudBioLinux](http://cloudbiolinux.org/) project repositories for the installation of [DEB packages](https://en.wikipedia.org/wiki/Deb_(file_format)) through the APT command.

Thinking about the replicability and reproducibility of different lines of research that benefit from bioinformatics analysis, [Dugong](https://hub.docker.com/r/dugong/dugong) is the only tool of its kind that provides [Jupyter Notebook](http://jupyter.org/) installed by default on all their versions. 

All of these features, among others, make [Dugong](https://hub.docker.com/r/dugong/dugong) one of the most complete [Docker](https://www.docker.com/) desktop environments available today, and allow any user with minimal computing knowledge to run a [Dugong](https://hub.docker.com/r/dugong/dugong) container in [high performance computing](https://en.wikipedia.org/wiki/Supercomputer) (HPC) environments, [Virtual Private Server](https://en.wikipedia.org/wiki/Virtual_private_server) (VPS), as well as in private, public, or hybrid [cloud computing](https://en.wikipedia.org/wiki/Cloud_computing) environments of different commercial service providers.

The [Dugong project](https://hub.docker.com/r/dugong/dugong) is publicly committed to the principles of open source software development, where people are encouraged to use free software, study how they function, improve and distribute them freely.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## MENU <a name="menu" />

- [Dugong flavours](#Dugong-flavours)
  - [DugongGUI Version](#DugongGUI)
  - [DugongCMD Version](#DugongCMD)
- [Bioinformatics Software](#Bioinformatics-Software)
    - [Conda and BioConda](#BioConda)
    - [LinuxBrew](#LinuxBrew)
    - [DEB Repository](#DEB)
- [Install Docker](#Install-Docker)
  - [Ubuntu](#Ubuntu)
  - [Fedora](#Fedora) 
  - [Windows](#Windows)
  - [MacOS](#MacOS) 
- [Deploy and access Dugong](#Deploy)
- [Video installation](#Video-installation)
- [Dugong Virtual Box](#Dugong-Virtual-Box)
- [Extending or adapting the Dugong image](#Extending)
- [Example of adapted tools in Dugong](#Example)
  - [CirComPara](#CirComPara)
- [Author](#Author)
- [Contributing](#Contributing)
- [MIT License](#MIT)
- [Learn More](#Learn-More)

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Dugong flavours <a name="Dugong-flavours" /> [[menu]](#menu)

Today, the Dugong operating system is available in two versions: [***DugongGUI***](https://github.com/DugongBioinformatics/dugongbioinformatics.github.io/blob/master/README.md#DugongGUI) and [***DugongCMD***](https://github.com/DugongBioinformatics/dugongbioinformatics.github.io/blob/master/README.md#DugongCMD).

[***DugongGUI***](https://github.com/DugongBioinformatics/dugongbioinformatics.github.io/blob/master/README.md#DugongGUI) is the main working environment of the project and our great differential for applications in bioinformatics and computational biology. Based on [Ubuntu 16.04](http://releases.ubuntu.com/16.04/), the [***DugongGUI***](https://github.com/DugongBioinformatics/dugongbioinformatics.github.io/blob/master/README.md#DugongGUI) image has as its main GUI the [XFCE4](https://xfce.org/), with a beta version containing the [IceWM](http://www.icewm.org/) graphical environment in development.

Already the [***DugongCMD***](https://github.com/DugongBioinformatics/dugongbioinformatics.github.io/blob/master/README.md#DugongCMD) version is focused on the fast access and availability of bioinformatics tools through an iterative web interface developed in [node.js](https://en.wikipedia.org/wiki/Node.js), which can be accessed directly by the browser. This version does not have a GUI installed by default, but allows [X11](https://en.wikipedia.org/wiki/X_Window_System) forwarding to the host machine.

An important feature of [Dugong](https://hub.docker.com/r/dugong/dugong) is that both versions provide system access through the [SSH protocol](https://en.wikipedia.org/wiki/Secure_Shell) and the exchange of files through [RSYNC](https://en.wikipedia.org/wiki/Rsync) and [SCP](https://en.wikipedia.org/wiki/Secure_copy). Also providing [BaseMount](https://basemount.basespace.illumina.com/), an opensource application that allows you to mount the [BaseSpace Sequence Hub](https://basespace.illumina.com/home/index) in [Dugong](https://hub.docker.com/r/dugong/dugong), allowing the user to navigate in projects, samples, runs and results of applications and interact directly with associated files.

Below we describe the tools available in each version of Dugong:

### DugongGUI Version <a name="DugongGUI" /> [[menu]](#menu)

This is the preinstalled software suite that enables better use of DugongGUI:

- [Xfce4](https://www.xfce.org/) (translated as four individual letters) is a free and open source desktop environment for Unix platforms such as Linux, Solaris and BSD. As a fast, easy-to-use open-source workbench, it was selected as the official GUI for the Dugong project.
- [IceWM](http://www.icewm.org/) is a window manager designed for lightweight simplicity and ease of use, but not focused on customizability. It looks similar to Windows 95. In beta testing at DugongGUI.

Access as graphical interfaces available in DugongGUI can be performed through two options:

- [VNC](https://www.realvnc.com/): a graphical desktop sharing system that uses the [Remote Frame Buffer (RFB) protocol](https://en.wikipedia.org/wiki/RFB_protocol) to remotely control another computer. It transmits the keyboard and mouse events from one computer to another, transmitting as graphical screen updates back in the other direction, over a network.
- [noVNC](http://kanaka.github.io/noVNC/noVNC/vnc.html):  is a client for the VNC protocol that runs in your browser, and a dumb TCP-to-Websockets proxy script that you run on your server if your VNC software doesn't already support [Websockets](https://en.wikipedia.org/wiki/WebSocket) in addition to [TCP](https://en.wikipedia.org/wiki/Transmission_Control_Protocol). It's implemented through [HTML5 Canvas](https://en.wikipedia.org/wiki/Canvas_element) and [Websockets](https://en.wikipedia.org/wiki/WebSocket) technologies, allowing an execution of a graphical desktop sharing system using a simple browser.

***DugongGUI*** also has a set of preinstalled software packages that allow a better use of the operating system, especially:

- [Anaconda Navigator](https://docs.continuum.io/anaconda/navigator/): is a desktop graphical user interface (GUI) that is included in Anaconda or Miniconda, and allows you to launch applications and easily manage ***Conda*** and ***Bioconda*** packages, environments and channels without using command-line commands.
- [Spyder IDE](https://github.com/spyder-ide): a powerful interactive development environment for the Python language with advanced editing, interactive testing, debugging and introspection features and a numerical computing environment thanks to the support of IPython (enhanced interactive Python interpreter) and popular Python libraries such as NumPy (linear algebra), SciPy (signal and image processing) or matplotlib (interactive 2D/3D plotting).
- [ASCIInema](https://asciinema.org/): is a free and open source solution for recording terminal sessions and sharing them on the web.
- [Google Chrome](https://www.google.com/chrome/browser/): a browser that combines a minimalist design with sophisticated technology to make the web faster, safer and easier.
- [MEGASync](https://mega.nz/#sync): a desktop client for MEGA Service Cloud providing easy automatic synchronization of files and folders between our computer and the cloud drive with 50Gb storage.
- [MEGAcmd](https://mega.nz/cmd): tool that allows access through the Mega cloud command line and provides a set of powerful commands for a file manipulation.

***DugongGUI*** allows a simple, quick and easy distribution of any bioinformatics application that can be installed on an Ubuntu operating system.  It also allows the generated containers to be used for a wide range of purposes, such as training, data analysis, tool implementation, devops, etc. In addition, it allows graphical visualization of results from different computational analyzes, such as graphs and figures of software and statistical tools, among others.

### DugongCMD <a name="DugongCMD" /> [[menu]](#menu)

This is the preinstalled software suite that enables better use of DugongCMD:

- [ASCIInema](https://asciinema.org/): is a free and open source solution for recording terminal sessions and sharing them on the web.
- [Showterm](https://showterm.io/): is an open source terminal record and upload application that lets you easy to record how-to in your terminal. It will record all your terminal activity in text-base and upload to showterm.io as a video and then generates a link for you to share with your team-mates or embed it in your website as an iframe.
- [MEGAcmd](https://mega.nz/cmd): tool that allows access through the Mega cloud command line and provides a set of powerful commands for a file manipulation.

Access to DugongCMD can be done through the following option:

- [tty.js](https://github.com/chjj/tty.js/): a terminal in your browser using node.js and socket.io. Based on Fabrice Bellard's vt100 for jslinux.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Bioinformatics Software <a name="Bioinformatics-Software" /> [[menu]](#menu)

Two open-source projects were integrated with [Dugong](https://hub.docker.com/r/dugong/dugong): [BioConda](https://bioconda.github.io/) and [Linuxbrew](http://linuxbrew.sh/), for the simple distribution of bioinformatics packages. 

### Conda and BioConda <a name="BioConda" /> [[menu]](#menu)

[***Conda***](https://conda.io) is a package manager that allows the installation, distribution and updating of different packages and their respective dependencies. It has a software distribution channel focused on bioinformatics tools called [Bioconda](https://bioconda.github.io).

Bioconda consists of:

- a repository of recipes hosted on GitHub
- a build system that turns these recipes into conda packages
- a repository of >2700 bioinformatics packages ready to use with conda install
- over 250 contributors that add, modify, update and maintain the recipes

For the installation of software through [***Conda***](https://conda.io) or [BioConda](https://bioconda.github.io/), simply execute the command below in a terminal in any version of [Dugong](https://hub.docker.com/r/dugong/dugong):

```
conda install <software>
```

Browse packages in the bioconda channel: [Available packages](https://bioconda.github.io/recipes.html#recipes)

For more details on the Conda Project, visit its [documentation](https://conda.io/docs/building/recipe.html#conda-recipe-files-overview).

#### EXAMPLE: Installation in Dugong using BioConda:

- Installing the bioinformatics tools: BWA and TOPHAT in DugongCMD. Installation performed through BioConda and operating test:

[![Watch the video](https://raw.githubusercontent.com/fabianomenegidio/dugong-bioinformatics/master/.misc/Screenshot%202017-05-09%20at%2001.33.06.png)](https://www.youtube.com/watch?v=FU944qartYE)

### LinuBrew <a name="LinuxBrew"/> [[menu]](#menu)

[Linuxbrew](http://linuxbrew.sh/) is a fork for Linux from [Homebrew](https://brew.sh/), the MacOS package manager, developed and maintained by Shaun Jackman. The project has [Homebrew Science](https://github.com/Homebrew/homebrew-science), a version focused on the distribution of scientific software. 

For the installation of software of bioinformatics through [Linuxbrew](http://linuxbrew.sh/) it is enough to execute the command below in a terminal in any version of [Dugong](https://hub.docker.com/r/dugong/dugong):

```
brew install homebrew/science/<software>
```

or

```bash 
brew tap homebrew/science
brew install <software> 
```

### DEB Repository <a name="DEB"/> [[menu]](#menu)

The installation of bioinformatics software in ***Dugong*** is extremely simple and can be run by Linuxbrew and Bioconda. In addition, it provides the BioLinux, CloudBioLinux and Linux Mint repositories for the apt-get package manager and for Synaptic.

There are currently 2707 bioinformatics packages available in the Bioconda repository, 673 in the Linuxbrew repository, and 250 in the BioLinux 8 repository.

The installation of bioinformatics packages in Dugong is not restricted to the methods presented. An example is BaseMount, the tool for mounting your BaseSpace Sequence Hub data as a Linux file system. With it, you can navigate projects, samples, runs, and application results and interact directly with associated files, just like any other local file system.

Sources such as GitHub, for example, can be used to install new tools simply and quickly.

![line](http://skstroi.ru/wp-content/uploads/2016/05/foot-line.png)

## Install Docker <a name="Install-Docker" /> [[menu]](#menu)

### Ubuntu: <a name="Ubuntu" /> [[menu]](#menu)

1. Set up the repository

Set up the Docker CE repository on Ubuntu. The lsb_release -cs sub-command prints the name of your Ubuntu version, like xenial or trusty.

    $ sudo apt-get -y install \
        apt-transport-https \
        ca-certificates \
        curl

    $ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

    $ sudo add-apt-repository \
        "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
        $(lsb_release -cs) \
        stable"

    $ sudo apt-get update

2. Get Docker CE

Install the latest version of Docker CE on Ubuntu:

    $ sudo apt-get -y install docker-ce

3. Test your Docker CE installation

Test your installation:

    $ sudo docker run hello-world


### Fedora <a name="Fedora" /> [[menu]](#menu)

1. Set up the repository

Set up the Docker CE repository on Fedora:

    $ sudo dnf -y install dnf-plugins-core

    $ sudo dnf config-manager \
        --add-repo \
        https://download.docker.com/linux/fedora/docker-ce.repo

    $ sudo dnf makecache fast
    
2. Get Docker CE

Install the latest version of Docker CE on Fedora:

    $ sudo dnf -y install docker-ce

Start Docker:

    $ sudo systemctl start docker

or

    $ sudo service docker start

3. Test your Docker CE installation

Test your installation:

    $ sudo docker run hello-world

### Windows: <a name="Windows" /> [[menu]](#menu)

Access: https://store.docker.com/editions/community/docker-ce-desktop-windows

### MacOS: <a name="MacOS" /> [[menu]](#menu)

Access: https://store.docker.com/editions/community/docker-ce-desktop-mac

![line](http://skstroi.ru/wp-content/uploads/2016/05/foot-line.png)

## Deploy and access Dugong <a name="Deploy" /> [[menu]](#menu)

The Docker project provides a public cloud called the [Docker Hub](https://hub.docker.com) for sharing the developed containers. This cloud allows access to the application in a centralized and simple way, that is, it is possible to obtain a complete Dugong environment with command lines for its implementation.

To start a container, the user must have Docker installed on his operating system, according to the tutorials available in the project documentation. The Dugong image is available in the [Docker Hub](https://github.com/fabianomenegidio/dugong-bioinformatics) and its use is the recommended method of installation.

Two steps are required to start a container containing Dugong. In the first step, the Dugong image is downloaded from the Docker Hub servers to the host, and in the second, a container is created on the host machine with the default Dugong installation. If the host machine is a Linux, the following commands must be performed in the terminal:

```
docker pull dugong/dugong
docker run -d -p 5901:5901 -p 6901:6901 --name Dugong -h Dugong -v $HOME/dugong/:/data/ \
--privileged dugong/dugong
```

At the end of the commands a Dugong instance will be available in the container named Dugong. Details about the container can be obtained through the command below:

```
docker ps
```
The default installation version of Dugong is DugongGUI with Xfce4. To change the installed version simply add one of the tags in the deploy command: ***xfce4***, ***icewm*** or ***cmd***.

Install DugongGUI Xfce4:

```
docker run -d -p 5901:5901 -p 6901:6901 --name DugongGUI -h DugongGUI -v $HOME/dugongxfce/:/data/ \
--privileged dugong/dugong:xfce
```

Install DugongGUI iceWM:

```
docker run -d -p 5901:5901 -p 6901:6901 --name DugongGUI -h DugongGUI -v $HOME/dugongicewm/:/data/ \
--privileged dugong/dugong:icewm
```

Install DugongCMD:

```
docker run -d -p 3000:3000 --name DugongCMD -h DugongCMD -v $HOME/dugongcmd/:/data/ \
--privileged dugong/dugong:cmd
```

Access to the Dugong container can be done in a variety of ways, with access through the simplest Docker console. This access will not be of great attraction to the user and should be used only in case of problems during the execution of Dugong and for the analysis of problems with the container. Through this access the user can restart Linux services, analyze system and application logs, among other functions.

To access the Docker console and access Dugong's bash, simply run the following command on the Linux terminal on your host machine:

```
docker exec -it Dugong /bin/bash
```

Two other methods for accessing DugongGUI is through VNC or noVNC. Ports 6901 and 5901 are respectively the VNC and noVNC execution ports. These ports are specified during container creation on the host machine and can be changed as per Docker documentation.

To access noVNC it is enough that the user directs his navigator to the address below, after starting the Dugong container. The default password for noVNC access is ***vncpassword*** and can be changed at any time. The default DugongGUI user is the ***dugong*** with the ***dugong*** password.

```
http://<IP or Host>:<port>/vnc_auto.html?password=vncpassword
```

A client is required for Dugong access through the VNC protocol. During the tests, the VNC® Viewer for Google Chrome application was used in the Chrome Web Store.

For access to DugongCMD the user can use an SSH client of his choice. We also provide access through the tty application, requiring only that the user direct their browser to the address below followed by port 3000. The default DugongCMD user is the ***dugong*** with the ***dugong*** password.

```
http://<IP or Host>:3000
```

## Video installation: <a name="Video-installation" /> [[menu]](#menu)

- Click to watch the installation of ***DugongGUI*** on ***Linux Ubuntu Server***:

[![Watch the video](https://raw.githubusercontent.com/fabianomenegidio/dugong-bioinformatics/master/.misc/Screenshot%202017-05-08%20at%2021.49.05.png)](http://showterm.io/2920acd0725f9fe78d3e5)

- Click to watch the installation of ***DugongGUI*** on ***Linux CentOS 7*** in the [CloudatCost](http://cloudatcost.com/) provider:

[![Watch the video](https://raw.githubusercontent.com/fabianomenegidio/dugong-bioinformatics/master/.misc/Screenshot%202017-05-10%20at%2006.30.41.png)](http://showterm.io/b521d2099d4e440461167#fast)


- Click to watch the installation of ***DugongCMD*** on ***Linux Ubuntu Server***:

[![Watch the video](https://raw.githubusercontent.com/fabianomenegidio/dugong-bioinformatics/master/.misc/Screenshot%202017-05-08%20at%2022.00.42.png)](http://showterm.io/65f18305c3a1dc80d7a2a)

- Click to watch the installation of ***DugongCMD*** on ***Linux CentOS 7*** in the [CloudatCost](http://cloudatcost.com/) provider:

[![Watch the video](https://raw.githubusercontent.com/fabianomenegidio/dugong-bioinformatics/master/.misc/Screenshot%202017-05-10%20at%2006.45.18.png)](http://showterm.io/f06861ae4a22381c148e4)

## Dugong Virtual Box <a name="Dugong-Virtual-Box" /> [[menu]](#menu)

The Dugong Virtual Box gets around the difficulty of installation by providing a functioning Dugong full install inside an Ubuntu or Fedora Linux virtual machine. You can use the Dugong Virtual Box on Mac OS X, Windows, or Linux.

It is strongly recommended that your system have 8 gigabytes or more of memory to use the Dugong Virtual Box.

- Download and install the VirtualBox (VB) version for your machine.
- Download the 64-bit Dugong Virtual Box, which is linked from the [Dugong Resources page](https://mega.nz/#F!cPhDUTTT!pXZy-CtLEvR4wx0uqpeqWQ). This file is large so it may take between a few minutes and a few hours depending on your Internet connection speed. You will need to unzip this file, which you can typically do by double-clicking on it.
- In the File menu, select Import Appliance. The Appliance Import wizard is displayed in a new window.
- Click Choose, browse to the location containing the *.ovf or *.ova file of the virtual machine of Dugong, and click Open.
- Make any adjustments you want to the displayed settings (you can also change the settings later) and click Import. The Appliance Import Wizard is closed and after a few moments, the imported virtual machine is listed in Oracle VM VirtualBox Manager.
- After the import, select the imported virtual machine and in the toolbar click the Settings button. Review the virtual machine settings to make sure that the virtual machine has the hardware it needs to operate. Make sure that the virtual machine has a CD/DVD drive.
- Once you have reviewed the settings, select the imported virtual machine and in the toolbar click the Start button. Verify that the virtual machine works.
- After the start of your virtual machine, execute the command below:

        docker start Dugong
        docker start DugongCMD
        docker start Dugong-CirComPara
       
- After starting the containers, enter the command below to obtain the ports for access through a browser:

        docker ps
        
- Finally, access the addresses below through a browser to access the respective versions of Dugong:
        
        DugongGUI and CirComPara: http://localhost:<port>/vnc_auto.html?password=vncpassword (ports displayed in the above command)
        DugongCMD: http://localhost:3000 (login: dugong / password: dugong)

## Extending or adapting the Dugong image <a name="Extending" /> [[menu]](#menu)

Dugong can be expanded or adapted to the most diverse needs in a research or teaching environment. All Dugong environment configuration scripts are available in the Git Hub (https://dugongbioinformatics.github.io/), including Dockerfile for building your image.

## Example of adapted tools in Dugong <a name="Example" /> [[menu]](#menu)

### CirComPara <a name="CirComPara" /> [[menu]](#menu)

***CirComPara*** is a computational pipeline to detect, quantify, and correlate expression of linear and circular RNAs from RNA-seq data.

- CircRNA analysis using a ***CirComPara*** tool on an ***Ubuntu Server*** with a ***DugongGUI*** container installed:

[![Watch the video](https://raw.githubusercontent.com/fabianomenegidio/dugongGUI-CirComPara/master/.misc/Screenshot%202017-05-09%20at%2000.57.47.png)](https://www.youtube.com/watch?v=8FlvmERIKJI)

See more: [DugongGUI CirComPara](https://github.com/fabianomenegidio/dugongGUI-CirComPara)

![line](http://skstroi.ru/wp-content/uploads/2016/05/foot-line.png)

![Docker](https://static1.squarespace.com/static/513914cde4b0f86e34bbb954/t/58409793bebafb1c4cfe75e3/1480628120385/DockerBanner.png)

## Author <a name="Author" /> [[menu]](#menu)

Current development is led by Fabiano Menegidio.

## Contributing <a name="Contributing" /> [[menu]](#menu)

You are invited to contribute new features, fixes, or updates, large or small; we are always thrilled to receive pull requests, and do our best to process them as fast as we can.

Before you start to code, we recommend discussing your plans through a GitHub issue, especially for more ambitious contributions. This gives other contributors a chance to point you in the right direction, give you feedback on your design, and help you find out if someone else is working on the same thing.

## MIT License <a name="MIT" /> [[menu]](#menu)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

***The software is provided "as is", without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose and noninfringement. in no event shall the authors or copyright holders be liable for any claim, damages or other liability, whether in an action of contract, tort or otherwise, arising from, out of or in connection with the software or the use or other dealings in the software.***


## Learn More <a name="Learn-More" /> [[menu]](#menu)

To learn more about Docker, go to:

http://docker.com

https://docs.docker.com/



![QRCode](https://raw.githubusercontent.com/fabianomenegidio/dugong-bioinformatics/master/.misc/qrcode.png)

[![DOI](https://zenodo.org/badge/88288867.svg)](https://zenodo.org/badge/latestdoi/88288867)
