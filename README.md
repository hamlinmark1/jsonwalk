# Treverse JSON using JSONPath queries.

## Examples

```bash
# Get list off all Pikachu's move from internet and sort alphabetically
curl "https://pokeapi.co/api/v2/pokemon/25/" 2>/dev/null | jsonwalk '$..move.name' | sort
# Get list of books from json stored locally
cat src/test/sample.json | java -jar target/jsonwalk-1.0.0-SNAPSHOT.jar   "$..book"
```


# Development

To build the native image install graalvm and ensure its configured properly for your project toolchain.

## Build and Execute

```bash
# Build
mvn jar:jar
# Get list off all Pikachu's move from internet and sort alphabetically
curl "https://pokeapi.co/api/v2/pokemon/25/" 2>/dev/null | java -jar target/jsonwalk-1.0.0-SNAPSHOT.jar '$..move.name' | sort
# Get list of books from json stored locally
cat src/test/sample.json | java -jar target/jsonwalk-1.0.0-SNAPSHOT.jar   "$..book"
```

## Libraries

[JsonPath](https://github.com/json-path/JsonPath)
[Picocli](https://picocli.info/#_compact_example)


[datasets](https://github.com/jdorfman/awesome-json-datasets)