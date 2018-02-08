# Class Instance Variable

```ruby
class Timer
  @current_time = Time.new

  class << self
    attr_accessor :current_time
  end

  attr_accessor :time

  def initialize
    @time = Timer.current_time
  end
end
```

```ruby
puts "time: #{Time.now}"
sleep 4

t_1 = Timer.new
puts t_1.time

sleep 4

t_2 = Timer.new
puts t_2.time
```
