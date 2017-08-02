## Comparison between Dugong and other bioinformatics services <a name="DugongCompare" /> [[menu]](#menu)

Below we compare Dugong with the main tools available for analysis of bioinformatics in virtualized platforms and Docker. We briefly describe the function of each tool and present a brief comparison of the characteristics available in contrast to Dugong.

## Comparison between Dugong and virtualization services:

Comparison between the main features provided by Dugong and the tools for bioinformatics [BioLinux](http://environmentalomics.org/bio-linux/), [CloudBioLinux](http://cloudbiolinux.org/), [CloVR](http://clovr.org) and [DNALinux](http://www.dnalinux.com).

As one of the methodologies used initially to provide a complete bioinformatics work environment independent of the host machine, several tools based on virtualization technology have been developed over time.

Some projects such as BioLinux, DNALinux and CloudBioLinux have sought to implement an easy-to-use virtual desktop for the end user, but these projects are no longer available or are not up to date, making it difficult to deploy or use with new users. Projects such as CloVR have made available full workflows in virtual environments such as Virtual Box and Vmware, but have also been discontinued or not updated to meet the current demands of new users.

Although virtualization has been a widely used approach to minimizing replicability and reproducibility issues in bioinformatics, high computational cost, low scalability, and difficulties in jointly deploying high performance computing platforms have proven to be new challenges for the community.

![Comparative](https://raw.githubusercontent.com/DugongBioinformatics/dugongbioinformatics.github.io/master/.misc/comparative_cloud.png)

## Comparison between Dugong and Docker services:

Comparison between the main features provided by Dugong and the tools for bioinformatics [BioContainer](https://github.com/BioContainers), [GUIdock](https://github.com/WebDataScience/GUIdock) and [AlgoRun](https://github.com/algorun/algorun).

![Comparative](https://raw.githubusercontent.com/DugongBioinformatics/dugongbioinformatics.github.io/master/.misc/comparative_docker.png)

In analyzing the comparative table we can see that Dugong is the most complete Docker service available so far, focused on implementing a work environment for bioinformatics analysis directed at the end user.

Even with the availability of several tools for the replicability and reproducibility of computational analysis, in addition to a complete graphical user interface independent of the host machine, Dugong presents a final image size very close to the other tools evaluated, justifying its adoption as a working environment.

## Other services focused on bioinformatics:

### BioShaDock

[BioShaDock](https://docker-ui.genouest.org): is a Docker registry for BioInformatics. In it are hosted Docker images dedicated to a broad spectrum of biological communities represented by the Biogenouest Western France network.

In particular, it provides:

- Command Line Tools
- Complex web server structures
- Images of Galaxy Docker that you can use with the specific Galaxy Docker tools, thanks to recent developments through the e-Biogenouest project (see our Toolshed)

**OBS:** We tried to make Dugong available on the Registry to compose your list of tools, but unfortunately attempts to register through your form presented the **Forbidden Error**, even following the tool's documentation.

### DockStore

[DockStore](https://docker-ui.genouest.org): is a Docker registry which provides a place for users to share tools encapsulated in Docker and described with the Common Workflow Language (CWL) or Workflow Description Language (WDL). This allows scientists to share analytical workflows so that they are machine readable and can be run in a variety of environments. While the Dockstore is focused on serving researchers in biosciences, the combination of Docker + CWL / WDL can be used by anyone to describe the tools and services in their Docker images in a standardized, machine-readable way.

Although not intended to provide a comprehensive, end-user focused desktop but a repository with different tools implemented in Docker technology and that can work together after adapting to the CWL environment requirements, we will soon release DugongGUI (XFCE4) and DugongCMD in the Registry DockStore.

The implementation of Dugong in the DockStore repository will provide a new option for the user of this service, which can add steps in their workflow that depend on tools with graphical interfaces. With this, you can perform analysis and visualize graphical data as an additional step in your pipeline, without the need to use a local workstation.

In the future, we'll also provide examples of how Dugong can be implemented in CWL workflows using the Dockstore.

Likewise, Dugong becomes a great choice for developers who need to autonomously deploy a Docker image with graphical interface in their future workflow or who want to make their graphical tool available in the Dockstore repository. Dugong adapts as a base image for the implementation of different tools.

### Go-Docker

[Go-Docker](http://www.genouest.org/godocker/): is a batch/cluster computing processing tool using Docker as an execution/isolation system, and can be used with environments with Sun Grid Engine, Torque, among others. However, Go-Docker does not manage to send the commands to the remote nodes, requiring integration with container management tools, such as: Docker Swarm, Apache Mesos, Kubernetes, among others. It acts as an additional layer above these tools on multiple user systems, where users do not have Docker privileges or expertise.

Its implementation depends on solid knowledge in a high performance computing environment using platforms such as Sun Grid Engine, Torque, SLURM, among others. It also requires knowledge about the Docker platform and orchestration systems, such as those already mentioned: Docker Swarm, Apache Mesos, Kubernetes, among others.

After the implementation by a Linux system administrator, the end user can execute containers with Dugong, mainly DugongCMD, to compose different pipelines and take advantage of the task scheduling system provided by Go-Docker.

For more information on how to implement a Go-Docker environment, visit the [documentation](https://godocker.atlassian.net/wiki/spaces/GOD/overview) provided by the developer.
