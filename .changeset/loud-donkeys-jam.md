---
'satisfier': patch
---

Update `tersify` to `^4.0.6`.

The build also moves from three `tsc` passes to `tsdown`. The published paths are
unchanged (`esm/index.js`, `cjs/index.js`, and the `.d.ts` beside each), but the emitted
JavaScript differs: the CJS output is now `es2015` rather than `es5`, and the unused
`tslib/` output is no longer built. Two `isNaN` calls became `Number.isNaN`; both are
already guarded by a `typeof x === 'number'` check, so behaviour is identical.
