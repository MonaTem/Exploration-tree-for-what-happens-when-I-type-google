# Some rules


- In accordance with the goal of vulgarization, a node should have between 2 and 5 children. If you have more, it's probably a good idea to factorize children into a broader description, easier to understand, and make it a node for more precise children.

- Use github flavored markdown (GFM)

- Links should be relatives

```
[Contribution guidelines for this project](./CONTRIBUTING.md)
```

- Structure of documents :
  - nodes and leafs are folders with `README.md` describing the node/leafs. It enables github/gitlab to automatically render the files when you browse the folders.
  - for navigability, each `README.md` should reference links to its children (if any)
