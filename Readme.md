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

Run the development server:

```sh
bud run
```

Then in another terminal, run `staticgen` to generate the static assets into `build/`

> Note: For this step, you'll need [staticgen](https://github.com/tj/staticgen) in your `$PATH`

```sh
staticgen
```

Finally, copy the generated build files into bud's `runtime/web/welcome` package.
