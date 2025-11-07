# my-dumb-helmcharts

A Helm chart repository hosted on GitHub Pages.

## 🚀 Usage

Add this Helm repository:

```bash
helm repo add my-charts https://christianh814.github.io/my-dumb-helmcharts/
helm repo update
```

Search for available charts:

```bash
helm search repo my-charts
```

Install a chart:

```bash
helm install my-release my-charts/<chart-name>
```

## 📦 Available Charts

- **example-app** - A sample nginx deployment (v0.1.0)

## 🛠️ Adding New Charts

1. Create your chart in the `charts/` directory:

```bash
cd charts/
helm create my-new-chart
```

2. Commit and push your changes to the `main` branch:

```bash
git add charts/my-new-chart
git commit -m "Add my-new-chart"
git push
```

3. The GitHub Actions workflow will automatically:
   - Package the chart
   - Create a GitHub release
   - Update the Helm repository index on GitHub Pages

## 📋 Repository Structure

```
.
├── .github/
│   └── workflows/
│       └── release.yml        # GitHub Actions workflow for chart releases
├── charts/
│   └── example-app/           # Example Helm chart
│       ├── Chart.yaml
│       ├── values.yaml
│       └── templates/
└── README.md
```

## 🔧 How It Works

This repository uses:

- **GitHub Pages** (`gh-pages` branch) to host the Helm repository
- **GitHub Actions** to automate chart packaging and releases
- **helm/chart-releaser-action** to manage chart versions and releases

When you push changes to charts in the `main` branch, the workflow:

1. Packages each chart that has changed
2. Creates a GitHub release with the chart package
3. Updates the `index.yaml` on the `gh-pages` branch
4. Makes the chart available via the Helm repository

## 📝 Notes

For personal use, you probably don't want to use this.
