```elixir [0|2-5|12-13]
defmodule SuperComputer.Plan do
  @identity_thief Application.get_env(
    :super_computer,
    :identity_thief
  )

  def heist_plan(target_name) do
    ...
    target_profile =
     [insert important logic here]

    stolen_profile =
      @identity_thief.steal_identity(target_profile)    
    ...
  end
end
```
NOTE:
- do not use run-time switching
- plays well with xref