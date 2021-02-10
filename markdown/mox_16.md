testing async
```elixir [0|5|10|13-15|]
setup :set_mox_global

test "success: does an async thing" do
  ...
  test_pid = self()

  stub(AsyncModule,
    :async_function,
    fn param ->
      send(test_pid, {:async_function_called, param})
    end)
  ...
  assert_received(
    {:async_function_called, ^expected_param}
    ) 
end
```
NOTE:
- pid must be outside of closure
- let the test do the assertions, not the mock
- assert recieved
- can pass a ref instead of an atom if you want
