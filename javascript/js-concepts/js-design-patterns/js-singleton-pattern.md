# Singleton

- It is essential in a scenario where only one instance needs to be created.
- For example, a **database connection**.
  - It is only possible to create an instance when the connection is closed or you make sure to close the open instance before opening a new one.
  - **This pattern is also referred to as strict pattern**.
- One drawback associated with this pattern is
  - its daunting experience in testing because of its hidden dependencies objects  
    which are not easily singled out for testing.

## Code Example

---

#### **From** [[js-design-patterns]] / [[js-concepts]]
