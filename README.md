# OpenProject Deploy

Recipes and examples for deploying OpenProject using Docker, Docker Compose, Kubernetes, etc.

## Docker Compose

### Install

Clone this repository:

    git clone https://github.com/opf/openproject-deploy --depth=1 --branch=stable/11 openproject

Go to the folder that was just created:

    cd openproject

Launch the containers:

    docker-compose up -d

After a while, OpenProject should be up and running on <http://localhost:8080>.

### Configuration

If you want to specify a different port, you can do so with:

    PORT=4000 docker-compose up -d

If you want to specify a custom tag for the OpenProject docker image, you can do so with:

    TAG=my-docker-tag docker-compose up -d

You can also set those variables into an `.env` file at the root of the
directory, and Docker Compose will pick it up automatically. See `.env.example`
for details.

### Uninstall

You can remove the stack with:

    docker-compose down

### Troubleshooting

You can look at the logs with:

    docker-compose logs -n 1000

For the complete documentation, please refer to https://docs.openproject.org/installation-and-operations/.
