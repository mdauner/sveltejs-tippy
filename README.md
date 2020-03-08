# sveltejs-tippy

![npm](https://img.shields.io/npm/v/sveltejs-tippy)
![npm bundle size](https://img.shields.io/bundlephobia/minzip/sveltejs-tippy)
![npm](https://img.shields.io/npm/dw/sveltejs-tippy)

![GitHub](https://img.shields.io/github/license/mdauner/sveltejs-tippy)
![Actions Status](https://github.com/mdauner/sveltejs-tippy/workflows/CI/badge.svg)

Tippy.js for [Svelte](https://svelte.dev/).

## Install

```shell
$ npm i sveltejs-tippy
```

or

```shell
$ yarn add sveltejs-tippy
```

## How to use

### Example

[![Edit sveltejs-tippy](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/s/sveltejs-tippy-h2ns7?fontsize=14&module=%2FApp.svelte)

```html
<script>
  import tippy from "sveltejs-tippy";

  const props = {
    content: "<span class='tooltip'>Styled tooltip text</span>",
    placement: "bottom"
  };
</script>

<style>
  :global(.tooltip) {
    font-size: 1.2rem;
    text-transform: uppercase;
  }
</style>

<button use:tippy={props}>
  Hover me
</button>
```
