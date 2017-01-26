```python
# Install the Python Requests library:
# `pip install requests`

import requests


def send_request():
    # Get All Orders
    # GET http://localhost:3000/api/orders

    try:
        response = requests.get(
            url="http://localhost:3000/api/orders",
            headers={
                "Accept": "application/vnd.api+json; version=1",
                "Authorization": "auth-key=S@mpl3!",
                "Content-Type": "application/vnd.api+json",
            },
        )
        print('Response HTTP Status Code: {status_code}'.format(
            status_code=response.status_code))
        print('Response HTTP Response Body: {content}'.format(
            content=response.content))
    except requests.exceptions.RequestException:
        print('HTTP Request failed')
```
