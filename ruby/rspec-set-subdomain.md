# Set a request subdomain for Rspec

When testing subdomain specific logic, you'll need to set
the subdomain via `request.host`.

```ruby
request.host = "some-subdomain." + request.host
```
