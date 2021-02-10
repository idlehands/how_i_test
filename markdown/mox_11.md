stub
```elixir [0|1]
  stub(SafeDouble,
    :model_number,
    fn _safe_location ->
      Factory.Safe.model_number()
    end)
```
NOTE: