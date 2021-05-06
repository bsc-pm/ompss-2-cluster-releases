# OmpSs-2 Releases

This meta-repository contains the official OmpSs-2@Clusters programming model's releases.

* OmpSs-2@Clusters Notes: https://github.com/bsc-pm/nanos6-cluster/blob/master/docs/cluster/Cluster.md

OmpSs-2@Clusters is based in the original OmpSs-2 and most of the documentation also valid.

* OmpSs-2 User Guide: https://pm.bsc.es/ompss-2-docs/user-guide  
* OmpSs-2 Specification: https://pm.bsc.es/ompss-2-docs/spec  
* OmpSs-2 Examples: https://pm.bsc.es/gitlab/ompss-2/examples  
* OmpSs-2 Docker Images: https://hub.docker.com/r/bscpm/ompss-2
* OmpSs-2 Release Notes: [NEWS.md](./NEWS.md)


# Getting Started

This repository contains all OmpSs-2@Clusters releases stored as *git tags*. These release
tags are named following the format `YYYY.MM[.PATCH]`, which can be, for instance,
`2021.05` or `2020.11.1`.

Firstly, clone this repository to your local computer:

```
$ git clone git@github.com:bsc-pm/ompss-2-cluster-releases.git
$ cd ompss-2-cluster-releases
```

After cloning this repository, run the following command to move to a particular
OmpSs-2 release:

```
$ git checkout 2021.05
```

Then, run the command below to download the Nanos6 and Mercurium
compiler sources in the `nanos6` and `mcxx` subfolders,
respectively. Those sources will be the ones that correspond to the
previously selected release.

```
$ git submodule update --init
```

Once these sources are downloaded, follow the installation instructions that are
detailed in the [User Guide](https://pm.bsc.es/ompss-2-docs/user-guide).
