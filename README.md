# QLon Playground 🕸️

**Query Language for Graph Reasoning** — a minimal, human-readable and AI-friendly language to explore and traverse relational graphs, JSON structures and knowledge workflows.

This playground is a lightweight prototype to test QLon queries directly on JSON-based graphs, with real-time visual output and mock explanations.

---

## ✨ Features

- 🧠 **Minimal syntax** inspired by XPath, Cypher and GraphQL  
- 🧾 **Pattern matching** on graph-like JSON data  
- 🔍 **Select fields**, navigate nested structures, and filter nodes  
- 📊 **Visual graph rendering** with `cytoscape.js`  
- 📂 **Load your own JSON files** to test live  
- 💬 **Mock natural language explanations** (future: AI-powered)  
- ✅ **MIT licensed**, open-source and modular

---

## 📦 Example Query

```qlon
nodes[process="SCM"] select(id, mode)
→ Filters nodes with process = "SCM" and returns the id and mode of each.

🚀 Quickstart
Clone this repo or download the ZIP

Open index.html in your browser

Load your JSON graph (optional)

Write QLon queries and explore the result & graph!

📁 JSON structure expected
The default format is a JSON object with:

json
Copia
Modifica
{
  "nodes": [ { ... } ],
  "connections": [ [fromId, toId], ... ]
}
But you can fully customize the shape and adjust your queries accordingly.

🛣️ Roadmap
 Static prototype with local parsing

 Visual graph rendering

 Tooltip on nodes

 JSON upload

 Connection path navigation (->connections->nodes)

 AI explanation of queries (LLM-based)

 Full Lark parser with AST interpreter

 Integration with agent memory and knowledge RAG
