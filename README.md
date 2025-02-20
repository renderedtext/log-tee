# LogTee

Library repository.

Provides logging functions suitable for pipelining:

## Installation

Add log_tee to your list of dependencies in `mix.exs`:

```elixir
def deps do
  [
    {:log_tee, github: "renderedtext/log-tee"}
  ]
end
```

## Usage

You can use the `LogTee` module to log messages at different severity levels while processing data in a pipeline.

### Example

```
[1, 2, 3]
|> LogTee.debug("list content")
|> Enum.sum
|> LogTee.debug("sum")
```

This will log the content of the list and the sum of the list elements.

### Available Functions

- `LogTee.debug(item, tag)`
- `LogTee.info(item, tag)`
- `LogTee.warn(item, tag)`
- `LogTee.error(item, tag)`

Each function logs the `item` with the specified `tag` at the corresponding severity level and returns the `item`.

## License

This software is licensed under [the Apache 2.0 license](LICENSE).