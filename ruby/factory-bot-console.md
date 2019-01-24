# Use `FactoryBot` in the console

I often find debugging easier with my spec factories. 

```ruby
require 'factory_bot'
FactoryBot.find_definitions
user = FactoryBot.create(:user)
```
