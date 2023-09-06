
# Use a base image
FROM ubuntu:22.04

# Set non-interactive mode for apt-get
ENV DEBIAN_FRONTEND=noninteractive

# Update the system and install the necessary dependencies
RUN apt-get update && apt-get upgrade -y && apt-get install -y     python3     python3-numpy     python3-matplotlib     python3-pandas     python3-sklearn     python3-pip     git     build-essential     autoconf     libgsl-dev     libhdf5-dev     libmpich-dev

# Install h5py using pip
RUN python3 -m pip install h5py

# Clone the repository (this can be commented out if the repo is already available in the Codespace)
# RUN git clone https://github.com/ASSISTLaboratory/WVU_RSM_Suite.git

# Setting up the working directory
WORKDIR /workspace

# Setting the user to vscode to ensure that the Codespace user can access and modify files
USER vscode

# Entrypoint
CMD [ "/bin/bash" ]
