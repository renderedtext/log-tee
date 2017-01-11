# LogTee

Library repozitory.

Provides logging functions sutable for pipelining:

```
[1, 2, 3]
|> LogTee.debug("list content")
|> Enum.sum
|> LogTee.debug("sum")
```
