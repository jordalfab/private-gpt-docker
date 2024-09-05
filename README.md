# private-gpt-docker
private-gpt-docker is a Dockerfile designed to create a private-gpt image. When the image is executed, the container allows access to the private-gpt web interface from the host system.
The Dockerfile is based on Dockerfile.ollama from https://github.com/zylon-ai/private-gpt.git repository.

### Prerequisites
- Docker installed on your system.
- Basic knowledge of Docker commands.

### Installation
Clone private-gpt repository:
```bash
git clone https://github.com/zylon-ai/private-gpt.git
```
copy the Dockerfile in the private-gpt directory.
Build the Docker Image:
```bash
docker build -t private-gpt .
```
Run the Docker Container:
```bash
docker run --name privategpt-container -e PGPT_PROFILES=ollama -p 8080:8080 private-gpt
```
