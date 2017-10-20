# Some rules


- In accordance with the goal of vulgarization, a node should have between 2 and 5 children. If you have more, it's probably a good idea to factorize children into a broader description, easier to understand, and make it a node for more precise children.

- Use github flavored markdown (GFM)

- Links should be relatives

```
[Contribution guidelines for this project](docs/CONTRIBUTING.md)
```

- Structure of documents :
  - nodes and leafs are folders with `index.md` describing the node/leafs
  - for navigability, each index.md should reference links to:
    - its parent
    - its children (if any)
    - its previous and next siblings (if any)  
