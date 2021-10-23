# storybook-base-url-repro

This repo shows that Storybook with the Webpack 5 builder cannot resolve
TypeScript absolute imports.

1. `yarn install`
2. `yarn tsc` (passes)
3. `yarn storybook` (fails: `ModuleNotFoundError: Module not found: Error: Can't resolve 'Components/Button'`)
4. Rename `AbsoluteImport.stories.tsx` to `AbsoluteImport.tsx` to exclude it from Storybook.
5. `yarn storybook` works now
