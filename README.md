# d3 indirections types

Type declarations for d3 indirections

## Installation

```
npm install @types/d3-indirections
```

## Notes

### Status

Currently missing are the full list of `ResourceType`s offer by d3, as well as the OSC, DMX and UDP indirection kinds.

### Indirection kinds

It may be useful to define the following functions to deduce the kind
of an incoming indirection in an if statement.

```typescript
/** @returns Whether an indirection is a manual indirection. */
function isManualIndirection(value: Indirection): value is ManualIndirection {
    return (<ManualIndirection>value).manualIndirection !== undefined;
}

/** @returns Whether an indirection is a list indirection. */
function isListIndirection(value: Indirection): value is ListIndirection {
    return (<ListIndirection>value).listIndirection !== undefined;
}
```