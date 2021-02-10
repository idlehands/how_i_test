```elixir [0|2]
defmodule SuperComputer.IndentityThief do
  @callback SuperComputer.IndentityThiefBehaviour
  
  @spec steal_identity(map()) :: map()
  def steal_identity(target_profile) do
    ...stolen_identity
  end
end
```
NOTE:
- If the behaviour is ONLY for testing, there are worse things than lumping those callbacks into the original module and it makes it easier for a later developer to see what you were doing.

- there IS 1 hefty caveat, but we will hit on that later
