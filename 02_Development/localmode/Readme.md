For detail check the page;

https://docs.balena.io/learn/develop/local-mode


## Overview


# Develop locally

Local mode is the development mode for balena. It allows you to build and sync code to a single development device in your local network without having to go through the balenaCloud build service and deployment pipeline. It uses the Docker daemon on the device to build container images, and then the device Supervisor starts the containers in the same way as if they were deployed via the cloud.



## Local mode requirements

To use local mode on a device:

* The device must be running balenaOS v2.29.0 or higher.
* The device must be running a [development](https://docs.balena.io/reference/os/overview) variant of the OS.
* You must have the [balena CLI](https://docs.balena.io/reference/balena-cli/latest) installed on your development machine.
* Local mode must be enabled through the balenaCloud dashboard. You can enable it from the device *Settings* tab.


Full details about Docker uses in Balena can be found from following link

https://docs.balena.io/learn/develop/dockerfile

https://docs.balena.io/learn/develop/multicontainer

Docker Container

Balena uses [Docker](https://www.docker.com/) containers to manage deployment and updates. You can use one or more containers to package your services with whichever environments and tools they need to run.


docker-compose.yml file

The multicontainer functionality provided by balena is built around the [**Docker Compose**](https://docs.docker.com/compose/overview/) file format. The balena device supervisor implements a subset of the [Compose v2.1 feature set](https://docs.docker.com/compose/compose-file/compose-file-v2/). You can find a full list of supported and known unsupported features in our [device supervisor reference docs](https://docs.balena.io/reference/supervisor/docker-compose).



### Production images

At this point it makes sense to move from development balenaOS images to full production images, ensuring that your application still runs properly without full local console access. You can still [access](https://docs.balena.io/learn/manage/ssh-access) the host OS and containers via the balena dashboard and CLI, but the production balenaOS image will close all open inbound ports.

For Production and Enterprise plan users who require a stable, supported release, you should choose an [ESR version](https://docs.balena.io/reference/os/extended-support-release) of the host OS. An ESR version guarantees that you will only have to update the host OS on the devices at most twice a year to ensure you are on a supported version. You can view devices that have ESR versions of the host OS [here](https://docs.balena.io/reference/os/extended-support-release#supported-devices).



I have not touched about security and more...  I felt like the information that I accumulated and gather are good enought to start to use fleet
