# Use `FactoryGirl` in the console

I often find debugging easier with my spec factories. 

```ruby
require 'factory_girl'
FactoryGirl.find_definitions
user = FactoryGirl.create(:user)
```
