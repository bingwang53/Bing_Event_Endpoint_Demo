# Bing Event Endpoint Demo (Kafka + IWHI EEM)

This folder contains starter assets for demonstrating Event Endpoint Management with Kafka.

## Topics

- `orders.created`
- `orders.status.updated`
- `orders.fulfillment.requested`

## Files

- `schemas/orders.created.avsc`
- `schemas/orders.status.updated.avsc`
- `schemas/orders.fulfillment.requested.avsc`
- `samples/orders.created.json`
- `samples/orders.status.updated.json`
- `samples/orders.fulfillment.requested.json`
- `commands/kcat-producer-examples.txt`
- `commands/kcat-consumer-examples.txt`
- `commands/kafka-console-examples.txt`
- `DEMO_FLOW_EVENT_ENDPOINTS.md`

## Quick Demo

1. Register Kafka cluster in IWHI EEM
2. Add event endpoints for above topics
3. Attach schemas and metadata
4. Produce `orders.created` event
5. Consume from subscriber and show event received
6. Produce `orders.status.updated` and show lifecycle
