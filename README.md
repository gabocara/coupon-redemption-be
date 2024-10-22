# coupon-redemption-be

Backend for coupon redemption.

## Initialization

git clone <repo-url>
npm install
npm run dev

## Improvement Proposal
A Redis cache service can be implemented to retrieve coupons more efficiently. The strategy would be to invalidate the cache per user when a new coupon is created.
RabbitMQ was used to send the creation of new coupons to a queue, allowing the process to be asynchronous and avoiding concurrency issues.
The implementation of the queue consumption process is missing, which would be the next step in improving the system.

## Scalability and Concurrency
RabbitMQ was added to handle coupon creation asynchronously, improving scalability and performance.
MongoDB transactions were used to lock coupons and prevent multiple consumptions of the same resource.
MongoDB replicas were configured to distribute the load and improve the system’s scalability.

## Postman Colections
This version improves clarity and flow, making it easy to understand the purpose of the Postman collection.
