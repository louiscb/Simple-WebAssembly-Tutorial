# Incredibly simple "Hello World!" in WebAssembly from C

This is a tutorial on how to create a incredibly simple program compiling C to WebAssembly. Avoiding as much "glue code" and external libraries as possible.

## Requirements

- Python
- Clang (Up to date version supporting wasm32)
- A modern browser

# Steps

First compile the c file to wasm using clang.

```
clang --target=wasm32 -nostdlib -Wl,--no-entry -Wl,--export-all -o main.wasm main.c
```

Then we need to run a HTTP server to serve our wasm file.

```
python server.py
```

Navigate to `localhost:8000` and you should see "Hello World!" in your browser. Opening the Javascript console will provide you with the results of the add function.


