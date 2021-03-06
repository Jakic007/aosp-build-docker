# aosp-build-docker
Docker image for building AOSP roms. Great solution if you don't want to fiddle with your OS installation and dependencies but still want to build roms.

Minimal build environment for syncing device trees using repo tool and compiling ROM.

# Prerequisites

* Preferable some linux distribution(64 bit)
* Working *docker* instalation
* At least 250 GB of free disk space to check out code and an extra 150 GB to build it
* Minimum 8 GB of RAM but with that use option *-j1* for all commands to do everything single threaded

# How to use

* Clone this repository  
  `git clone <link>`
* Build docker image from provided Dockerfile.  
  `docker-compose build`
* Runs the built image interactively.
   `docker-compose up`

## How to sync
* Set up git config  
  ```
     git config --global user.name "Your Name"
     git config --global user.email "you@example.com"
  ```
* Initialize repository from AOSP manifest.  
  `repo init -u https://android.googlesource.com/platform/manifest`
* Finally sync and grab a coffee or two since it will take some time to download ~200 GB of data and check out.  
  `repo sync`
## How to build
* 
