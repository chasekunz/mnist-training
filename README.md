
# MNIST Training Project

## Introduction
This repository contains a machine learning project for training a Convolutional Neural Network (CNN) on the MNIST dataset using PyTorch. The project is containerized using Docker, which provides the necessary environment but does not include the code or data. These will be mounted into the Docker container when running it.

## Prerequisites
- Docker (with GPU support if using an NVIDIA GPU)
- Git (for version control)

## Getting Started

### Clone the Repository
First, clone this repository to your local machine using Git:
```bash
git clone https://github.com/your-username/mnist-training.git
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
This command mounts your current directory (`$(pwd)`) to `/usr/src/app` in the container, allowing the container to access and run your code, and use your data. It also forwards port 8888 from the container to port 8888 on your local machine, allowing you to access the Jupyter notebook server running in the container.

## Project Structure
- `src/`: Contains the Python scripts for training the model.
- `models/`: Contains the CNN model architecture.
- `notebooks/`: Jupyter notebooks for data exploration.
- `data/`: Data directory for MNIST dataset.
- `tests/`: Unit and integration tests for the project.
- `Dockerfile`: Dockerfile for setting up the container environment.
- `requirements.txt`: Python dependencies for the project.

## Contributing
Contributions to this project are welcome! Please fork the repository and submit a pull request with your changes.

## License
This project is licensed under the [MIT License](LICENSE).
