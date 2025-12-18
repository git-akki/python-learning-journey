# Python Virtual Environment

A **virtual environment** is an isolated Python setup created **per project**.

It allows each project to:
- use its own Python packages
- use different versions of the same library
- avoid breaking other projects

This is a **standard practice** in professional Python development.

---

## Why Virtual Environments Exist

When you install Python on your machine, it is installed **system-wide**.

If you then install packages using:
```bash
pip install some-library
