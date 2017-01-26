```ruby
require 'net/http'

# Get Line Item (GET )
def send_request
  uri = URI('http://localhost:3000/api/line_items/')

  # Create client
  http = Net::HTTP.new(uri.host, uri.port)

  # Create Request
  req =  Net::HTTP::Get.new(uri)
  # Add headers
  req.add_field "Authorization", "auth-key=S@mpl3!"
  # Add headers
  req.add_field "Accept", "application/vnd.api+json; version=1"

  # Fetch Request
  res = http.request(req)
  puts "Response HTTP Status Code: #{res.code}"
  puts "Response HTTP Response Body: #{res.body}"
rescue StandardError => e
  puts "HTTP Request failed (#{e.message})"
end
```
