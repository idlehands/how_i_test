/mix.exs
```elixir
def project do
  [
    ...
    elixirc_paths: elixirc_paths(Mix.env),
    ...
  ]
end

defp elixirc_paths(:test),
  do: ["test/support", "lib"]
  
defp elixirc_paths(_),
  do: ["lib"]
```
NOTE:
- you'll need to make sure the file is in your compile paths