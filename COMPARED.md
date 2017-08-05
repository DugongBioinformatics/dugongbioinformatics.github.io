## MENU <a name="menu" />

- [Comparison between Dugong and other bioinformatics services](#DugongCompare)
    - [Comparing Dugong to virtualization services](#DugongCompare)
    - [Comparing Dugong to Docker-based systems](#DugongCompare)
    - [Other services focused on bioinformatics](#DugongCompare)

## Comparing Dugong to other bioinformatics services <a name="DugongCompare" /> [[menu]](#menu)

In this page, we compare Dugong with the main tools available for bioinformatics analyses in virtualized platforms and Docker-based systems/services. We shortly describe the function of each tool and present a brief comparison regarding their main characteristics, in contrast to Dugong.

## Comparing Dugong to virtualization services:

Comparison between the main features provided by Dugong and the bioinformatics  tools [BioLinux](http://environmentalomics.org/bio-linux/), [CloudBioLinux](http://cloudbiolinux.org/), [CloVR](http://clovr.org) and [DNALinux](http://www.dnalinux.com).

![Comparative](https://raw.githubusercontent.com/DugongBioinformatics/dugongbioinformatics.github.io/master/.misc/comparative_cloud.png)

As we look at the table, we can see that Dugong provides a number of benefits compared to the tools based on virtualization technology analyzed herein.

Among these benefits, it is interesting to point Dugong´s lower consumption of computational resources (CPU, Memory, I/O), in contrast to virtualization technologies, such as Vmware and Virtual Box, for example. Thanks to Docker technology, Dugong also enables high scalability and the possibility of easy deployment on high-performance computing platforms.

Other benefits inherent in container technology, when compared to classical virtualization include faster boot time, better distribution of resources, direct access to hardware and reduced redundancy.

Another point worth mentioning is that most of the virtualization-based tools that were intended to provide a complete end-user work environment are no longer upgraded (CloVR and the classic version of CloudBioLinux), or entirely discontinued, (BioLinux and DNALinux).

## Comparing Dugong to Docker-based systems:

The major characteristics of Dugong, in comparison with other Docker-based bioinformatics systems ([AlgoRun](https://github.com/algorun/algorun), [GUIdock](https://github.com/WebDataScience/GUIdock) and [BioContainer](https://github.com/BioContainers))  can be viewed in the following table.

![Comparative](https://raw.githubusercontent.com/DugongBioinformatics/dugongbioinformatics.github.io/master/.misc/comparative_docker.png)

AlgoRun consists of a Docker-based packaging system that provides an interesting way to connect bioinformatics-related Docker images to a user-friendly graphic interface. However, integration of different tools to their specific graphic interfaces is still a time-consuming process and few applications have been fully integrated into the AlgoRun template, limiting their use in a larger variety of bioinformatics analyses.

In a similar way, GUIdock is a Docker Package containing the entire computational environment to run bioinformatics applications with a graphical user interface. However, the software is presented mostly as a proof of concept, focusing on Cytoscape tools, mostly associated with the analysis of biological networks. Thus, GUIdock does not support a whole range of applications for bioinformatics analyses, such as OMICS-related tools, for example.

Biocontainers provides Docker images integrated with the BioConda repository, which carries more than 2500 bioinformatics software in a standardized environment, with special emphasis on OMICS-related analytical tools and represents a major contribution to ensure data analyses through Docker-based systems. Nonetheless, Biocontainers operates exclusively through the Linux command line, hampering its use amongst less experienced users. Although future development of BioContainers may lead to its integration with the Galaxy graphical interface through [Galaxy Interactive Environments](https://galaxyproject.org/admin/gies/) (GIEs), GIE deployment is not a trivial operation, since they have complex interactions with numerous services. Moreover, implementation of the [Galaxy instance](https://galaxyproject.org/admin/get-galaxy/) displays large requirements for memory and disk space and [additional Galaxy tools](https://galaxyproject.org/admin/get-galaxy/#install-tools) have different requirements in computer memory, I/O speed, disk space, network bandwidth, density of computing cores, and parallel environment configurations, among other issues.

Dugong, on the other hand, is the most comprehensive Docker system developed so far, providing more than 3500 software available from three major open-source bioinformatics repositories: [BioConda](http://bioconda.github.io/), [LinuxBrew](http://linuxbrew.sh/) and BioLinux Repository. Software installation and management can be performed with the aid of an XFCE4 Graphic User Interface (GUI), which facilitates user interaction with different computing ecosystems, by enabling execution of a complete graphic work environment in personal computers, high performance computing systems (HPC), virtual private servers (VPS) and cloud computing environments. Dugong also incorporates the popular Jupyter Notebook, which allows software execution through pre-configured protocols (without the need for command typing) and provides a standardized mechanism to save and exchange protocols and results amongst users, which shall greatly contribute to ensure replicability and reproducibility of data analyses across laboratories.

## Other services focused on bioinformatics:

### BioShaDock and DockStore

[BioShaDock](https://docker-ui.genouest.org) and [DockStore](https://docker-ui.genouest.org): are Docker registries for bioinformatics tools. They contain Docker images dedicated to a broad spectrum of biological analyses. BioShaDock is a highly comprehensive repository, carrying command line tools, complex web server frameworks and Galaxy Docker images. Dockstore is focused on providing researchers different Docker-based bioinformatics software, which can be integrated into more complex processes through pipeline construction tools, such as Common Workflow Language (CWL) or Workflow Description Language (WDL). Dugong (and all the pre-configured software that it carries) can be integrated into Dockstore pipelines and used to visualize graphical results from different types of analyses.

### Go-Docker

[Go-Docker](http://www.genouest.org/godocker/): is a batch/cluster computing processing tool using Docker as an execution/isolation system, and can be used with environments based on Sun Grid Engine and Torque, among others. It acts as an additional layer above these tools on multiple user systems, where users do not have Docker privileges or expertise. However, Go-Docker does not send commands to remote nodes and requires integration with container management tools / orchestration systems, such as: Docker Swarm, Apache Mesos and Kubernetes, among others. Thus, its implementation depends on solid knowledge regarding high performance computing platforms. Nonetheless, after Go-Docker implementation by a Linux system administrator, users can execute Dugong containers (using mainly DugongCMD) to compose different pipelines and take advantage of the task scheduling system provided by Go-Docker. For more information on how to implement a Go-Docker environment, visit the [documentation](https://godocker.atlassian.net/wiki/spaces/GOD/overview) provided by the developer.
