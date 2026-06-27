# Contributing to Eudora Menu

Thanks for your interest in contributing! Here's how to get involved.

## 🐛 Reporting Bugs

Open a [GitHub Issue](../../issues/new?template=bug_report.md) and fill out the bug report template.  
Please include:
- What you clicked / what you did
- What you expected to happen
- What actually happened
- Your YimMenu and GTA V version

## 💡 Suggesting Features

Open a [Feature Request](../../issues/new?template=feature_request.md) and describe your idea.  
The more detail you give, the easier it is to implement.

## 🔧 Submitting Code

1. Fork this repository
2. Create a new branch: `git checkout -b feature/my-feature`
3. Make your changes to `Eudora.lua`
4. Commit with a clear message: `git commit -m "feat: add X button to Y menu"`
5. Push your branch and open a Pull Request

### Code Style Guidelines
- Use `local` variables where possible — avoid polluting global scope
- Use `ipairs` loops for repetitive button lists, not copy-pasted blocks
- Move `gui.show_message` calls **outside** of loops — never inside
- Keep indentation consistent (4 spaces)
- Add a comment for any non-obvious stat name or global offset

## ❤️ Thank You

Every contribution, no matter how small, helps make Eudora better for everyone.
