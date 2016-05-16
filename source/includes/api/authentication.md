# Authentication

> To authorize, use this code:

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: YOUR_API_KEY"
```

> Make sure to replace `YOUR_API_KEY` with your API key.

Access to the API uses an API key for authentication. You can register a new API key at our [developer portal](https://example.com/developers).

The API expects an API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: <YOUR_API_KEY>`

<aside class="notice">
You must replace <code>&lt;YOUR_API_KEY&gt;</code> with your personal API key.
</aside>