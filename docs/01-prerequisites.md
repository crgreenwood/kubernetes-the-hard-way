# Prerequisites

## IBM Cloud Platform

This tutorial leverages the [IBM Cloud Platform](https://cloud.ibm.com/) to streamline provisioning of the compute infrastructure required to bootstrap a Kubernetes cluster from the ground up. [Sign up](https://cloud.ibm.com). Note that it is possible to gain up to $1200 credit on new accounts using a quick search in [Google](https://www.google.com/search?q=ibm+cloud+free+credit)

**TBC** Estimated cost to run this tutorial: $0.22 per hour ($5.39 per day).

> The compute resources required for this tutorial exceed the Google Cloud Platform free tier.

## IBM Cloud CLI

### Install the IBM Cloud CLI

Follow the IBM Cloud CLI [documentation](https://console.bluemix.net/docs/cli/reference/ibmcloud/download_cli.html) to install and configure the `ibmcloud` command line utility.

Verify the Google Cloud SDK version is 218.0.0 or higher:

```
ibmcloud -v
```

### Set a Default Compute Region and Zone

This tutorial assumes a default compute region and zone have been configured.

If you are using the `gcloud` command-line tool for the first time `init` is the easiest way to do this:

```
gcloud init
```

Otherwise set a default compute region:

```
gcloud config set compute/region us-west1
```

Set a default compute zone:

```
gcloud config set compute/zone us-west1-c
```

> Use the `gcloud compute zones list` command to view additional regions and zones.

## Running Commands in Parallel with tmux

[tmux](https://github.com/tmux/tmux/wiki) can be used to run commands on multiple compute instances at the same time. Labs in this tutorial may require running the same commands across multiple compute instances, in those cases consider using tmux and splitting a window into multiple panes with `synchronize-panes` enabled to speed up the provisioning process.

> The use of tmux is optional and not required to complete this tutorial.

![tmux screenshot](images/tmux-screenshot.png)

> Enable `synchronize-panes`: `ctrl+b` then `shift :`. Then type `set synchronize-panes on` at the prompt. To disable synchronization: `set synchronize-panes off`.

Next: [Installing the Client Tools](02-client-tools.md)
