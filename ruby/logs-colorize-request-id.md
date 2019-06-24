# Crude colorized `:request_id` in logs 

In your `development.rb` file:

```ruby
  BG_COLORS = [41, 42, 43, 44, 45].freeze
  BG_INDEX = -1
  
  config.log_tags = [lambda do |request|
    if BG_INDEX == (BG_COLORS.length - 1)
      BG_INDEX = -1
    end
    BG_INDEX = BG_INDEX + 1
    "\e[#{BG_COLORS[BG_INDEX]}m#{request.request_id}\e[0m"
  end]
```
