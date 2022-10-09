# Integrate-Ray-ODH-on-MOC
Collabrate with Red hat Mentors to integrate Ray on MOC(smaug cluster)
Ray with ODH on MOC

# Vision and Goals Of The Project:
The project aims to integrate Ray with Mass Open Cloud (MOC). Ray is a unified framework for scaling AI and Python applications. It is currently used to deploy Open Data Hub (ODH), a service platform for AI service on Red Hat's Kubernetes-based OpenShift® Container Platform and Ceph Object Storage. Our ultimate goal for this project is to be able to deploy and scale Open Data Hub services using Ray on MOC.

The objectives of the project can be divided into four components:
1.    Installing Red Hat's Kubernetes-based OpenShift® Container Platform on MOC
2.    Deploying ODH deployment on MOC-based OpenShift Containers
3.    Installing Ray on MOC 
4.    Using Ray to scale ODH services on MOC-based OpenShift Containers

# Users/Personas Of The Project:
Data Scientists/Engineer: Will use Ray to scale their ML workloads. They can use Ray along with other tools in the ODH.
DevOps Engineer: Will make sure that the Ray cluster/ Operator is up and running. 
# Scope and Features Of The Project:
This project will include understanding RAY, Kubernetes, and Operate First on a high level, integrating RAY on MOC, troubleshooting any unexpected issues and testing the whole pipeline with real-life examples. This project will be presented in front of the Cloud Computing at Boston University and the Operate First team at RedHat. For our final product, ideally, RAY would be seamlessly integrated into a user-friendly interface, i.e. jupyter notebook, so that the parallelization will be taken care of in the background and a status indicator will be displayed in the foreground.
# Solution Concept
Our goal is to integrate Ray with ODH on MOC but let’s take a look at its integration on Openshift:


Figure: Architecture of Ray Integration with ODH on Openshift

This image shows how Ray helps to parallelize tasks in the AI pipeline of ODH on the Openshift. Openshift is a Kubernetes-based container platform and Open Data Hub (ODH) provides a blueprint to building an AI as a service on this platform. As you write @ray.remote in the start of your code in the ODH pipeline, Ray operator creates pods which parallelize the tasks and help to scale the AI and python workloads. 

In our ideal solution we aim to replicate the same integration of Ray with ODH on Mass Open Cloud (MOC). We plan to start by setting up the CRC (which is a minimal OpenShift 4.x cluster setup on a local laptop or desktop computer) on one of the local machines. Then we shall move to the setup of ODH on CRC and then to install the Ray operator on it. This will help us understand the integrations of Ray with Openshift. If everything works fine on CRC then we’ll move to replicate that on MOC as our final release.
# Acceptance criteria

Our acceptance criterion for this project is that we expect to fulfill all previous requirements and planning. In the final presentation, the team is expected to share information on how to replicate the same integration of Ray with ODH on Mass Open Cloud, as well as feature-specific information. At the end of the semester, we have at least a deep understanding of the following Kubernetes operators and Kube deployment concepts: operators, CRD, CR, roles+rolebindings+service-accounts, services and routes, pods. We are aware that Open Data Hub can be customized through the use of user profiles. In what manner does Ray operate at the user interface and deployment levels. We plan to implement something similar to Ray'scombination of ODH and MOC. The first step will be to set up CRC on one of the local computers. Further, we will install the Ray operator and configure ODH on CRC. Learning how Ray and Openshift work together is essential. We will make a final release to the public if all tests pass on CRC, after which we will do the same on MOC.
# Release Planning:
We plan to setup openshift(crc) on our vms by 10 oct.
We plan to setup ray operator  on our openshift cluster on vms by 24 oct.
We deploy ODH and test our data pipeline.
We test Ray + ODH deployments manually on our namespace in smaug cluster on moc.
We raise PR for ray operator on smaug cluster by 9 December.
