# dotenv

Reads `.env` files into a table.

```lus nocheck
local dotenv = require("https://atmosp.here/2.0/dotenv.lus")

local env = dotenv.parse("PORT=8080\nURL=http://localhost:${PORT}\n")
print(env.URL)   --> http://localhost:8080
```

The package requires Lus 2.0. It declares the permissions fs:read and env:read in its header. It calls no `pledge` of its own, so the program that loads it keeps control of its permissions.

The reference is in the doc comments of `dotenv.lus`. Run `lus doc dotenv.lus` to print it.
