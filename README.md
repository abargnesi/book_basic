# Ruby introduction

## Sending a message

Ruby objects are mutable. Objects can respond to messages (e.g. methods), in a dynamic fashion, and you can change this at run-time.

```ruby
my_obj = Object.new
# can I respond to the foo message?
my_obj.respond_to?(:foo)
# => false

# add foo message handler to my_obj
class << my_obj

  def foo
    :foo
  end
end

# how about now?
my_obj.respond_to?(:foo)
# => true


# send the foo message to my_obj
my_obj.send(:foo)
# => :foo

# send the foo message using dot notation
my_obj.foo
# => :foo
```
