# Modular Monolith with Clean Architecture and Centralized Directory.Build

This project is a **.NET 9** designed following the principles of **Clean Architecture** and supported by a **multi-layer, centralized Directory.Build structure**.  
The goal is to establish a scalable, predictable, and maintainable architecture that grows with the business while keeping development consistent across the entire solution.

---

## 📐 About Clean Architecture

**Clean Architecture**, popularized by Robert C. Martin (Uncle Bob), promotes a design in which:

- **Business rules are at the center** (Domain)
- **Infrastructure and external systems are outer layers**
- **Dependencies always flow inwards**, toward the core
- **Use cases drive the application**, not frameworks

This approach creates software that is:

- **Independent of UI**  
- **Independent of database**  
- **Independent of external frameworks**  
- **Highly testable**  
- **Easy to evolve without breaking the rest of the system**

The main intention is to build systems where **change is isolated**, and core business logic remains clean, stable, and decoupled from volatile technologies.

---

Each layer has a clear responsibility:

- **Domain** → Entities, Aggregates, Value Objects, Domain Events, Interfaces  
- **Application** → Use Cases, Commands, Queries, Validation, Ports  
- **Infrastructure** → Database, Persistence, External Services, Providers  
- **Presentation** → REST API, Controllers/Endpoints, Configuration  
- **Tests** → Validation of behavior across all layers  

This structure ensures that each module can grow independently without compromising the overall architecture.

---

## ⚙️ Centralized Directory.Build — Why It Matters

A key characteristic of this project is the use of **Directory.Build.props** and **Directory.Packages.props** to centralize:

- Compiler settings  
- Warning rules  
- Analyzer configurations  
- NuGet package versions  
- Build behaviors  
- Code-style definitions  
- Access control between projects  
- Shared MSBuild properties across the entire solution  

### 🔍 Why is this important?

Large solutions often struggle with:

- Configuration duplication  
- Divergent rules between projects  
- Inconsistent analyzers  
- Versions drifting across modules  
- Difficulty maintaining a unified architecture  

By centralizing build configuration:

✔ You guarantee **architectural consistency**  
✔ All modules follow the **same compiler behaviors**  
✔ A single change applies to **every project instantly**  
✔ New projects added to the solution automatically inherit all settings  
✔ The architecture can scale predictably without configuration drift  
✔ It enforces conventions that teams or contributors must follow  

---

## 🚀 Key Features

- Full **Clean Architecture** structure  
- Centralized **Directory.Build** And && **Directory.Packages** configuration  
- Strong boundaries between modules  
- Shared conventions applied solution-wide  
- MSBuild-driven architecture governance  
- Easy scalability without configuration chaos  
- Ideal for enterprise-grade systems  