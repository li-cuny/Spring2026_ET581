## 1. What is a Branch?
A branch is like a **parallel universe** for your code:
- The main branch (`main` or `master`) is your stable code.
- A new branch lets you **experiment or work on a feature** without breaking the main code.

Think: "I want to try something new, but I don’t want to ruin the main code." That’s a branch.

---

## 2. See Which Branch You Are On
Open your terminal in your project folder:

```bash
git branch
```
- The branch with * is your current branch.

- Usually, it starts on main (or master).

## 3. Create a New Branch
```bash
git branch my-new-branch
```

Replace my-new-branch with your feature name, e.g., feature/login or bug/header-fix.

This creates the branch, but you are still on your old branch.

- Always switch back to main before creating a new branch:
```bash
git checkout main
```

## 4. Switch to the Branch
git checkout my-new-branch


Now you are “inside” the branch and can make changes safely.

## 5. Shortcut: Create & Switch in One Step
```bash
git checkout -b my-new-branch
```

This does both create and switch at the same time.

## 6. Push Your Branch to Remote (Optional)
```bash
git push -u origin my-new-branch
```

-u sets it as the default remote branch so next time you can just git push.



