# Docker based Swift REPL and compiler

Run Swift on any system using [docker](http://docker.com).

## Using this container

### Running the swift REPL

```bash
docker run -t -i jensravens/swift swift
```

### Running your script with the swift interpreter

This mounts your folder under `/app` inside of the container and executes it.

```bash
docker run -t -i -v [your folder here]:/app jensravens/swift swift /app/main.swift
```

### Compiling your project

This is using `swift build` including the swift package manager to build your project in the specified directory.

```bash
docker run -t -i -v [your folder here]:/app -w /app jensravens/swift swift build
```

## Development

### Building the image

```bash
docker build -t swift .
```
