
```json
  {
    "data": {
      "id": "480226771879331308",
      "type": "orders",
      "links": {
        "self": "https://api.mwwondemand.com/api/orders/480226771879331308"
      },
      "attributes": {
        "created-at": "2016-03-08T14:05:15.978Z",
        "updated-at": "2016-03-08T14:05:15.978Z",
        "state":"received",
        "state-events": [ "invalidate_it", "process_it", "cancel_it"],
        "bill-name": "Phillip J. Fry",
        "bill-address1": "123 Green St.",
        "bill-address2": "Suite 321",
        "bill-city": "New New York",
        "bill-state": "CA",
        "bill-country": null,
        "bill-zip": "10012",
        "bill-phone":null,
        "bill-email":null,
        "ship-name":null,
        "ship-address1": null,
        "ship-address2": null,
        "ship-city": null,
        "ship-state": null,
        "ship-zip": null,
        "ship-country": null,
        "ship-phone": null, "ship-email": null,
        "shipping-method": "321",
        "po": "123"
      },
      "relationships": {
        "line-items": {
          "links": {
            "self": "https://api.mwwondemand.com/api/orders/480226771879331308/relationships/line-items",
            "related":"https://api.mwwondemand.com/api/orders/480226771879331308/line-items"
          }
        },
        "user": {
          "links": {
            "self": "https://api.mwwondemand.com/api/orders/480226771879331308/relationships/user",
            "related":"https://api.mwwondemand.com/api/orders/480226771879331308/user"
          }
        }
      }
    },
    "meta": {
      "warnings":[
        {
          "title": "Param not allowed",
          "detail": "vendor-order-id is not allowed.",
          "code": 105
        },
        {
          "title": "Param not allowed",
          "detail": "line-items-attributes is not allowed.",
          "code": 105
        }
      ]
    }
  }
```