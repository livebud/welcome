# Welcome

Welcome page for new [Bud](https://github.com/livebud/bud) installations.

## Install

```sh
npm install
go mod tidy
bud run
```

## Embedding within Bud

You can update the welcome page in Bud by doing the following.

Note: You'll need [staticgen](https://github.com/tj/staticgen) in your `$PATH`

Run the development server:

```sh
bud run
```

Then in another terminal, run `staticgen` to generate the static assets into `build/`

```sh
staticgen
```

Finally, copy the generated build files into bud's `runtime/web/welcome` package.
