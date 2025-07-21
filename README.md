# vite-plugin-js-obfuscator

A simple Vite plugin that obfuscates final JS bundles using [javascript-obfuscator](https://github.com/javascript-obfuscator/javascript-obfuscator)

## Installation

```bash
npm install @sochetra-nov/vite-plugin-js-obfuscator --save-dev
```

## Usage

```js
// vite.config.js
import viteJsObfuscator from "@sochetra-nov/vite-plugin-js-obfuscator";

export default {
  plugins: [
    viteJsObfuscator({
      compact: true,
      controlFlowFlattening: true,
      debugProtection: true,
      debugProtectionInterval: 1000,
      selfDefending: true,
    }),
  ],
};
```

### Preset Config

```js
// vite.config.js
import viteJsObfuscator, {
  highObfuscationLowPerformance,
  mediumObfuscationOptimalPerformance,
  lowObfuscationHighPerformanceConfig,
} from "@sochetra-nov/vite-plugin-js-obfuscator";

export default {
  plugins: [viteJsObfuscator(lowObfuscationHighPerformanceConfig)],
};
```
