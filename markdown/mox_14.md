stub'n'flunk
```elixir [0|3|4]
  stub(SafeDouble,
    :model_number,
    fn _safe_location ->
      flunk(":model_number shouldn't have been called")
    end)
```
NOTE:
- you can add an additional param for the number of times, but 0 didn't use to be a valid number
- more explicit