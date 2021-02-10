```elixir[0|1-3|6]
defmodule SuperComputer.IndentityThiefBehaviour do
  @callback steal_identity(map()) :: map()
end

defmodule SuperComputer.IndentityThief do
  @behaviour SuperComputer.IndentityThiefBehaviour
  
  @spec steal_identity(map()) :: map()
  def steal_identity(target_profile) do
    ...stolen_identity
  end
end
```
NOTE:
- we need define a behaviour for the functions that will be needed for the double
