iterate!
```elixir [0|1|2|3|]
for user_state <- [:new, :closed] do
  test "error: returns 409 when state is invalid (:#{user_state})", %{conn: conn} do
    user_state = unquote(user_state)
    {:ok, user} = Factory.insert_user(state: user_state)
    {:ok, token, _} = Support.Helpers.encode_and_sign(%{user: user})
    conn_with_token = put_req_header(conn, "authorization", "Bearer " <> token)

    response =
      conn_with_token
      |> put(block_path(conn, :cancel, user.id))
      |> json_response(409)

    assert response["errors"] == [%{"detail" => "Failed to transition from #{user_state} on cancel"}]
  end
end
```

NOTE: