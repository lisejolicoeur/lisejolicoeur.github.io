---
permalink: /
title: "Personal page of Lise Jolicoeur, 3rd year PhD Student at CEA"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hi! My name is Lise Jolicoeur and I am currently a 3rd year PhD Student at CEA, INRIA Bordeaux and University of Bordeaux.
After studying computer science at IUT d'Orsay for a 2-year degree, I got an engineering degree from Université de Technologie de Compiègne.

Background
======
------
Since the design of the first clusters dedicated to high performance computing more than 25 years ago, the field of high performance scientific computing has undergone massive evolution. The processing power of these clusters has been multiplied by several million by mobilizing a growing number of processing units with hierarchical and heterogeneous architectures. The use of high-performance computing has spread to most scientific fields, leading to the use of these machines for more and more diverse applications. They are integrated within workflows that can include pre- and post-processing steps or even the publication of results within community databases.

To meet these needs, computing centers must evolve the service that is offered using these clusters. The model generally used - a multi-user UNIX environment replicated uniformly on a set of compute nodes that users can allocate using a job manager is indeed reaching its limits. On the one hand, it is very difficult to maintain a uniform software environment to meet the needs of all users. On the other hand, job managers used in HPC are not fully adapted to dynamic workflows or workflows based on persistent services. Finally, these shared software environments offer a large attack surface, which makes it necessary to restrict the way they are used to protect against malicious users as much as possible.

At the same time, cloud computing providers have designed architectures that are intended from the outset to allow great flexibility in the execution of any type of calculation while guaranteeing strong isolation between their customers. However, using these cloud infrastructures for HPC often means deploying an architecture similar to that of a traditional cluster within the resources allocated by the provider. This requires duplicating management efforts for each group of users and does not allow pooling resources and skills as efficiently.


Thesis objectives
======
------
The main objective of this thesis is to show how we can bring cloud capabilities on HPC clusters by studying and implementing different approaches. To bring flexibility in HPC clusters and allow the execution of services and complex workflows, we develop a container network to create isolated user environments on top of HPC resources. This container network is implemented in PCOCC, a containerization software developped at CEA that integrates with Slurm to launched containerized jobs. We conduct multiple experiments to determine the impact of the container network on performance, as networking is a crucial component to optimize
the execution of HPC workloads. Additionally, we virtualize and benchmark RDMA communications in order to provide full isolation between workloads of different users
for all communications.
We also study two approaches for bringing flexibility to HPC clusters. In collaboration with the Lawrence Livermore National Laboratory that hosted me for a summer internship in 2024, we studied and benchmarked the execution of HPC applications in a rootless Kubernetes implementation called Usernetes. This approach enables
users to launch Kubernetes as a resource on HPC clusters to easily launch services alongside HPC applications on the same resources. In particular, we focused on
integrating RDMA and GPUs to reach near native performance for workloads running in Usernetes.
Finally, we studied the integration of another project called HPK on our cluster. HPK allows us to deploy a minimal Kubernetes cluster on HPC resources and 
launch Kubernetes workloads through Slurm. This approach enables a unified handling of resources on HPC clusters while giving users a Kubernetes interface to submit and manage workloads in a cloud native way. We focus on integrating PCOCC into this solution to have tight integration between workloads launched directly through Slurm and workloads launch with Kubernetes. 
Besides the technical contributions, we also propose a detailed state of the art of HPC and Cloud convergence to show how the ecosystem is evolving in both HPC and Cloud to support increasingly converged workflows that require both HPC and cloud capabilities.

