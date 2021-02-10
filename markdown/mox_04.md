/test/support/doubles.ex
```elixir
Mox.defmock(SuperComputer.IndentityThiefDouble,
  for:
    [
      SuperComputer.IndentityThiefBehaviour,
      SuperComputer.SecondBehaviour
    ]  
  )
```
NOTE:
- if you need your double to stand in for more than one thing, pass a list
- ask yourself why you did this