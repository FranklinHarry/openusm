# Open Universal Systems Manager

![alt text](https://github.com/openusm/openusm/blob/master/images/openusm_logo.png)

A modern approach to DellEMC Server Management & Insight Logs Analytics solution integrated with monitoring & logging pipeline using Docker,  Redfish & ELK Stack.

# Highlights

- OpenUSM is a suite of open source tools/scripts which purely uses Redfish API to perform Server Management tasks & Insight Log Analytics using Dockerized ELK Stack.
- OpenUSM can be bundled as Docker Images which is lightweight, stand-alone, executable package of a piece of software that includes everything needed to run it: code, runtime, system tools, system libraries, settings. Hence, no need of host dependencies packages
- OpenUSM is an out-of-band system management solution purely based on Redfish API Interface.
- It is a platform agnostic solution(can be run from laptop, server or cloud) and works on any of Linux or Windows platform with Docker Engine running on top of it.
<br></br>

![alt text](https://github.com/openusm/openusm/blob/master/images/kibana_openusm.png)
<p>    ------------------- Kibana visualizing Pie-Chart for LC logs collected over the last 1 year time period--------------------</p>

# Value Proposition

- OpenUSM architecture can scale both vertically & horizontally
- OpenUSM architecture can be easily integrated and extended with 3rd party open source tools.(example - the choice of InfluxDB instead of Prometheus as monitoring tool, using 3rd Party logging tool instead of ELK stack etc.)
- OpenUSM bundle can be built and customized by anyone based on the needs and holds a plug-and-play components and functionalities.
- OpenUSM can easily be integrated with Chef/Ansible/Puppet for automating the Server Management tasks/operations.

# Architecture

![alt text](https://github.com/openusm/openusm/blob/master/images/how_openusm_works.png)

# How openUSM works?

OpenUSM uses "Container-Per-Server(CPS)" model. For each server management tasks, there are Python-scripts which when executed builds and run Docker containers, uses Redfish API to communicate directly with Dell iDRAC, collects iDRAC/LC logs and pushes it to ELK(Elasticsearch, Logstash & Kibana) stack for further log analytics.For n-number of Dell Servers, the overall iDRAC/LC logs gets collected to centralized ELK stack which again runs as Microservices inside Docker containers. One can easily see iDRAC logs under Kibana UI. OpenUSM uses Prometheus Stack for monitoring System components like GPU/CPU monitoring using NVIDIA-DOCKER & Node Exporter. 



![alt text](https://github.com/openusm/openusm/blob/master/images/openusm_architecture.png)


# Getting Started with OpenUSM

## Preparing Your System

[Ubuntu](docs/os/ubuntu-installation.md) <br>
[Debian](docs/os/debian-installation.md) <br>
[CentOS](docs/os/centos-installation.md) <br>
[RHEL](docs/os/rhel-installation.md) <br>

OpenUSM is a suite of tools and utilities which configures and manage the lifecycle of system management. OpenUSM has a capability to perform the following functions:

[BIOS Token Change](docs/bios-token.md) <br>
[Firmware Update](docs/firmware.md)<br>
[Pushing iDRAC Logs to ELK Stack](docs/idrac2elk.md)


## Documentation

Check out our guides for documentation, deployment guides and tutorials.

## Roadmap ahead

Refer [Report](https://github.com/openusm/openusm/tree/master/reports) section to track what new features and improvement are coming next in OpenUSM.

# How do I become a contributor?

We invite new contributors to contribute towards this project repository. We would also ask you to propose any improvements or contributions for future releases.
