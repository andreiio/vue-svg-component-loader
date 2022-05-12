# vue-svg-component-loader
Zero-dependency webpack loader that turns SVG files into Vue components. This loader doesn't do anything else.

## Installation

```sh
npm install vue-svg-component-loader --save-dev
```
## Configuration

```js
module.exports = {
    module: {
        rules: [
            {
                test: /\.svg$/,
                use: [
                    'raw-loader', // not included, install separately
                    'svgo-loader', // not included, install separately
                    'vue-svg-component-loader',
                ],
            },
        ],
    },
};
```

## Usage

```vue
<template>
    <div>
        <AppLogo />
    </div>
</template>

<script>
    import AppLogo from 'path/to/logo.svg';

    export default {
        components: {
            AppLogo,
        },
    };
</script>
```
