```shell
curl -X "POST" "https://api.mwwondemand.com:443/api/orders" \
  -H "Accept: application/vnd.api+json; version=1" \
  -H "Authorization: auth-key=YOU_API_KEY" \
  -H "Content-Type: application/vnd.api+json" \
  -d $'{
  "data": {
    "type": "orders",
    "attributes": {
      "vendor-po": "dcbfdc59b8b51bbb530f0299b6db25c7",
      "shipping-method": "SAMPLE",
      "shipping-name": "Phillip J. Fry",
      "shipping-address": "123 Green St.\\nSuite 321",
      "shipping-city": "New New York",
      "shipping-state": "NY",
      "shipping-postal-code": "10012",
      "billing-name": "Hubert J. Farnsworth"
    }
  },
  "included": [
    {
      "type": "line-items",
      "attributes": {
        "line-number": 1,
        "quantity": 2,
        "description": "It's not sò fluffy!",
        "product-code": "293",
        "po": 312,
        "item-properties": {
          "thread-color": "red",
          "blah": "blah-2"
        },
        "designs": [
          {
            "image_remote_url": "http://images.apple.com/v/home/cj/images/promos/ipad_pro_large.jpg",
            "position": "centered",
            "crop": "left"
          }
        ]
      }
    },
    {
      "type": "line-items",
      "attributes": {
        "line-number": 2,
        "quantity": 5,
        "description": "It's sò fluffy!",
        "product-code": "294",
        "po": 312,
        "item-properties": {
          "thread-color": "red",
          "blah": "blah-2"
        },
        "designs": [
          {
            "image_remote_url": "http://images.apple.com/v/home/cj/images/heros/iphone-6s-change_xlarge.jpg"
          }
        ]
      }
    }
  ]
}'
```
