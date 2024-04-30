# URL Shortener Service

This is a URL shortener service developed in TypeScript and Nest.js, utilizing Redis for caching, Docker for containerization, and Jest for testing.

[![JavaScript](https://skillicons.dev/icons?i=typescript,nodejs,redis,nestjs,git,docker,jest)](https://skillicons.dev)
## Overview

This service allows users to shorten long URLs into concise, easy-to-share links. It provides a RESTful API for shortening URLs and redirecting users to the original long URLs.

## Videos
- [Complete feature working](https://drive.google.com/file/d/12leK7WIccR2kyukd4cHF4VNbn_vvRsGI/view?usp=sharing)
  
## Features

- Shorten URLs: Convert long URLs into short, manageable links.
- Redirect: Redirect users from short links to the original long URLs.
- Cache: Utilize Redis for caching to improve performance and reduce database load.
- Docker: Containerize the application for easy deployment and scalability.
- Testing: Implement unit and integration tests using Jest for ensuring code quality and reliability.

## Installation

To run this service locally, follow these steps:

1. Clone the repository:

```bash
git clone https://github.com/devmaiko/url-shortener.git
```

2. Install dependencies:

```bash
cd url-shortener
npm install
```

3. Start the server:

```bash
yarn start:dev
```

The service should now be running locally on `http://localhost:3000`.

## Usage

To use the URL shortener service, follow these steps:

1. Shorten a URL:

```bash
POST /shorten

Should sent as x-www-form-urlencoded
 
{
  "url": "https://example.com/very-long-url-with-many-characters"
}
```

2. Receive a shortened URL in the response:

    You should access be you server endpoint e.g: localhost:3000/lpa0wo

```json
{
  "hash": "lpa0wo"
}
```


3. Access the shortened URL to be redirected to the original long URL.

## API Endpoints

- `POST /shorten`: Shorten a URL.
- `GET /:shortCode`: Redirect to the original long URL associated with the given short code.

## Technologies Used

- [Nest.js](https://nestjs.com/): A progressive Node.js framework for building efficient, reliable, and scalable server-side applications.
- [Redis](https://redis.io/): An open-source, in-memory data structure store, used for caching.
- [Docker](https://www.docker.com/): Containerization platform for packaging, distributing, and running applications.
- [Jest](https://jestjs.io/): A delightful JavaScript testing framework with a focus on simplicity.
- [TypeScript](https://www.typescriptlang.org/): A typed superset of JavaScript that compiles to plain JavaScript.

## Testing

To run the tests, execute:

```bash
yarn test
```

## Deployment

This service can be easily deployed using Docker. Simply build the Docker image and run it in your desired environment.

```bash
docker compose up -d
```
