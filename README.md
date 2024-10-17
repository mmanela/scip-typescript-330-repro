# Minimal Repro for Duplicate Path in scip-typescript

This is a minimal repro for  https://github.com/sourcegraph/scip-typescript/issues/330. 

## Steps 
1. From the child folder, run `scip-typescript index` 
2. Examine the index and notice it contains `../index.ts` path


The issue is caused due to the 
```
   "references": [
      { "path": ".." }
    ]
```

property in the child folder's tsconfig.json.
