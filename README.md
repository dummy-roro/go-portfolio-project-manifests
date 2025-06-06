# Go Portfolio Helm Chart

This Helm chart deploys the **Go Portfolio App** to a Kubernetes cluster. The app is packaged as a Docker container and configured using Kubernetes resources managed via Helm.

---

## 📦 Chart Details

- **App Name**: Go Portfolio
- **Chart Version**: 0.1.0
- **Maintainer**: dummy-roro
- **Source Repo**: [GitHub - go-portfolio](https://github.com/dummy-roro/go-portfolio)
- **Docker Image**: `docker.io/<your-dockerhub-username>/go-portfolio:<tag>`

---

## 🚀 Installation

```bash
helm repo add go-portfolio https://dummy-roro.github.io/go-portfolio-project-manifests
helm install my-portfolio go-portfolio/go-portfolio
```

To install from local chart:

```bash
helm install my-portfolio ./go-portfolio
```

---

## ⚙️ Configuration

| Parameter       | Description                         | Default              |
|----------------|-------------------------------------|----------------------|
| `image.repository` | Docker image repository             | `docker.io/your-username/go-portfolio` |
| `image.tag`     | Docker image tag (e.g. commit SHA)  | `latest`             |
| `image.pullPolicy` | Image pull policy                   | `IfNotPresent`       |
| `service.type`  | Kubernetes service type              | `ClusterIP`          |
| `service.port`  | Service port                         | `80`                 |
| `replicaCount`  | Number of app replicas               | `1`                  |

To customize:

```bash
helm install my-portfolio ./go-portfolio \
  --set image.tag=abc1234 \
  --set replicaCount=2
```

---

## 🔄 Upgrade

```bash
helm upgrade my-portfolio ./go-portfolio --set image.tag=<new-sha>
```

---

## 🧪 Testing

You can test the chart locally using Helm:

```bash
helm template ./go-portfolio
```

---

## 🧼 Uninstall

To delete the deployment:

```bash
helm uninstall my-portfolio
```

---

## 📁 Project Structure

```text
charts/
  go-portfolio/
    Chart.yaml
    values.yaml
    templates/
    README.md   <-- You are here
```

---

## 🛠️ Helm Dependencies

This chart does not use subcharts or dependencies. All templates are self-contained.

---

## 📞 Support

For issues or contributions, please visit the [main GitHub repository](https://github.com/dummy-roro/go-portfolio).
