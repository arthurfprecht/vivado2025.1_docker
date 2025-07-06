# Vivado 2025.1 Docker image

This repository contains a Xilinx Unified SDI 2025.1 docker image based on Ubuntu 24.04.
It is based on Thierry Delafontaine's (delafthi) repo, original credits to him.

## Usage

1. Download the [`Xilinx Unified Installer 2025.1: Linux Self Extracting Web Instaler`](https://www.xilinx.com/support/download/index.html/content/xilinx/en/downloadNav/vivado-design-tools.html)
   and place into the directory.
2. Adapt `install_config.txt` to your likings, or regenerate
   `install_config.txt` by running
   `./FPGAs_AdaptiveSoCs_Unified_SDI_2025.1_0530_0145_Lin64.bin -- --batch ConfigGen` and
   copying the generated file into the directory.
3. Build the docker image by running `./build.sh`.
4. At the beginning of the `./build.sh` script you need to log in with your
   Xilinx credentials in order to create a authenication token for the web
   installer.
5. Adjust the `PROJECT_PATH` variable in `run.sh` to mount your project folder
   and run the docker image with `./run.sh`.
6. Start Vivado from the docker terminal with `vivado`.
