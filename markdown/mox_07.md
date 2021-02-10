```elixir [0|3|11-17|11|12|13-17|19|6]
defmodule SuperComputer.PlanTest do
  use SuperComputer.DataCase
  import Mox
  alias SuperComputer.{IndentityThiefDouble, PlanTest}

  setup :verify_on_exit!

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
- you'll need to make sure the file is in your compile paths