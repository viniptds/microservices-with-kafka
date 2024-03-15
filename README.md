# Microservice Integration using Kafka

## Requirements

* Docker ^24
* Node ^18.14
* NPM ^9.6.0

## Installation

1. Install npm dependencies: Run `cd order-service && npm i` and `cd payment-service && npm i`
2. Start Docker container: Run `docker-compose up -d`
3. Execute Nest services: run `npm run start` on each service following the following order: order-service, payment-service

## Testing

Use some HTTP client (Postman, Insomnia, curl, etc.) and make a `POST` request to `http://localhost:3000/order` with a JSON body. For example:

```json
{
    "name": "John Doe",
    "amount": 9.90
}
```

If everything worked well, then a log message will show up in the payment-service terminal. Like this one:

`Received order:  { id: 'jrmxn5', amount: 9.90, name: 'John Doe' }`
