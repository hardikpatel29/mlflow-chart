# 🧪 MLflow Helm Chart

This repository hosts a Helm chart for deploying [MLflow](https://mlflow.org/) using the Bitnami Helm chart as a base.

---

## 📦 How This Chart Was Packaged

### 1. Pull the Bitnami Chart

```bash
helm pull bitnami/mlflow --untar
```

### 2. Package the Chart

```bash
helm package ./infra/helm/mlflow
```

### 3. Generate `index.yaml`

```bash
helm repo index charts/ --url https://github.com/hardikpatel29/mlflow-chart/
```

### 4. Move Files to `docs/` Directory

```bash
mkdir -p docs
cp charts/* docs/
```

### 5. Push to GitHub

```bash
git add .
git commit -m "Add packaged chart and index"
git push origin main
```

---

## 🌐 Enable GitHub Pages

1. Go to your GitHub repository.
2. Navigate to **Settings** → **Pages**.
3. Under **Source**, choose:
   - **Branch**: `main`
   - **Folder**: `/docs`
4. Click **Save**.

> This will publish your Helm chart repo at:  
> `https://hardikpatel29.github.io/mlflow-chart/`

---

## 🚀 How to Use This Helm Repository

### Add the Repository

```bash
helm repo add my-mlflow https://hardikpatel29.github.io/mlflow-chart/
```

### Update Repositories

```bash
helm repo update
```

### Search Charts

```bash
helm search repo my-mlflow
```

---

## 📁 Directory Structure

```
mlflow-chart/
├── docs/
│   ├── mlflow-x.y.z.tgz
│   └── index.yaml
├── mlflow/
└── README.md
```

---


