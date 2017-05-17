# ActiveRecord and `DATABASE_URL` 

Today we discovered that ActiveRecord prefers the ENV var `DATABASE_URL` over the settings outlined in our Rails 5.0.1 `db/database.yml` file. 

This was not expected. 😐

Here's the offending code, buried in `connection_handling.rb` of ActiveRecord v5.0.2:

```ruby
def config
  @raw_config.dup.tap do |cfg|
    if url = ENV['DATABASE_URL']
      cfg[@env] ||= {}
      cfg[@env]["url"] ||= url
    end
  end
end
```

