/test/support/doubles.ex
```elixir
Mox.defmock(SuperComputer.IndentityThiefDouble,
  for: SuperComputer.IndentityThiefBehaviour)
```
NOTE:
- skip adding the calls to define mocks to your test_helper.ex and go with the more explicit and compilte