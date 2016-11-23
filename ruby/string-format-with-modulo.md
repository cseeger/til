# String formatting with `%`

Ruby let's you format (or even substitute) string values with String#%. Passing
in args has to be the coolest feature.

```ruby
> "this is a %{string}" % {string: 'test'}
"this is a test"
> "this is a %{string}"
"this is a %{string}"
> "this is a %{string}" % {string: nil}
"this is a "
```

[source](http://ruby-doc.org/core-2.2.0/String.html#method-i-25)
