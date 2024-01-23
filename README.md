# Introduction

This repository contains a basic Ansible demo created for learning purposes.

# Requirements

1. Docker: 1.10.0+
2. Docker Compose: 2.0+

# Steps

1. Navigate into the project folder.

```bash
cd ansible-docker-demo
```

2. Build Docker images and start containers using Docker Compose.

```bash
docker compose up --build --detach
```

3. After successfully starting the containers, you can start a bash terminal in the running containers using the following commands.

```bash
docker exec -it ansible-controller-container bash
```

```bash
docker exec -it ansible-controller-node bash
```

4. Start a bash terminal in `ansible-controller` using the method described above. Finally, you can go to `/src` directory and run example playbook located in `src/playbooks/ping.yml`.

```bash
cd /src
export ANSIBLE_HOST_KEY_CHECKING=False && ansible-playbook -i inventory.yaml playbooks/ping.yml -v
```

# Post Processing

1. After successfully completing the demo, you can clean up created images and running container instances.

```bash
docker compose down --volumes --rmi local
```

If you prefer to keep the created images, you can remove `--rmi local`.

```bash
docker compose down --volumes
```
