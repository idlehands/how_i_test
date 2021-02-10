assert on all the values
```elixir [0|2|3|4]
assert_values_for(
  expected: {expected_params, :string_keys},
  actual: {media_from_db, :atom_keys},
  fields: fields_for(Media) -- [:id, :inserted_at, :updated_at]
)
```

NOTE:
- is dynamic
- fields_for
- anything skipped should be tested below