# Changelog

## 1.0.0

**Release date:** TBD

Version 1.0.0 is the first release of `dotenv`.

- Added the `dotenv` package.
  - `dotenv.parse`: Parses the text of a `.env` file into a table from names to values.
  - `dotenv.load`: Reads a `.env` file, keeps its values, and can set them as environment variables.
  - `dotenv.get`: Returns a loaded value or the environment variable of a name.
  - `dotenv.reset`: Clears every loaded value.
