# Glossary — Git-Native Model Registry

| Term | Meaning | Spanish translation / adaptation | Practical application | Examples (max 2) | Synonyms | Common environments |
|---|---|---:|---|---|---|---|
| Git | Distributed version control system for tracking changes in files | Control de versiones distribuido | Version code, configs, model artifacts | `git commit`, `git revert` | VCS | Dev, Data, ML, Infra |
| Repository (Repo) | Versioned container of files and history | Repositorio | Store code, models, and pipelines | Model repo, data repo | Project, codebase | GitHub, GitLab |
| Commit | A snapshot of changes recorded in Git | Confirmación / cambio versionado | Traceability and rollback | Commit a model change, revert commit | Revision | Dev, ML, Data |
| Pull Request (PR) | A request to merge proposed changes into a branch | Solicitud de cambios | Review and governance gate | PR to add new model, PR to update pipeline | Merge Request | GitHub, GitLab |
| Git Hook / Webhook | Event triggered by Git operations | Gancho / notificación automática | Trigger CI/CD or pipelines | PR → trigger training job | Trigger | CI/CD |
| GitOps | Operating systems using Git as the source of truth | Operación basada en Git | Declarative infra and model ops | Commit → deploy infra | Declarative Ops | DevOps, Platform |
| Model Registry | Versioned catalog of ML models + metadata | Registro de modelos | Governance, lineage, and reproducibility | Register v1 model, view metadata | Model catalog | MLOps |
| Model Versioning | Explicit version control for models | Versionado de modelos | Rollback and auditability | `model_v1.2`, rollback to v1.1 | Artifact versioning | ML, Compliance |
| Artifact | A persistent output of a build or pipeline | Artefacto | Store models, serialized files, logs | `.onnx` model file, training logs | Build output | CI/CD, ML |
| Pipeline | An automated sequence of tasks (train → eval → deploy) | Canalización | Define repeatable workflows | `pipeline.yaml` for training | Workflow | CI/CD, MLOps |
| Runner / Agent | Component that executes pipeline jobs | Agente de ejecución | Run jobs in private infra | Training runner on customer network | Worker | CI/CD |
| Infrastructure (Infra) | Compute, storage and network resources | Infraestructura | Run training, serving | GPU cluster, storage buckets | Platform | Cloud, On-prem |
| On-prem / On-premise | Customer-owned, local infrastructure | Infra local / en sitio | For sensitive data or compliance | Local GPU servers | Local infra | Enterprise |
| Tailscale | Zero-trust private network built on WireGuard | Red privada segura (Tailscale) | Securely connect infra and runners | Runner connects via Tailscale mesh | Zero-trust VPN | DevOps, Security |
| Zero-Trust | Security model that never trusts by default | Confianza cero | Minimize lateral movement and access risks | Short-lived access tokens | Least privilege | Security |
| ACL (Access Control List) | Rules that define who can access a resource | Lista de control de acceso | Fine-grained access policies | Repo ACL for reviewers | Access policy | Security |
| RBAC | Role-based access control for permissions | Control por roles | Enforce org roles and permissions | Admin, reviewer roles | Role policy | Enterprise |
| Training (ML) | Process of optimizing a model with data | Entrenamiento | Produce models from datasets | Train with dataset v2 | Fit | ML |
| Fine-tuning | Adjusting a pre-trained model to a target task | Ajuste fino | Adapt LLMs or models for customers | Fine-tune LLM on support data | Transfer learning | AI |
| Dataset | Structured collection of data used for training and testing | Conjunto de datos | Input for training and evaluation | `users_v1.csv` dataset | Data corpus | Data, ML |
| Hyperparameters | Non-learned settings controlling training behavior | Hiperparámetros | Configure training runs | `learning_rate=0.001` | Training config | ML |
| Evaluation (Eval) | Measurement of model performance | Evaluación | Validate model before deploy | Accuracy test, confusion matrix | Validation | ML |
| Drift | Change in data distribution or model performance over time | Deriva del modelo | Detect model degradation | Data drift alert, model decay | Model drift | MLOps |
| Serving / Inference | Running a model to produce predictions | Servicio / inferencia | Provide production predictions | `/predict` API endpoint | Model hosting | Production |
| Rollback | Revert to a previous model or deployment | Reversión | Fast recovery from regressions | Rollback to stable commit | Revert | Ops |
| Audit Log | Immutable log of system events for compliance | Registro de auditoría | Legal and security traces | Access logs, deploy history | Trace | Legal, Security |
| WORM Logs | Write-once, read-many logs for tamper-proof evidence | Logs inmutables (WORM) | Legal evidence and compliance | WORM storage for audit trails | Immutable logs | Compliance |
| SSO | Single sign-on for centralized authentication | Inicio de sesión único | Simplify corporate access | Login via Okta | Federated auth | Enterprise |
| SAML / OIDC | Identity federation protocols for SSO | Protocolos de identidad (SAML / OIDC) | SSO integrations | Okta SAML, Azure OIDC | Identity protocol | Security |
| KMS | Key Management System for encryption keys | Sistema de gestión de claves | Customer-managed encryption | Customer KMS for S3 encryption | Key vault | Security |
| Encryption at Rest / in Transit | Protecting data stored and moving across networks | Cifrado en reposo / en tránsito | Secure PII and model artifacts | TLS for APIs, AES for storage | Data protection | Cloud |
| Multi-tenant | Single platform serving multiple customers with isolation | Multicliente | Scale SaaS with tenant isolation | Tenant quotas and admin | Shared platform | SaaS |
| Quota | Usage limit assigned per tenant or team | Cuota | Control usage and cost | GPU hours quota | Usage cap | Platform |
| Observability | Collection of metrics, logs, traces to understand systems | Observabilidad | Debugging and SRE workflows | Metrics, traces, logs | Monitoring | SRE |
| Prometheus | Metrics collection and time-series DB | Sistema de métricas (Prometheus) | Export performance and resource metrics | `model_inference_latency` metric | Metrics engine | Ops |
| Grafana | Dashboarding and visualization for metrics | Panel de métricas (Grafana) | Create dashboards and alerts | Drift dashboard | Dashboard tool | Ops |
| CI/CD | Continuous Integration / Continuous Deployment | Integración y despliegue continuo | Automate build, test, and deploy | CI pipeline to run tests | Automation | DevOps |
| SLA | Service Level Agreement: uptime and support commitments | Acuerdo de nivel de servicio | Contractual availability and remedies | 99.9% uptime SLA | Service guarantee | Business |
| Time-to-Value | Time until a customer gets measurable value | Tiempo hasta generar valor | Business metric for POC and onboarding | POC → working model | TTV | Product |
| ARR / MRR | Annual / Monthly Recurring Revenue — SaaS metrics | Ingreso recurrente anual/mensual | Track subscription revenue | $X M MRR | Recurring revenue | Finance |
| Chargeback | Internal allocation of cloud or platform costs to teams | Reparto de costos | Showback/chargeback by team | Cost per team report | Cost attribution | Enterprise |
