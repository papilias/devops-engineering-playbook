# Production Readiness Checklist

Service / Platform: `[Service Name]`  
Target Go-Live Date: `YYYY-MM-DD`  
Engineering Lead: `@owner`

## 1. CI/CD & Supply Chain Security
- [ ] Automated build and test pipeline configured via centralized templates
- [ ] Container image built from approved hardened base image (non-root user)
- [ ] Vulnerability scan (Trivy) passing with zero unmitigated `CRITICAL` CVEs
- [ ] SBOM generated and archived as a build artifact

## 2. Infrastructure & Resilience
- [ ] Infrastructure provisioned via version-controlled IaC (Terraform / Bicep)
- [ ] Horizontal Pod Autoscaler (HPA) and resource requests/limits configured
- [ ] Liveness and readiness probes (`/healthz`) verified under load
- [ ] Zero-downtime rolling deployment strategy tested in staging

## 3. Identity, Secrets & Networking
- [ ] Zero hardcoded credentials; secrets injected via Key Vault / Workload Identity
- [ ] Least-privilege RBAC / IAM roles reviewed
- [ ] TLS enforced end-to-end with valid certificate auto-renewal

## 4. Observability & Incident Response
- [ ] Structured logs shipping to central Log Analytics / CloudWatch
- [ ] Key SLIs (latency, error rate, saturation) visible on team dashboard
- [ ] Actionable alerts routed to on-call channel with linked runbook
