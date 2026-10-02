# scholarfeed

scholarfeed

## Checks

Run these before opening a PR. CI runs the same ones.

```sh
uv run ruff format && uv run ruff check && uv run pytest && uv audit --preview-features audit-command
npx @stoplight/spectral-cli lint openapi.yaml
sqlite3 -bail :memory: ".read sqlite/schema.sql"   # the app opens ${APP_DATA:-.}/app.db
```

`main` is protected: open a PR; the `ci` check must pass before merging (squash only).
