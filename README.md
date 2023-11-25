
# MNIST Training Project

## Introduction
Welcome to the MNIST Training Project! This repository is dedicated to exploring and comparing different neural network architectures, including CNNs (Convolutional Neural Networks), DNNs (Deep Neural Networks), and a pre-trained ResNet model adapted using transfer learning, all using the classic MNIST dataset. The project is containerized with Docker to provide a consistent and reproducible environment for running experiments.

## Prerequisites
- Docker (GPU support required for NVIDIA GPUs)
- Git (for version control)

## Getting Started

### Clone the Repository
To begin, clone this repository to your local machine:
```bash
git clone https://github.com/chasekunz/mnist-training.git
cd mnist-training
```

### Build the Docker Image
Build the Docker image using the following command:
```bash
docker build -t mnist-training .
```
This command creates a Docker image named `mnist-training` based on the instructions in the `Dockerfile`.

### Run the Docker Container with Mounted Volumes
Run the Docker container, mounting the code and data directories:
```bash
docker run --gpus all -p 8888:8888 -v $(pwd):/usr/src/app mnist-training
```
This mounts the current directory to `/usr/src/app` in the container and forwards port 8888 for Jupyter notebook access.

## Project Structure
- `notebooks/`: Jupyter notebooks for model comparison and data exploration.
- `data/`: Directory for the MNIST dataset.
- `Dockerfile`: Defines the Docker container environment.
- `requirements.txt`: Lists dependencies for the project.

## Exploring the Notebooks
The highlight of this repository is the Jupyter notebooks found in the `notebooks/` directory. Here, you'll find detailed and beginner-friendly notebooks that walk you through the process of training and evaluating various neural network models on the MNIST dataset.

## Contributing
We encourage contributions! Please fork the repository and submit pull requests with your enhancements.

## License
This project is open-sourced under the [MIT License](LICENSE).
