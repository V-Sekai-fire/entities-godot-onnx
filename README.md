# entities-godot-onnx

A Rust GDExtension that loads ONNX models in Godot and runs inference on tensors from GDScript.

## What it is for

A model loads as a resource, inputs are built as tensors from packed arrays, and a call returns the output tensors, using the platform's hardware execution provider where the build has one and the CPU elsewhere. An editor plugin imports `.onnx` files, and `sample/` is a Godot project that exercises it. The script API is in `docs/USAGE.md`.

## Build and run

```sh
janet misc/build.janet
```

This runs the Rust tests, builds the extension and copies it into `sample/`; open `sample/` in Godot and run the main scene. `docs/BUILD.md` has the requirements.

## Licence

Apache-2.0 or MIT, at your option; see `LICENSE`.
