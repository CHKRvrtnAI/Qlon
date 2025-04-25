
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
people[name="Alice"] → friends → friends[name="Suzy"]
people[name="Alice"] → friends → friends
people[name="Alice"] → friends[age=32] → friends
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
