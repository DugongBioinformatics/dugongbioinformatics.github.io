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

![Dugong](https://raw.githubusercontent.com/DugongBioinformatics/dugongbioinformatics.github.io/master/.misc/Dugong%20-%20images%20paper.png)

Through the simple Docker Client commands, the user can download the Dugong images **(a)**, and install and manage the containers generated using the Docker Daemon on the host computer **(b)**. The Dugong image is currently available in Docker Hub **(c)**, containing more than 3000 bioinformatics software and its dependencies thanks to the integration of the BioConda and LinuxBrew projects **(d)**. 

Among the software that can be installed in Dugong, and enjoy its graphical interface XFCE4, are: Blast2GO, UGene, Apache Taverna, Integrative Genomics Viewer (IGV), Mauve, RStudio, Cytoscape, QIIME **(e)**, among others. Some of these software are already functional in a Dugong image in our GitHub repository.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Test Dugong NOW!

To test the operation of Dugong and demonstrate the ease of use and the possibility of using the service in different operating systems and platforms we provide some installation templates on dply.co's servers.

**dply.co** allows the creation of an absolutely free server for two hours, and can be used for a longer time for payment. If you choose not to buy more time for the server, it is deleted automatically after 2 hours without any charge.

dply.co servers are hosted in the DigitalOcean cloud and have the following specifications:

- 1 CPU
- 512MB RAM
- 20GB Disk

We currently offer the following operating systems: CentOS 6, CentOS 7, Debian 7, Debian 8, Fedora 24, Fedora 25, Ubuntu 14.04, Ubuntu 16.04.

Test the Dugong on a machine with Ubuntu 16.04 by clicking the button:

[![Dply](https://dply.co/b.svg)](https://dply.co/b/mekdDIAk)

Learn more about Dply and other ways to test Dugong on other operating systems by [clicking here](https://github.com/DugongBioinformatics/Dply/blob/master/README.md).

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## MENU <a name="menu" />

- [Dugong flavours](#Dugong-flavours)
  - [DugongGUI Version](#DugongGUI)
  - [DugongCMD Version](#DugongCMD)
- [Installing Bioinformatics Software](#Bioinformatics-Software)
    - [Conda and BioConda](#BioConda)
    - [Anaconda Navigator](#Anaconda)
    - [LinuxBrew](#LinuxBrew)
    - [DEB Repository](#DEB)
- [Reproducibility and Replicability](#Reproducibility)
    - [Jupyter Notebook](#Jupyter)
    - [Getting the token and accessing the Jupyter Notebook](#AccessJupyter)
    - [Script and ScriptReplay Commands](#ScriptReplay)
- [Deploy Dugong Image](#Deploy)
    - [Deploy DugongGUI](#DeployDugongGUI)
    - [Deploy DugongCMD](#DeployDugongCMD)
- [Deploy Dugong Image by graphical interface](#DeployGUI)
    - [Kitematic (Windows and Mac)](#DeployGUI)
    - [Data Pulley (Linux)](#DeployGUI)
- [Access Dugong Container](#AccessDugong)
    - [Access through the Docker console](#DugongConsole)
    - [Access through the SSH protocol](#DugongSSH)
    - [Access through the VNC and noVNC](#DugongVNC)
    - [Access through a Web Terminal in Node.js](#DugongNode)
- [Extending or adapting the Dugong image](#Extending)
    - [Example of adapted tools, replicability and reproducibility in Dugong](#Example)
     - [CirComPara Pipeline](#CirComPara)
     - [CirComPara: Simulating reproducibility and replicability in alternative OS](#CirComPara)
     - [CirComPara: Simulating reproducibility and replicability using a pipeline in Jupyter Notebook](#CirComPara)
     - [CirComPara: Results of simulations](#CirComPara)
     - [CirComPara: Quick installation](#CirComPara)
- [Dugong Virtual Box](#Dugong-Virtual-Box)
    - [Deploy Dugong Virtual Box](#DugongVM)
- [Comparison between Dugong and other bioinformatics services](#DugongCompare)
    - [Comparing Dugong to virtualization services](#DugongCompare)
    - [Comparing Dugong to Docker-based systems](#DugongCompare)
    - [Other services focused on bioinformatics](#DugongCompare)
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

- [noVNC](http://kanaka.github.io/noVNC/noVNC/vnc.html):  is an HTML5-based remote desktop web client that can communicate with a remote VNC server via Web Sockets. The noVNC architecture is composed of 6 main components:

  - VNC / RFB Deployment Core: This component encapsulates all the intelligence of the RFB protocol and is the main machine that orchestrates everything else.
  - Canvas abstraction: This component provides an abstraction of the HTML5 Canvas APIs. It also has the Canvas detection functionality to handle browsers that do not have the full implementation of HTML5.
  - User Interface: Any interaction with the HTML DOM (except Canvas) is encapsulated in this component. It renders page controls such as the connect / disconnect button, settings, and the status of responses. This is the main component that allows easy integration of noVNC with Dugong and other tools.
  - Utilities: This contains several generic routines and extensions used by noVNC including: extensions to Javascript arrays to make them more useful as queues, event management between browsers, debugging / logging.
  - WebSockets Compatibility: Enables Flash (flex) emulation for browsers that do not have native support for WebSockets, as well as providing encryption support for WebSocktes.
  - WebSockets Proxy for TCP: a TCP-to-Websockets proxy script, which implements an initial validation similar to HTTP to establish the connection, and then each packet sent begins with a 0 (zero) byte and ends with a 255 byte. This proxy becomes necessary for translation between WebSockets and the standard TCP socket, while VNC does not implement native support for WebSockets.
  
  The following list shows full features offered by noVNC.

   - Supports all modern browsers including those on iOS, Android.
   - Supported VNC encodings: raw, copyrect, rre, hextile, tight, tightPNG
   - WebSocket SSL/TLS encryption (i.e. “wss://”) support
   - 24-bit true color and 8 bit colour mapped
   - Supports desktop resize notification/pseudo-encoding
   - Local or remote cursor
   - Clipboard copy/paste
   - Clipping or scrolling modes for large remote screens
   
  More information about noVNC can be found on the [project page](https://github.com/novnc/noVNC/wiki).

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

## Installing Bioinformatics Software <a name="Bioinformatics-Software" /> [[menu]](#menu)

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

Browse packages in the BioConda channel: [Available packages](https://bioconda.github.io/recipes.html#recipes)

For more details on the Conda Project, visit its [documentation](https://conda.io/docs/building/recipe.html#conda-recipe-files-overview).

#### EXAMPLE: Installation in Dugong using BioConda:

- Video installation of bioinformatics tools: BWA and TOPHAT in DugongCMD. Installation performed through BioConda and operating test:

[![Watch the video](https://raw.githubusercontent.com/fabianomenegidio/dugong-bioinformatics/master/.misc/Screenshot%202017-05-09%20at%2001.33.06.png)](https://www.youtube.com/watch?v=FU944qartYE)

### Anaconda Navigator <a name="Anaconda"/> [[menu]](#menu)

[Anaconda Navigator](https://docs.continuum.io/anaconda/navigator/) is a desktop graphical user interface (GUI) that allows to launch applications and easily manage conda packages, environments and channels without using command-line commands. 

Navigator is an easy, point-and-click way to work with packages and environments without needing to use conda commands in a terminal window. You can use it to find the packages you want, install them in an environment, run the packages and update them, all inside Navigator.

The DugongGUI version provides the [Anaconda Navigator](https://docs.continuum.io/anaconda/navigator/) in its graphical interface with the Conda and BioConda repositories configured and functional.

Below is a preview of the [Anaconda Navigator](https://docs.continuum.io/anaconda/navigator/) interface:

![Anaconda Navigator](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_yCq7aubg9ux_p.135391_1486144822844_anaconda_navigator.PNG)

For more details on the Anaconda Navigator, visit its [documentation](https://docs.continuum.io/anaconda/navigator/).

#### EXAMPLE: Installation in Dugong using Anaconda Navigator:

- Video installation of bioinformatics tools: BWA and TOPHAT in DugongGUI. Installation performed through Anaconda Navigator and operational test:

[![Watch the video](https://raw.githubusercontent.com/DugongBioinformatics/dugongbioinformatics.github.io/master/.misc/Screenshot%20from%202017-08-01%2001-18-04.png)](https://youtu.be/e9VOTzTOG7k)

### LinuxBrew <a name="LinuxBrew"/> [[menu]](#menu)

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

Browse packages in the LinuxBrew channel: [Available packages](http://braumeister.org/repos/Homebrew/homebrew-science/browse/a)

For more details on the LinuxBrew Project, visit its [documentation](https://github.com/Homebrew/brew/blob/master/docs/README.md).


### DEB Repository <a name="DEB"/> [[menu]](#menu)

In addition, it provides the [BioLinux](http://environmentalomics.org/bio-linux/), [CloudBioLinux](http://cloudbiolinux.org/) and [Linux Mint](https://www.linuxmint.com/) repositories for the apt-get package manager.

The installation of bioinformatics packages in [Dugong](https://hub.docker.com/r/dugong/dugong) is not restricted to the methods presented. Sources such as [GitHub](github.com), [Bitbucket](https://bitbucket.org), [Sourceforge](https://sourceforge.net), [Pypi](https://pypi.python.org/), among others, can be used to install new tools simply and quickly.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Reproducibility and Replicability <a name="Reproducibility"/> [[menu]](#menu)

Among the main objectives of the [Dugong](https://hub.docker.com/r/dugong/dugong) project is the provision of a complete work platform for the end user that allows the reproducibility and replicability of their research in the most diverse computational environments.

With this in mind, we implemented in all versions of [Dugong](https://hub.docker.com/r/dugong/dugong) the widely used [Jupyter Notebook](http://jupyter.org/), among other utilities focused on the reproducibility of analyzes composed by complex computational environments and pipelines with different execution dependencies.

### Jupyter Notebook <a name="Jupyter"/> [[menu]](#menu)

[Jupyter Notebook](http://jupyter.org/) extends the console-based approach to interactive computing in a qualitatively new direction, providing a web-based application suitable for capturing the whole computation analysis: developing, documenting, and executing code, as well as communicating the results. The [Jupyter Notebook](http://jupyter.org/) combines two components:

- **Web application**: a browser-based tool for interactive authoring of documents which combine explanatory text, mathematics, computations and their rich media output.

- **Notebook documents**: a representation of all content visible in the web application, including inputs and outputs of the computations, explanatory text, mathematics, images, and rich media representations of objects.

Main features of the web application:

- In-browser editing for code, with automatic syntax highlighting, indentation, and tab completion/introspection.
- The ability to execute code from the browser, with the results of computations attached to the code which generated them.
- Displaying the result of computation using rich media representations, such as HTML, LaTeX, PNG, SVG, etc. For example, publication-quality figures rendered by the matplotlib library, can be included inline.
- In-browser editing for rich text using the Markdown markup language, which can provide commentary for the code, is not limited to plain text.
- The ability to easily include mathematical notation within markdown cells using LaTeX, and rendered natively by MathJax.

Below is a preview of the [Jupyter Notebook](http://jupyter.org/) interface:

![Jupyter Notebook](https://docs.microsoft.com/pt-br/azure/virtual-machines/linux/media/jupyter-notebook/ipy-notebook-spectral.png)

[Dugong](https://hub.docker.com/r/dugong/dugong) provided the [Jupyter Notebook](http://jupyter.org/) with [Python 2.7.1](https://www.python.org/), the [IPython2 Kernel](http://ipython.readthedocs.io/en/stable/index.html) and the [Notebook Conda Kernel](https://docs.continuum.io/anaconda/user-guide/tasks/use-jupyter-notebook-extensions), this extension allows administration of the entire Conda environment and a package installation through the Jupyter interface. Below is a preview of the [Notebook Conda Kernel](https://docs.continuum.io/anaconda/user-guide/tasks/use-jupyter-notebook-extensions) interface:

![Jupyter Notebook](https://raw.githubusercontent.com/DugongBioinformatics/dugongbioinformatics.github.io/master/.misc/Screenshot%20from%202017-08-01%2002-22-16.png)

### Getting the token and accessing the Jupyter Notebook <a name="AccessJupyter" /> [[menu]](#menu)

To access Jupyter Notebook, first deploy one of the versions of Dugong, according to our [tutorials](#Deploy).

After deploy, enter the following command on the terminal of the host machine:

```
docker logs DugongGUI
```
or

```
docker logs DugongCMD
```
A message, similar to the one below, will be displayed:

```
[...]
[I 01:06:50.036 NotebookApp] [nb_conda_kernels] enabled, 2 kernels found
[W 01:06:50.258 NotebookApp] WARNING: The notebook server is listening on all IP addresses and not using encryption. This is not recommended.
[I 01:06:50.359 NotebookApp] [nb_conda] enabled
[I 01:06:50.365 NotebookApp] Serving notebooks from local directory: /headless/data
[I 01:06:50.365 NotebookApp] 0 active kernels 
[I 01:06:50.365 NotebookApp] The Jupyter Notebook is running at: http://[all ip addresses on your system]:8888/?token=60a698e3d55cd77ffb61eb138e16fd874c11ab994199e859
[I 01:06:50.365 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
[C 01:06:50.366 NotebookApp] 
    
    Copy/paste this URL into your browser when you connect for the first time,
    to login with a token:
        http://localhost:8888/?token=60a698e3d55cd77ffb61eb138e16fd874c11ab994199e859
```

Copy the Jupyter Notebook access address along with the token. Paste the address into the browser.

NOTE: If the access is not local, enter the IP / Hostname of the machine with the Jupyter Notebook next to the 8888 access port (Ex: http: // IP: 8888). In the new window, in the "Password or token" field, enter the previously obtained token.

For more details on the Jupyter Notebook, visit its [documentation](http://jupyter-notebook.readthedocs.io/en/latest/).

## Script and ScriptReplay Commands <a name="ScriptReplay"/> [[menu]](#menu)

The **script** and **scriptreplay** commands are used to record and play terminal sessions on Linux distributions, respectively. The sum of these commands in a pipeline allows reproducibility and replicability at the Linux command line and is available in all versions of [Dugong](https://hub.docker.com/r/dugong/dugong).

The **script** command stores terminal activities in a log file that will be named by a user, when a name is not provided by a user, the default file name is used. The **scriptrepaly** command helps to reproduce information in your log file used with the script command. The timing information is explained by the --timing = file option used with the command and the file generated by the previous command.

More details on the commands can be obtained through the video below:

[![Watch the video](https://raw.githubusercontent.com/DugongBioinformatics/dugongbioinformatics.github.io/master/.misc/Screenshot%20from%202017-08-01%2002-59-05.png)](https://www.youtube.com/watch?v=BGdxsjiLF-U)

Channel video: https://www.linuxhelp.com/script-scriptreplay-commands-linux-examples/

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Deploy Dugong Image <a name="Deploy" /> [[menu]](#menu)

The [Dugong](https://hub.docker.com/r/dugong/dugong) project provides a public cloud called the  for sharing the developed containers. This cloud allows access to the application in a centralized and simple way, that is, it is possible to obtain a complete Dugong environment with command lines for its implementation.

To start a container, the user must have Docker installed on his operating system, according to the [tutorials available in the project documentation](https://docs.docker.com/engine/installation/#server). The [Dugong image](https://github.com/fabianomenegidio/dugong-bioinformatics) is available in the [Docker Hub](https://hub.docker.com) and its use is the recommended method of installation.

Two steps are required to start a container containing [Dugong](https://hub.docker.com/r/dugong/dugong). In the first step, the [Dugong image](https://github.com/fabianomenegidio/dugong-bioinformatics)  is downloaded from the [Docker Hub](https://hub.docker.com) servers to the host, and in the second, a container is created on the host machine with the default [Dugong](https://hub.docker.com/r/dugong/dugong) installation. If the host machine is a Linux, the following commands must be performed in the terminal:

```
docker pull dugong/dugong
docker run -d -p 5901:5901 -p 6901:6901 -p 8888:8888 -p 2222:22 --name Dugong -h Dugong -v $HOME/dugong/:$HOME/data/ \
--privileged dugong/dugong
```

At the end of the commands a Dugong instance will be available in the container named Dugong. Details about the container can be obtained through the command below:

```
docker ps
```

The default installation version of Dugong is DugongGUI with XFCE4. 

To change the installed version simply add one of the tags in the deploy command: ***xfce4***, ***icewm*** or ***cmd***.

### Deploy DugongGUI Image <a name="DeployDugongGUI" /> [[menu]](#menu)

Install DugongGUI Xfce4:

```
docker run -d -p 5901:5901 -p 6901:6901 -p 8888:8888 -p 2222:22 --name DugongGUI -h DugongGUI \
  -v $HOME/dugongxfce/:$HOME/data/ --privileged dugong/dugong:xfce4
```

Install DugongGUI iceWM:

```
docker run -d -p 5901:5901 -p 6901:6901 -p 8888:8888 -p 2222:22 --name DugongGUI -h DugongGUI \
-v $HOME/dugongicewm/:$HOME/data/ --privileged dugong/dugong:icewm
```

### EXAMPLE: Video installation DugongGUI:

- Click to watch the installation of ***DugongGUI*** on ***Linux Ubuntu Server***:

[![Watch the video](https://raw.githubusercontent.com/fabianomenegidio/dugong-bioinformatics/master/.misc/Screenshot%202017-05-08%20at%2021.49.05.png)](http://showterm.io/2920acd0725f9fe78d3e5)

- Click to watch the installation of ***DugongGUI*** on ***Linux CentOS 7*** in the [CloudatCost](http://cloudatcost.com/) provider:

[![Watch the video](https://raw.githubusercontent.com/fabianomenegidio/dugong-bioinformatics/master/.misc/Screenshot%202017-05-10%20at%2006.30.41.png)](http://showterm.io/b521d2099d4e440461167#fast)

### Deploy DugongCMD Image <a name="DeployDugongCMD" /> [[menu]](#menu)

Install DugongCMD:

```
docker run -d -p 3000:3000 -p 8888:8888 -p 2222:22 --name DugongCMD -h DugongCMD \
  -v $HOME/dugongcmd/:$HOME/data/ --privileged dugong/dugong:cmd
```

### EXAMPLE: Video installation DugongCMD:

- Click to watch the installation of ***DugongCMD*** on ***Linux Ubuntu Server***:

[![Watch the video](https://raw.githubusercontent.com/fabianomenegidio/dugong-bioinformatics/master/.misc/Screenshot%202017-05-08%20at%2022.00.42.png)](http://showterm.io/65f18305c3a1dc80d7a2a)

- Click to watch the installation of ***DugongCMD*** on ***Linux CentOS 7*** in the [CloudatCost](http://cloudatcost.com/) provider:

[![Watch the video](https://raw.githubusercontent.com/fabianomenegidio/dugong-bioinformatics/master/.misc/Screenshot%202017-05-10%20at%2006.45.18.png)](http://showterm.io/f06861ae4a22381c148e4)

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Deploy Dugong Image by graphical interface  <a name="DeployGUI"/> [[menu]](#menu)

[Kitematic](https://github.com/docker/kitematic) is a simple application for managing Docker containers on Mac and Windows, allowing the deploy of Docker images and the installation and administration of containers. Dugong can be installed through [Kitematic](https://github.com/docker/kitematic) or other softwares with the same function, such as [Data Pulley](http://datapulley.com/).

Kitematic:

![Kitematic](https://cloud.githubusercontent.com/assets/251292/8246120/d3ab271a-15ed-11e5-8736-9a730a27c79a.png)

Data Pulley

![Data Pulley](http://35.184.241.64/images/Pull.png)

For more details, visit the projects page.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Access Dugong Container <a name="AccessDugong"/> [[menu]](#menu)

### Access through the Docker console <a name="DockerConsole"/> [[menu]](#menu)

Access to Dugong containers can be done in many ways, with access through the simplest Docker console. This access will not be of great attraction to the user without command line experience and should only be used in case of problems while running Dugong. Through this access, the user can restart Linux services, analyze system logs and applications, among other functions. To access the Docker console, simply run the following command on the Linux terminal on your host machine:

```
docker exec -it Dugong /bin/bash
```

### Access through the SSH protocol <a name="DugongSSH"/> [[menu]](#menu)

Access through the SSH protocol is also available in all versions of Dugong. 

The Dugong execution command includes the "-p 2222: 22" option, where we direct the SSH port of the container to port 2222 of the host. To access Dugong by SSH, from your host machine, simply execute the following command:

```
ssh -p 2222 dugong@localhost
```

The **dugong** user's default password (**dugong**) will be requested at that time. This password can be changed through the command: **passwd dugong**

### Access through the VNC and noVNC <a name="DugongVNC" /> [[menu]](#menu)

Two other methods for accessing DugongGUI is through VNC or noVNC. Ports 6901 and 5901 are respectively the VNC and noVNC execution ports. These ports are specified during container creation on the host machine and can be changed as per Docker documentation (**-p 6901:6901 -p 5901:5901**).

To access noVNC it is enough that the user directs his navigator to the address below, after starting the Dugong container. The default password for noVNC access is ***vncpassword*** and can be changed at any time. The default DugongGUI user is the ***dugong*** with the ***dugong*** password.

```
http://<IP or Host>:<port>/vnc_auto.html?password=vncpassword
```

A client is required for Dugong access through the VNC protocol. During the tests, the VNC® Viewer for Google Chrome application was used in the Chromebook:

![VNC](https://raw.githubusercontent.com/DugongBioinformatics/dugongbioinformatics.github.io/master/.misc/Screenshot%20from%202017-08-01%2004-17-39.png)

![VNC](https://raw.githubusercontent.com/DugongBioinformatics/dugongbioinformatics.github.io/master/.misc/Screenshot%20from%202017-08-01%2004-18-33.png)

### Access through a Web Terminal in Node.js <a name="DugongNode" /> [[menu]](#menu)

For access to DugongCMD the user can use an SSH client of his choice. We also provide access through the tty application, requiring only that the user direct their browser to the address below followed by port 3000. The default DugongCMD user is the ***dugong*** with the ***dugong*** password.

```
http://<IP or Host>:3000
```

Example of access through the Web Terminal in a Google Chrome:

![WebTerminal](https://raw.githubusercontent.com/DugongBioinformatics/dugongbioinformatics.github.io/master/.misc/Screenshot%20from%202017-08-01%2004-24-06.png)

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Extending or adapting the Dugong image <a name="Extending" /> [[menu]](#menu)

Dugong can be expanded or adapted to the most diverse needs in a research or teaching environment. All Dugong environment configuration scripts are available in the Git Hub (https://dugongbioinformatics.github.io/), including Dockerfile for building your image.

### Example of adapted tools, replicability and reproducibility in Dugong <a name="Example" /> [[menu]](#menu)

#### CirComPara Pipeline <a name="CirComPara" /> [[menu]](#menu)

***CirComPara*** is a computational pipeline to detect, quantify, and correlate expression of linear and circular RNAs from RNA-seq data.

- Video from a CircRNA analysis using the CirComPara tool on an Ubuntu Server with a DugongGUI container installed. The video presents a complete implementation of CirComPara with the test data provided by the authors and their expected results:

[![Watch the video](https://raw.githubusercontent.com/DugongBioinformatics/dugongbioinformatics.github.io/master/.misc/Screenshot%20from%202017-08-01%2004-41-23.png)](https://www.youtube.com/watch?v=8FlvmERIKJI)

For more information on adapting CirComPara to Dugong and accessing analysis results using Dugong and CirComPara in different computing environments, go to: [DugongGUI CirComPara](https://github.com/DugongBioinformatics/DugongRepository/tree/master/GUI/CirComPara/XFCE4)


---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Dugong Virtual Box <a name="Dugong-Virtual-Box" /> [[menu]](#menu)

The Dugong Virtual Box gets around the difficulty of installation by providing a functioning Dugong full install inside an Ubuntu, Fedora or Arch Linux virtual machine. You can use the Dugong Virtual Box on Mac OS X, Windows, or Linux.

### Deploy Dugong Virtual Box <a name="DugongVM" /> [[menu]](#menu)

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

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Comparison between Dugong and other bioinformatics services <a name="DugongCompare" /> [[menu]](#menu)

We provide a comparison of Dugong with the main tools available for analysis of bioinformatics in virtualized platforms and Docker. 

To view this comparison [click here](https://github.com/DugongBioinformatics/dugongbioinformatics.github.io/blob/master/COMPARED.md).

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

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

[![DOI](https://zenodo.org/badge/88288867.svg)](https://zenodo.org/badge/latestdoi/88288867)
