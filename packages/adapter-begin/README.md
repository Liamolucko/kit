# adapter-begin

Adapter for Svelte apps that creates a [Begin](https://begin.com/) app, using a function for dynamic server rendering.

## Configuration

Add the adapter to your `svelte.config.cjs`:

```js
module.exports = {
  ...
	adapter: '@sveltejs/adapter-begin'
};
```

This adapter expects to find an OpenJS Architect [app.arc](https://arc.codes/) file in the project root. It will use it to determine where to write static assets to based on the `@static` configuration. The default configuration for this file is as follows:

```arc
@app
svelte-kit-app

@http
get /

@static
folder public
```
