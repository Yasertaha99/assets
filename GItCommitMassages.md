# **cheatsheet for writing good Git commit messages**
- something simple you can follow every time. Here’s a practical one:

---

# ✅ Git Commit Message Cheatsheet

### 1️⃣ Format (Conventional Style)

```
<type>(<scope>): <short description>
<BLANK LINE>
<longer description / details>
<BLANK LINE>
<footer / issues / breaking changes>
```

---

### 2️⃣ Commit Types (Common)

| Type       | Description                         |
| ---------- | ----------------------------------- |
| `feat`     | New feature                         |
| `fix`      | Bug fix                             |
| `chore`    | Build / config / tooling changes    |
| `docs`     | Documentation changes               |
| `style`    | Code style / formatting only        |
| `refactor` | Refactoring (no feature/bug change) |
| `perf`     | Performance improvements            |
| `test`     | Add / modify tests                  |
| `ci`       | CI/CD changes                       |

---

### 3️⃣ Scope (Optional)

* The part of the project affected. Examples:

```
(feat): add login form
(fix(auth)): fix token refresh bug
(chore(vite)): update proxy config
```

---

### 4️⃣ Short Description (≤50 chars)

* Clear, present tense, no punctuation at end.
  Examples:

```
feat: add server-side maintenance middleware
fix(api): correct 503 response for maintenance
style: format App.vue with Prettier
```

---

### 5️⃣ Long Description (Optional)

* Explain **why** this change was made, not what (the code already shows that).
  Example:

```
feat(maintenance): show Blade page during maintenance

- Middleware `CheckStatus` added to detect maintenance
- SPA only loads when site is ready
- Admin and API routes bypass maintenance
- Blade page uses 503 and noindex meta for SEO
```

---

### 6️⃣ Footer / Issues / Breaking Changes

* Reference issues or note breaking changes:

```
Closes #23
BREAKING CHANGE: API endpoint /site-status changed
```

---

### ✅ Example Full Commit

```
feat(maintenance): server-side maintenance mode

- Add CheckStatus middleware
- Show Blade maintenance page if site under maintenance
- Admin/dashboard and API routes bypass maintenance
- SPA loads only when site ready
- Blade page uses 503 + noindex
Closes #42
```

---
