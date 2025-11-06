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

### How the Pre-release Cycle Works

1. Start with the first pre-release:  
   `1.0.0-alpha.1`
2. As fixes or changes are added, increment the pre-release number:  
   `1.0.0-alpha.2`, `1.0.0-alpha.3`, etc.
3. When the project becomes feature-complete, switch to **beta**:  
   `1.0.0-beta.1`
4. Once testing stabilizes, release **RC (Release Candidate)** versions:  
   `1.0.0-rc.1`, `1.0.0-rc.2`
5. When fully tested and approved, release the stable build:  
   `1.0.0`

---

### Handling Many Pre-releases

Yes, you can technically have versions like `1.0.0-alpha.32` —  
the `.32` simply means it’s the 32nd pre-release build of version `1.0.0`.

However, it’s better to move through **phases** rather than having endless alphas:

| Stage | Example | Purpose |
|--------|----------|----------|
| Alpha | `1.0.0-alpha.1` → `1.0.0-alpha.5` | Early internal testing |
| Beta | `1.0.0-beta.1` → `1.0.0-beta.4` | Feature-complete, wider testing |
| RC | `1.0.0-rc.1` → `1.0.0-rc.2` | Final validation before release |
| Stable | `1.0.0` | Production-ready version |

This keeps the version history clean and shows progress toward stability.

---

### After the Stable Release

Once `1.0.0` is released:
- A **bug fix** → `1.0.1`
- A **new feature** → `1.1.0`
- A **breaking change** → `2.0.0`

Future development for the next version can start again as pre-releases:

1.1.0-alpha.1 → 1.1.0-beta.1 → 1.1.0 → 1.1.1 → ...
## 🚀 4. Recommended Practices

✅ **Always bump versions before merging** into `main` or deploying.  
✅ **Update CHANGELOG.md** to explain what changed.  
✅ **Tag each release** in Git:

```bash
git tag -a v1.2.0 -m "Add new analytics dashboard"
git push origin v1.2.0
