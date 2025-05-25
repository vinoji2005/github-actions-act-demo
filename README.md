# ⚡️ GitHub Actions + act Demo

Run GitHub Actions **locally** — fast, safe, and efficient 🚀  
This repository shows you how to lint and test Python code locally using [act](https://github.com/nektos/act), a tool that simulates GitHub Actions on your machine using Docker.

> 🎯 Ideal for DevOps, SREs, Cloud Architects, and Developers who want to save time!

---

## 📌 Features

✅ Linting with `flake8`  
✅ Unit testing with `pytest`  
✅ Simulate GitHub-hosted runners using Docker  
✅ Compatible with Apple M1/M2 chips via `--container-architecture`  
✅ No need to push to GitHub every time you tweak a workflow

---

## 🛠️ Prerequisites

| Tool    | Required | Install Guide                              |
|---------|----------|--------------------------------------------|
| Docker  | ✅ Yes    | [Install Docker](https://docs.docker.com/get-docker/) |
| `act`   | ✅ Yes    | [act Installation](https://github.com/nektos/act#installation) |

---

## 🧪 Workflows Included

### 🔍 Lint Workflow (`flake8`)
Run Python linter locally:

```bash
act -j lint
```

### 🧪 Test Workflow (`pytest`)
Run unit tests locally:

```bash
act -j test
```

### 🧠 Run All Jobs for a GitHub Event
Simulate a `push` or `pull_request` event and run all jobs:

```bash
act push
```

You can also use:

```bash
act pull_request
```

---

## 🍎 M1/M2 Mac Users

If you're using an Apple Silicon Mac, use:

```bash
act -j lint --container-architecture linux/amd64
```

Or set this as the default:

```bash
echo "--container-architecture linux/amd64" >> ~/.actrc
```

---

## 🔐 Using Secrets

1. Copy the example file:

```bash
cp .secrets.example .secrets
```

2. Add your secrets to `.secrets`:

```ini
MY_SECRET=super-secret-token
```

3. Run `act` with secrets:

```bash
act --secret-file .secrets
```

---

## 💡 Python Dependencies

Add the following to `requirements.txt`:

```txt
flake8
pytest
```

Install them locally (optional):

```bash
pip install -r requirements.txt
```

---

## 📝 Sample Python App (`src/app.py`)

```python
def greet(name):
    print(f"Hello, {name}!")

greet("GitHub Actions")
```

## 🧪 Sample Unit Test (`tests/test_sample.py`)

```python
def test_sample():
    assert 2 + 2 == 4
```

---

## 📄 .gitignore

```gitignore
__pycache__/
*.pyc
.venv/
.env/
.secrets
```

---

## 📚 Resources

- 📦 [`act` GitHub Repo](https://github.com/nektos/act)
- 📘 [GitHub Actions Docs](https://docs.github.com/en/actions)
- 🧪 [pytest Docs](https://docs.pytest.org/)
- 🔍 [flake8 Docs](https://flake8.pycqa.org/en/latest/)

---

## 👨‍💻 Author

**Vinoth Subbiah**  
Principal Cloud Architect | DevOps | SRE | Infra Automation  
📧 [vinoji2005@gmail.com](mailto:vinoji2005@gmail.com)  
🔗 [GitHub](https://github.com/vinoji2005) • [Medium](https://medium.com/@vinoji2005)

---

## 🤝 Contributing

Pull requests are welcome!  
If you find a bug or want to add features (Docker builds, Terraform, Node.js workflows), open an issue or PR 🚀

---

## 🏁 License

[MIT](LICENSE)
