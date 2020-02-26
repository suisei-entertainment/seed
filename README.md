<h1 align="center">
    <a name="logo" href="https://www.suiseientertainment.com">
        <img src="https://raw.githubusercontent.com/suisei-entertainment/seed/release/assets/suisei_logo_big.png"
             alt="Suisei Entertainment"
             width="1000">
    </a>
    <br>
    <div style="height:80px;font-family:courier;font-size:150%"> SEED Virtual Reality Platform </div>
</h1>

<div align="center">
    <h4>
        <a href="https://travis-ci.org/suisei-entertainment/seed">
            <img src="https://travis-ci.org/suisei-entertainment/seed.svg?branch=development"/>
        </a>
        <a href="https://codeclimate.com/github/suisei-entertainment/seed/test_coverage">
          <img src="https://api.codeclimate.com/v1/badges/f3851432c921cac51934/test_coverage" />
        </a>
        <a href="https://codeclimate.com/github/suisei-entertainment/seed/maintainability">
          <img src="https://api.codeclimate.com/v1/badges/f3851432c921cac51934/maintainability" />
        </a>
        <a href="https://snyk.io/test/github/suisei-entertainment/seed?targetFile=requirements.txt">
          <img src="https://snyk.io/test/github/suisei-entertainment/seed/badge.svg?targetFile=requirements.txt" alt="Known Vulnerabilities" data-canonical-src="https://snyk.io/test/github/suisei-entertainment/seed?targetFile=requirements.txt" style="max-width:100%;">
        </a>
        <a href="https://github.com/suisei-entertainment/stargazers">
            <img src="https://img.shields.io/github/stars/suisei-entertainment/seed.svg?style=plasticr"/>
        </a>
        <a href="href="https://github.com/suisei-entertainment/seed/commits/developmen">
            <img src="https://img.shields.io/github/last-commit/suisei-entertainment/seed.svg?style=plasticr"/>
        </a>
        <a href="href="https://github.com/suisei-entertainment/seed/commits/development">
            <img src="https://img.shields.io/github/license/suisei-entertainment/seed.svg?style=plasticr"/>
        </a>
    </h4>
</div>

This is the main repository of the SEED virtual reality platform.

# Features

# Directory Structure

+ **.env**: The directory containing the virtual Python environment created by
virtualenv. Only present when working in a virtual environment.
+ **.git**: The directory containing Git internals. Do not touch, unless you
absolutely know what you are doing.
+ **.sde**: Contains various files created by SDE while working on the platform. Only present if SDE has already been executed at least once.
+ **assets**: Contains all binary assets, typically images and other media.
+ **scripts**: Contains various utility scripts mainly utilized by CI.
+ **src**: Contains the source code of the platorm.

Each subdirectory contains additional README.md files with a description of
the content of that subdirectory.

# Requirements

## Hardware Requirements (Development)

Working on SEED requires a fairly recent computer with one of
the following supported operating systems:

* Apple Mac OS X 10.13.2 'High Sierra' or later
* Ubuntu 18.04 LTS or later
* Windows 10 or later

In terms of hardware, the recommended configuration for development is at
least an 8-core CPU with 8 GB RAM, and preferrably a fast SSD.

## Hardware Requirements (Deployment)

Running a headless SEED node requires the following hardware:

* **CPU:** It is recommended to have at least 8 CPU cores.
* **Memory:** The actual memory requirement heavily depends on the actual
services running on the node, but at least 8 GB memory is recommended. Nodes
acting as a data cache or database are recommended to have at least 32 GB of
RAM.
* **Network**: The minimum network bandwidth required by a SEED node is at least a 100 Mbps symmetrical connection, but 1 Gbps symmetrical connection is
recommended.
* **Storage**: For a normal SEED node, storage is mostly used only for
logging. Still, a fast, preferably NVMe SSD is recommended with a few GB free
space. For database nodes the fastest and largest possible storage is
preferred.

Running a SEED client requires the same hardware as a headless node, except for GPU. For optimal performance, a recent GPU (GeForce 2070 or Radeon 5700 or
better) is recommended.

## External Dependencies

# Getting Started

The easiest way to start working within the SEED repository is to
build the latest version of the documentation for yourself. This can be done
in the following way:

+ Make sure you have the following minimum prerequisites:
    + **Python 3.7** - The latest version the better. Although the x86 version
                       should work it is recommended to install an x64 version.
                       Versions older than 3.7 will not work due to the missing
                       type hint annotations feature in earlier releases.

+ Make sure that the path to the Python executable is added to your PATH
environment variable.

+ Setup your environment the following way:
    + Open a terminal and navigate to the root of the repository.
    + (OPTIONAL) Create a Python virtual environment with the following
    command: `virtualenv .env`
    + (OPTIONAL) Activate the virtual environment with the following command:
    `source /path/to/repository/.env/bin/activate`
    + Execute the following command: `python -m suisei.sde --install`

The setup utility will make sure all of the required dependencies are
installed in your system, and it will also build the development documentation.

After it is finished, you can open the generated documentation
the following way:

  + Execute the following command in the command line:
        `sde --opendocs`

This should bring up your browser if you are in a GUI environment and open the
documentation that you've just generated.

Read the **Getting Started** section in the documentation to know how to
continue.

