```python
# Install the Python Requests library:
# `pip install requests`

import requests


def send_request():
    # Patch Webhook
    # PATCH http://localhost:3000/api/webhooks/

    try:
        response = requests.patch(
            url="http://localhost:3000/api/webhooks/",
            headers={
                "Content-Type": "application/vnd.api+json",
                "Authorization": "Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjo2NDgzODcyODM1Njg4MjE1MjYsImV4cCI6MTQ4MDUxNzcyOX0.SijY04z68CwqQ6AV2N3cWSng6fQAl06zodWicym_uuY",
                "Accept": "application/vnd.api+json; version=1",
            },
            data="{
  \"data\": {
    \"id\": \"\",
    \"type\": \"webhooks\",
    \"attributes\": {
      \"url\": \"http://localhost:3001/mwwondemand-order-notifications\",
      \"printed\": true,
      \"pressed\": true,
      \"cut\": true,
      \"sewn\": true,
      \"turned\": true,
      \"packed\": true
    }
  }
}"
        )
        print('Response HTTP Status Code: {status_code}'.format(
            status_code=response.status_code))
        print('Response HTTP Response Body: {content}'.format(
            content=response.content))
    except requests.exceptions.RequestException:
        print('HTTP Request failed')
```
