# DEMO_FLOW_EVENT_ENDPOINTS.md

## Objective

Demonstrate IWHI Event Endpoint Management governance for Kafka topics used by ProductOrder.

## Steps

1. Register Kafka cluster in IWHI EEM
2. Add/manage endpoints:
   - orders.created
   - orders.status.updated
   - orders.fulfillment.requested
3. Attach schemas from `schemas/`
4. Add metadata: owner, environment, lifecycle state
5. Produce sample events from `samples/`
6. Consume and verify events
7. Show endpoint discoverability and access controls in EEM

## Value Talking Points

- API-like governance for events
- Discoverable and reusable event contracts
- Better control over producer/consumer onboarding
- Version and lifecycle visibility across event endpoints
