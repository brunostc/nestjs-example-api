# NestJS Example API

This is a NestJS v10 application that uses Docker and Docker Compose to spin up containers for MySQL and Node.js. It is a sample API used for study purposes.


## Getting Started

### Prerequisites

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

### Installation

1. **Clone the repository**

```
git clone https://github.com/brunostc/nestjs-example-api.git
cd nestjs-example-api
```

2. **Start the containers**

```
docker-compose up -d --build
```

This will spin up two containers:
- `mysql`: Runs MySQL database.
- `app`: Runs the NestJS application.

### Accessing the Application

The NestJS application will be available at `http://localhost:3000`.

### Environment Variables

The application uses the following environment variables for database configuration:

- `DATABASE_HOST`: Hostname of the database (default: `mysql`).
- `DATABASE_PORT`: Port number of the database (default: `3306`).
- `DATABASE_USER`: Username for the database (default: `user`).
- `DATABASE_PASSWORD`: Password for the database (default: `secret`).
- `DATABASE_NAME`: Name of the database (default: `nest_example_api`).

These variables are defined in the `docker-compose.yml` file.

### Stopping the Containers

To stop the running containers, use:

```
docker-compose down
```

### Installing New Dependencies

1. Install the dependency locally:

```
npm install <dependency-name>
```

2. Rebuild the Docker container:

```
docker-compose up -d --build
```

## Repository

The repository for this project can be found at [GitHub](https://github.com/brunostc/nestjs-example-api).

## License

This project is licensed under the MIT License.
