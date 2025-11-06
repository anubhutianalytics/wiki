# 🔢 Semantic Versioning Guide

Version numbers help us (and others) understand **what changed** in a release — whether it's a small fix or a major redesign.  
We follow the **Semantic Versioning (SemVer)** standard:  
**MAJOR.MINOR.PATCH** (e.g. `2.4.1`)

---

## 📦 1. Version Format

**MAJOR.MINOR.PATCH**

| Part | Example | When to Increment | Meaning |
|------|----------|------------------|----------|
| **MAJOR** | `2.0.0` | When you make **incompatible or breaking changes** | Old code may no longer work |
| **MINOR** | `2.1.0` | When you **add new features** that are **backward-compatible** | New capabilities, but old ones still work |
| **PATCH** | `2.1.3` | When you **fix bugs** or make **small safe changes** | Improves reliability without new features |

---

## 🧭 2. Examples

| Scenario | Old Version | New Version | Explanation |
|-----------|--------------|-------------|--------------|
| Fixed a small bug | `1.0.0` | `1.0.1` | PATCH increment |
| Added a new API endpoint | `1.0.1` | `1.1.0` | MINOR increment |
| Changed existing API behavior | `1.1.0` | `2.0.0` | MAJOR increment |
| Added docs or internal changes only | `2.0.0` | `2.0.0` | No version bump needed (optional) |

---

## 🧩 3. Pre-release Versions

During active development, you can use pre-release tags:

| Format | Example | Meaning |
|---------|----------|---------|
| `1.0.0-alpha` | `1.0.0-alpha` | Early testing, unstable |
| `1.0.0-beta` | `1.0.0-beta` | Feature-complete but still testing |
| `1.0.0-rc.1` | `1.0.0-rc.1` | Release candidate, almost ready for final release |

---

## 🚀 4. Recommended Practices

✅ **Always bump versions before merging** into `main` or deploying.  
✅ **Update CHANGELOG.md** to explain what changed.  
✅ **Tag each release** in Git:

```bash
git tag -a v1.2.0 -m "Add new analytics dashboard"
git push origin v1.2.0
