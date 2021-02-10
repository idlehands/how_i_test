use custom messages to be super explicit
```elixir
assert DateTime.compare(existing_record.updated_at, returned.updated_at) == :lt,
        "value for :updated_at should be more recent than original value"
```

NOTE:
- super important when you are iterating
- or in helpers
- or it you're asserting that something is true