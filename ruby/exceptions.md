# Ruby Exceptions

> From [exceptions rdoc](https://ruby-doc.org/3.2.2/syntax/exceptions_rdoc.html)

Ruby uses the `rescue` keyword to catch exceptions and errors when they happend. rescue receives a list of Error type to handle (by default it catches StandardError and its subclasses).

```ruby
begin
  # Code here
rescue <Error1, Error2>
  # Do something when Error1 or Error2 happen
end
```

To run a block whenever an error happens or not we use the `ensure` keyword (like `finally` keyword in multiple languages)

```ruby
begin
  # Code here
rescure Error
  # ...
ensure
  # Runs after begin or rescue
end
```

Also, there is `else` keyword for running a block explicitly when an exception does not happen

```ruby
begin
  # Code here
rescue Error
  # ...
else
  # Run if Error not raised
end
```

The `retry` keyword inside a `rescue` block, will run again the `begin` block.
```ruby
begin
  # Code here
rescue Error
  # ...
  retry # Will run again `begin`
end
```

> This could generate an infinite loop, so we need to be careful
