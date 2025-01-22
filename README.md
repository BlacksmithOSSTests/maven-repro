# Maven Build Cache Demo

This is a simple project to demonstrate Maven's repository and build cache functionality.

## Project Structure
- Simple Calculator class with basic arithmetic operations
- JUnit 5 tests to verify functionality
- Maven configuration with build cache settings

## Building and Testing

To build the project:
```bash
mvn clean install
```

To run tests:
```bash
mvn test
```

## Testing Repository and Build Cache

1. First build (will download dependencies and populate local repository):
```bash
mvn clean install
```

2. Second build (should be faster due to cached dependencies and build artifacts):
```bash
mvn install
```

3. To verify build cache, make a small change to the Calculator.java file and rebuild.

## Local Repository Location
- Default: `~/.m2/repository`
- You can check the cached artifacts in this directory

## Build Cache Location
- Default: `~/.m2/build-cache`
- Maven stores compiled classes and other build artifacts here for incremental builds 