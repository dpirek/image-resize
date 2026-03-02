# resize-image-wasm

Zero-dependency image resize utility built with Node.js and WebAssembly.

## Notes

- No npm dependencies are required.
- Resize math uses an embedded WASM module.
- Supported input/output formats: `.bmp`, `.ppm` (P6 binary), `.jpg`, `.jpeg`, `.png`.
- JPEG/PNG support uses the macOS `sips` system tool for codec conversion.

## Usage

```bash
node ./src/resize.js --input ./in.bmp --output ./out.bmp --width 1200
```

Or:

```bash
npm run resize -- --input ./in.ppm --output ./out.ppm --height 480
```

JPEG example:

```bash
node ./src/resize.js --input ./in.jpg --output ./out.jpg --width 1200
```

PNG example:

```bash
node ./src/resize.js --input ./in.png --output ./out.png --width 1200
```

## Options

- `--input, -i` input file path (required)
- `--output, -o` output file path (required)
- `--width, -w` target width
- `--height, -h` target height

At least one of `--width` or `--height` is required.
