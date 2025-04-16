# Sample project showing Vitest base path bug

When the base path set in `svelte.config.js` is equal to the beginning of the actual project path vitest fails because it resolves the node_modules path incorrectly.

## Steps to reproduce

If you are on macOS simply:

- clone this sample repo somewhere into your home directory (path to project starts with `/Users`)
- try to run `npm run test`

If you are on another OS:

- clone this sample repo somewhere on your machine and replace in `svelte.config.js` in the line `base: "/Users"` the `"/Users"` by the beginning of your project path.
- try to run `npm run test`
