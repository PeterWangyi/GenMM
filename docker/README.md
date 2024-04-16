## Build Docker Environment and use with GPU Support

Before you can use this Docker environment, you need to have the following:

- Docker installed on your system
- NVIDIA drivers installed on your system
- NVIDIA Container Toolkit installed on your system


### Build and Run
1. Navigate to the GENMM root directory
   ```sh
   cd path_to_GENMM_folder
   ```
2. Build docker image:
   ```sh
   docker build -f docker/Dockerfile -t genmm:latest .
   ```
3. Start the docker container:
   ```sh
   docker run --gpus all --name genmm -it genmm:latest /bin/bash
   ```

## Troubleshooting

If you encounter any issues with the Docker environment with GPU support, please check the following:

- Make sure that you have installed the NVIDIA drivers and NVIDIA Container Toolkit on your system.
- Make sure that you have specified the --gpus all option when starting the Docker container.
- Make sure that your deep learning application is configured to use the GPU.