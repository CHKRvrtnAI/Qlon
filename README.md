
# 🔷 QLon Playground

> 👁️ Visualize. ✍️ Describe. 🤖 Execute.  
> **QLon** is a minimal declarative language to describe patterns over graphs.
> This playground lets you write QLon queries, visualize them, and get results instantly.

---

## ✨ What is QLon?

**QLon** is a human-friendly, AI-friendly, automation-ready language to express relationships between entities.

Example:
```qlon
people[name="Alice"] → friends[age>30]
```

---

## 📚 Basic Syntax

### ▶️ Node
```qlon
Entity
```

### ▶️ Node with filters
```qlon
Entity[property="value"]
Entity[prop!=42]
Entity[score>=7.5]
```

### ▶️ Relationship
```qlon
EntityA → relation → EntityB
```

### ▶️ Multi-hop path
```qlon
A → B → C → D
```

---

## 🔧 Supported Operators

| Operator | Meaning              |
|----------|----------------------|
| `=`      | Equal                |
| `!=`     | Not equal            |
| `>`      | Greater than         |
| `<`      | Less than            |
| `>=`     | Greater or equal     |
| `<=`     | Less or equal        |

---

## 🧠 Examples

```qlon
people[name="Alice"] → friends[age=32]
people[age>=30] → friends[age!=28]
```

```qlon
people → friends → coworkers[seniority>3]
```

---

## 🧪 Mock Dataset (included)

```json
{
  people: [
    {
      name: "Alice",
      age: 30,
      friends: [
        { name: "Bob", age: 28, friends: [{ name: "Carol", age: 32 }] },
        { name: "Carol", age: 32, friends: [{ name: "Bob", age: 28 }, { name: "Suzy", age: 18 }] }
      ],
      colleagues: [
        { name: "Dave", age: 27, department: "HR" },
        { name: "Eve", age: 35, department: "Marketing" }
      ]
    },
    {
      name: "Dave",
      age: 27,
      friends: [{ name: "Alice", age: 30 }],
      department: "HR"
    },
    {
      name: "Carol",
      age: 32,
      friends: [{ name: "Alice", age: 30 }],
      colleagues: [{ name: "Eve", age: 35, department: "Marketing" }]
    },
    {
      name: "Eve",
      age: 35,
      department: "Marketing",
      friends: [{ name: "Bob", age: 28 }],
      colleagues: [{ name: "Alice", age: 30 }]
    }
  ],
  departments: [
    {
      name: "HR",
      employees: [{ name: "Dave", age: 27 }],
      location: "Building 1"
    },
    {
      name: "Marketing",
      employees: [{ name: "Eve", age: 35 }],
      location: "Building 2"
    }
  ]
}
```

---

## 🧱 QLon Grammar (draft)

```ebnf
query      ::= path
path       ::= node ("→" node)*
node       ::= NAME ("[" filters? "]")?
filters    ::= filter ("," filter)*
filter     ::= NAME operator value
operator   ::= "=" | "!=" | ">" | "<" | ">=" | "<="
value      ::= number | quoted_string
```

---

## 🚀 Roadmap

- [x] Logical operators support
- [x] Interactive graph rendering
- [ ] Wildcards and OR support (`*`, `|`)
- [ ] `.qlon` file saving
- [ ] JSON export
- [ ] Prompt-to-QLon AI integration

---

## 🪪 License

MIT © 2025

---

## 💬 Contact & credits

Built with ❤️ to define the future of **action-driven reasoning AI**.
