# 🧩 Engineering Standards

Our engineering conventions ensure consistency across all projects at **Anubhuti Analytics**.

---

## 🗄️ Database Conventions

| Area | Convention |
|------|-------------|
| **Schemas** | Separate schemas for OLTP and OLAP (`oltp` and `dbo`). |
| **Table Names** | Use **plural**, **lowercase**, **snake_case** (e.g., `customers`, `order_items`). |
| **Primary Keys** | Use descriptive names — e.g., `enterprise_id`, **not just** `id`. |
| **Column Names** | Use **lowercase**, **snake_case**. |

---

## 💻 Client-Side Conventions

| Item | Convention |
|------|-------------|
| **Model Class Names** | Singular, **PascalCase** (e.g., `Customer`). |
| **Model File Names** | Singular, **snake_case** (e.g., `customer_model.ts`). |
| **Function Names** | Verb-based, **snake_case** (e.g., `fetch_data()`). |
| **Variable Names** | Descriptive, **snake_case**. |

---

## 🖥️ Server-Side Conventions

| Item | Convention |
|------|-------------|
| **Model Class Names** | Singular, **PascalCase** (e.g., `Order`). |
| **Model File Names** | Singular, **snake_case** (e.g., `order_model.py`). |
| **Function Names** | Verb-based, **snake_case**. |
| **Variable Names** | Descriptive, **snake_case**. |
| **API Routes** | Plural, **kebab-case** (e.g., `/api/customers`, `/api/order-items`). |

---

## 🔄 Version Control

Follow [Semantic Versioning](./semantic-versioning.md) for release versioning.

---

## 🤝 Contributing

If you need to propose a change to these standards:
1. Open a PR with a clear explanation.
2. Tag `@engineering-core` for review.
3. Once approved, update affected documentation or code references.
