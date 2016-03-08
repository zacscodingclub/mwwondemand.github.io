
# Orders

## Submit Order

```shell
curl http://localhost:3000/api/orders \
  -d '{
    "data": {
      "type": "orders",
      "attributes": {
        "vendor-order-id": "cds-0001",
        "line-items-attributes": [
          {
            "line-number": 1,
            "quantity": 2,
            "description": "Warm Blanket!",
            "product-code": "295",
            "item-properties": {
              "thread-color": "red",
              "blah": "blah-2"
            },
            "path_to_image": "http://images.apple.com/v/home/cj/images/promos/ipad_pro_large.jpg"
          },
          {
            "line-number": 2,
            "quantity": 5,
            "description": "Super Soft Pillow!",
            "product-code": "1029",
            "item-properties": {
              "thread-color": "red",
              "blah": "blah-2"
            },
            "path_to_image": "http://images.apple.com/v/home/cj/images/heros/iphone-6s-change_xlarge.jpg"
          }
        ],
        "po": "123",
        "shipping-method": "321",
        "bill-name": "Phillip J. Fry",
        "bill-address1": "123 Green St.",
        "bill-address2": "Suite 321",
        "bill-city": "New New York",
        "bill-state": "CA",
        "bill-zip": "10012"
      }
    }
  }' \
  -X POST \
  -H "Content-Type: application/vnd.api+json" \
  -H "Accept: application/vnd.api+json; version=2" \
  -H "api-key: YOUR_API_KEY"
```

## Get All Orders


```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get()
```

```shell
curl "http://example.com/api/kittens"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all kittens.

### HTTP Request

`GET http://example.com/api/kittens`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

