- cheat with the behaviour callbacks (breaks stub_with)
- skip the test_helper (add the new file path to mix.exs)
- don't pin in your function heads, assert on the values
- keep stubs dumb
- use compile time module selection when you can
- pass-through or stub_with for integration tests
- use stub + flunk to assert a call did not happen
- set_mox_from_context is a lovely default
- one of the ways to test async
NOTE:
