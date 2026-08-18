# AI service Kubernetes manifests

Before applying, replace `REPLACE_WITH_OPENROUTER_API_KEY` in `secret.yaml` and
set `FRONTEND_ORIGIN` in `deployment.yaml` to the public URL of the frontend.

Build the Docker image using the AI Integration directory, make it available to
your Kubernetes cluster, then apply these manifests:

```powershell
kubectl apply -f k8s-manifest/ai-service
```

The service is internal (`ClusterIP`). Expose it through an Ingress or API
gateway for browser requests; do not expose the OpenRouter key to the frontend.
