# UPS Tracking Webhook with Track123

Receive UPS shipment tracking updates in your application through Track123 webhooks.

> This guide uses Track123's unified webhook flow. It is not official UPS webhook documentation.

## Set up UPS tracking updates

1. Register the shipment with Track123.

2. Set `courierCode` to `ups` when UPS is already known.

2. Use [Carrier Detection](https://docs.track123.com/reference/detection-courier) when the carrier code is not available.

3. Add an HTTPS webhook URL in Track123.
4. Select the tracking events your application needs.
5. Verify the webhook signature before processing the event.
6. Handle repeated deliveries safely with idempotent processing.

## Webhook security and retries

Validate every received event according to the Track123 webhook guide. Keep your webhook endpoint private, log delivery failures safely, and return a successful response only after your application accepts the event.

## Resources

- [Track123 webhook guide](https://docs.track123.com/reference/getting-started-with-your-api)
- [Track123 delivery status reference](https://docs.track123.com/reference/package-status)
- [Track UPS packages on Track123](https://www.track123.com/carriers/ups)
- [Back to UPS tracking API](README.md)
