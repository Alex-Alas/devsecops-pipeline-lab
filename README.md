# devsecops-pipeline-lab

Laboratorio 3 · Automatización del Despliegue Continuo mediante IaC
Nube II — ESEN, Ciclo III 2026

Sitio web estático desplegado en AWS S3 mediante Terraform, con despliegue
continuo automatizado por GitHub Actions.

## Estructura

- `infra/` — código Terraform (bucket S3, website configuration, política de lectura pública)
- `infra/website/index.html` — contenido del sitio
- `.github/workflows/deploy.yml` — pipeline de despliegue continuo

## Despliegue local

```bash
cd infra
terraform init
terraform plan  -var="bucket_name=NOMBRE_DEL_BUCKET"
terraform apply -var="bucket_name=NOMBRE_DEL_BUCKET" -auto-approve
```
