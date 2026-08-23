# Yacht Documentation Website ⛵

Official documentation source for **[Yacht](https://github.com/SelfhostedPro/Yacht)** — a web interface for managing Docker containers with an emphasis on templates and 1-click deployments.

This website is built with **[Docusaurus](https://docusaurus.io/)**.

---

## 🚀 Quick Start

### 1. Prerequisites
- **Node.js**: >= 18.0 (Node 20 recommended)
- **Yarn**: Classic (`v1.x`)

### 2. Installation

```bash
yarn install --frozen-lockfile
```

### 3. Local Development

```bash
yarn start
```

Starts a local development server at `http://localhost:3000` with hot-reloading.

### 4. Build

```bash
yarn build
```

Compiles the static assets and HTML into the `build/` directory for production deployment.

---

## 🚢 CI/CD & Deployment

Deployments to **GitHub Pages** are automated via GitHub Actions:
- Any commit merged into the `main` branch triggers `.github/workflows/deploy.yml`.
- Builds the Docusaurus project and publishes the artifact directly to the GitHub Pages environment.
- Manual triggers are also available via `workflow_dispatch` in the **Actions** tab.

---

## 🤝 Contributing

Contributions to improve Yacht's documentation are welcome!
1. Fork or branch from `main`.
2. Edit or add documentation markdown files in `docs/` and sidebar entries in `sidebars.js`.
3. Test locally with `yarn start`.
4. Open a Pull Request.

---

## 📜 License
Licensed under the [MIT License](LICENSE).
