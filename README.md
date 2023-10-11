# Kittygram: Instagram for Cats 🐱

[![Main Kitty workflow](https://github.com/ddisson/kittygram_final/actions/workflows/main.yml/badge.svg)](https://github.com/ddisson/kittygram_final/actions/workflows/main.yml)

Kittygram is a platform dedicated to cat enthusiasts and the cats themselves. Share snapshots of your furry friends and enjoy browsing pictures from other members.

## Описание проекта

Kittygram has been designed as an Instagram exclusively for cats. This project includes an API for data management and a frontend where users can browse pictures, register, sign in, and much more.

## Deployment

Kittygram uses Docker for deployment. Below are the steps to deploy Kittygram using `docker-compose`.

### Prerequisites

1. Ensure you have Docker and `docker-compose` installed.
2. Clone the repository: git clone https://github.com/ddisson/kittygram_final.git
3. Navigate to the directory: cd kittygram_final

### Deploying

1. Create a `.env` file at the root of the project and populate it with the necessary environment variables.
2. Start the services: docker-compose up -d


## Services

### Database (`db`)

- Uses the `postgres:13.10` image.
- Data is persisted using a volume named `pg_data`.

### Backend (`backend`)

- Uses the custom image `ddisson/kitty_backend`.
- Depends on the `db` service.

### Frontend (`frontend`)

- Uses the custom image `ddisson/kitty_frontend`.

### Gateway (`gateway`)

- Uses the custom image `ddisson/kitty_gateway`.
- Exposes port `9000`.

## Environment Variables

Refer to the `.env.example` file for the necessary environment variables and their descriptions.

## Technologies Used

- Django
- Django Rest Framework
- PostgreSQL
- Docker

## Author

[ddisson](https://github.com/ddisson)

---

For inquiries, reach out via my GitHub profile or email: `ddisson@yandex.ru`.


