# SFTP Chart

This chart deploys an SFTP server and two pods, one for writing files and one for reading files.

## Prerequisites

- Kubernetes 1.16+
- Helm 3.0+

## Installation

To install the chart, run the following command:

```bash
helm install sftp-app ./sftp-ch
```

To uninstall the chart, run the following command:

```bash
helm uninstall sftp-app
```
## Working
We have a shared folder between writer and reader pods.
Writer pod uploads files to shared folder every 30 seconds
and reader reads all the files present in the shared folder
and copies them into its downloads folder.
