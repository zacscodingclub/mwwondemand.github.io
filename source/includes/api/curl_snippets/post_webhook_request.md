```shell
curl -i -X POST https://api.mwwondemand.com/api/webhooks \
  -d '{
    "data": {
      "type": "webhooks",
      "attributes": {
        "url": "https://your-server.com/order-notifications"
      }
    }
  }' \
  -H "Content-Type: application/vnd.api+json" \
  -H "Accept: application/vnd.api+json; version=2" \
  -H "Authorization: YOUR_API_KEY"
```