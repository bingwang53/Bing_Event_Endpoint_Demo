# Event Streams Connection Checklist (IWHI EEM)

Use this checklist to connect IBM Event Streams to IWHI Event Endpoint Management.

## 1. Event Streams Setup (IBM Cloud)

- [ ] Event Streams instance created
- [ ] Topics created:
  - [ ] `orders.created`
  - [ ] `orders.status.updated`
  - [ ] `orders.fulfillment.requested`
- [ ] Service credentials created

## 2. Collect Connection Values

Fill these from Event Streams credentials/UI:

- Bootstrap servers: `<BOOTSTRAP_SERVERS>`
- Port: `<PORT>` (usually 9093)
- Security protocol: `SASL_SSL`
- SASL mechanism: `PLAIN`
- Username: `token`
- Password/API key: `<API_KEY_OR_PASSWORD>`
- CA certificate needed?: `<YES/NO>`

## 3. IWHI EEM Connection Form

In IWHI Event Endpoint Management, create Kafka connection with:

- Name: `event-streams-demo`
- Broker/Bootstrap: `<BOOTSTRAP_SERVERS>`
- Port: `<PORT>`
- TLS/SSL: enabled
- Authentication: SASL/PLAIN
- Username: `token`
- Password: `<API_KEY_OR_PASSWORD>`

Then click:

- [ ] Test connection
- [ ] Save

## 4. Register Endpoints

- [ ] Add/discover topic `orders.created`
- [ ] Add/discover topic `orders.status.updated`
- [ ] Add/discover topic `orders.fulfillment.requested`

## 5. Attach Schemas

Use files from:

`C:\Users\BingWang\Bing_Event_Endpoint_Demo\schemas`

- [ ] `orders.created.avsc`
- [ ] `orders.status.updated.avsc`
- [ ] `orders.fulfillment.requested.avsc`

## 6. Publish/Subscribe Test

- [ ] Produce sample event to `orders.created`
- [ ] Consume from subscriber app
- [ ] Confirm message appears in logs/consumer output
- [ ] Confirm endpoint metrics/visibility in EEM

## 7. Troubleshooting Quick Checks

If connection fails:

1. Verify bootstrap server + port
2. Verify SASL settings (`SASL_SSL` + `PLAIN`)
3. Regenerate service credentials and retry
4. Ensure firewall/proxy allows outbound to Event Streams

If publish/consume fails:

1. Verify topic names exactly match
2. Check ACL/authorization for client
3. Confirm schema compatibility if validation is enabled

## 8. Copy-Paste Template

```
Bootstrap servers: 
Port: 
Security protocol: SASL_SSL
SASL mechanism: PLAIN
Username: token
Password/API key: 
Topics: orders.created, orders.status.updated, orders.fulfillment.requested
```
