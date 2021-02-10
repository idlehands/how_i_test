set_mox_from_context
```elixir [0|6]
defmodule SuperComputer.PlanControllerTest do
  use SuperComputer.ConnCase
  import Mox
  alias SuperComputer.{IndentityThiefDouble, PlanTest}

  setup [:set_mox_from_context, :verify_on_exit!]

  test "success: retrieves " do
    expected_name = Factory.profile_name()

    expect(IndentityThiefDouble,
      :steal_identity,
      fn target_profile ->
        assert target_profile.name == expected_name
        assert target_profile.age > 18
        Factory.profile()
      end)

    assert ... = PlanTest.heist_plan(expected_name)
  end
end
```
NOTE:
- When async: true is used the mode is :private, otherwise :global is chosen.