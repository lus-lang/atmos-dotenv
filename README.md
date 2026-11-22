# dotenv

`dotenv` reads `.env` files into a table, so a program can keep settings such as ports, URLs, and keys out of its source.

The following example reads a configuration whose URL refers to the port defined before it.

```lus nocheck
local dotenv = require("https://atmosp.here/2.0/dotenv.lus")

local env = dotenv.parse("PORT=8080\nURL=http://localhost:${PORT}\n")
print(env.URL)   --> http://localhost:8080
```

The package requires Lus 2.0 and declares the permissions `fs:read`, `env:read`, and `env:write`, which it uses to read `.env` files and to read and set environment variables. It never calls `pledge`, so the program that loads it keeps control of its permissions.

The reference is in the doc comments of `dotenv.lus`, which `lus doc dotenv.lus` prints.
