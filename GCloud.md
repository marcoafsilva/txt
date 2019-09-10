# Installing and Configurating GCloud

## Quick Start

### Install GCloud

```
cd /opt/

sudo curl -O https://dl.google.com/dl/cloudsdk/channels/rapid/downloads/google-cloud-sdk-262.0.0-linux-x86_64.tar.gz

sudo tar xvf google-cloud-sdk-262.0.0-linux-x86_64.tar.gz

sudo ./google-cloud-sdk/install.sh

sudo vim ~/.bashrc

// Put the line below inside the ~/.bashrc file
export PATH="/opt/google-cloud-sdk/bin:$PATH"
```
