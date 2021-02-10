```elixir [0|12-18]
defmodule SuperComputer.Plan do

  def heist_plan(target_name) do
    ...
    target_profile =
     [insert important logic here]

      identity_thief().steal_identity(target_profile)    
    ...
  end

  defp identity_thief() do
    Application.get_env(
      :super_computer,
      :identity_thief
    )
  end
end
```
NOTE:
- do not use run-time switching