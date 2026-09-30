# Awesome-Distributed-Training-Platform

## Top Distributed Training Platform Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Multi-GPU Orchestration, Cluster Scheduling & Fault-Tolerant Training*  

**Last updated: September 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Distributed Training**. These tools orchestrate multi-GPU and multi-node training jobs, manage cluster resources, handle fault tolerance and checkpointing, and optimize hyperparameter search across large-scale deep learning workloads.



**Examples** include Anyscale, Determined AI, Lightning AI, Run:AI, SageMaker Training, Vertex AI Training, Azure ML Compute, Kubeflow, ClearML, Valohai, MosaicML, Weights & Biases, Modal, Paperspace Gradient, Saturn Cloud, Domino Data Lab, Lambda Stack, Databricks Mosaic AI, and Azure ML (the category leaders).



**Open-source emphasis**: This section is expanded with active projects for self-hosting, custom schedulers, and transparent cluster management — ideal for ML engineers, platform teams, and researchers building vendor-independent training infrastructure. The open-source ecosystem is anchored by **Determined AI** (full training platform), **Kubeflow** (Kubernetes-native ML), and **Ray/KubeRay** (distributed compute), with strong coverage in experiment tracking and hyperparameter optimization.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Anyscale](https://www.anyscale.com/)**  

  Enterprise platform for running Ray at scale. Provides managed infrastructure for ML training, serving, and data processing workloads with BYOC deployment, auto-scaling, and Kubernetes support (EKS, AKS, GKE, CoreWeave, Nebius). Features Anyscale Runtime (formerly RayTurbo) with proprietary enhancements including mid-epoch resumption, elastic training, and job-level checkpointing that survives driver or cluster failure . Available in Hosted and Bring-Your-Own-Cloud models .



- **[Determined AI](https://determined.ai/)**  

  Open-source deep learning training platform (acquired by HPE in 2021, now HPE Machine Learning Development Environment). Handles GPU scheduling across heterogeneous clusters (NVIDIA H100, A100, V100, AMD MI300), elastic scaling, automatic checkpoint management with fault-tolerant resumption, and distributed hyperparameter search using ASHA and population-based training . Wraps PyTorch and TensorFlow training loops, transparently parallelizes across devices using DDP or Horovod, and provides WebUI and REST API for experiment tracking, metric visualization, and model artifact management . Licensed per-GPU for HPE enterprise deployments .



- **[Lightning AI](https://lightning.ai/)**  

  Cloud platform from the creators of PyTorch Lightning with free GPU hours (e.g., 80 hours), Studio features, and pay-as-you-go pricing. Pro and Teams tiers for professional developers, Enterprise tier offers BYOC and enhanced security .



- **[Run:AI](https://www.run.ai/)**  

  GPU orchestration and virtualization platform (now NVIDIA Run:ai) with GPU Fractions for sharing GPUs across workloads. Enables dynamic memory and compute allocation, reducing wait times and improving utilization. Works alongside other schedulers via reservation pods. Supports multi-GPU fractions for workloads requiring more than one device .



- **[SageMaker Training](https://aws.amazon.com/sagemaker/)**  

  AWS's fully managed ML platform with distributed training libraries (SMP), managed Spot training, built-in algorithms, and inference optimization (Neo). Deep integration with AWS ecosystem .



- **[Vertex AI Training](https://cloud.google.com/vertex-ai)**  

  Google Cloud's unified ML platform with TPU support, best TensorFlow integration, Vizier hyperparameter tuning, and custom containers. Strong AutoML capabilities and BigQuery ML integration .



- **[Azure ML Compute](https://azure.microsoft.com/en-us/products/machine-learning)**  

  Microsoft's managed ML platform with PyTorch distributed training support (MASTER_ADDR, MASTER_PORT, WORLD_SIZE, RANK environment variables), process_count_per_instance configuration, and integrated MLOps .



- **[Modal](https://modal.com/)**  

  Serverless cloud platform for GPU workloads with multi-node training clusters (beta) via @clustered decorator. Offers B200 ($6.25/hr) and H200 ($4.54/hr) GPUs with 3.2 Tbps Infiniband RDMA for linear scaling with node count . Sub-second cold starts via lazy-loaded, content-addressed images. Recycled compute on idle GPUs available for fault-tolerant background tasks .



- **[Weights & Biases](https://wandb.ai/)**  

  Experiment tracking and model management platform with integrations across training frameworks and platforms.



- **[Databricks Mosaic AI](https://www.databricks.com/)**  

  Unified data intelligence platform with Mosaic AI for training, fine-tuning, and serving foundation models.



- **[MosaicML](https://www.mosaicml.com/)**  

  Platform for training foundation models with optimized training stack (acquired by Databricks).



- **[Paperspace Gradient](https://www.paperspace.com/)**  

  Cloud platform for ML development with GPU-powered notebooks and training workflows.



- **[Saturn Cloud](https://saturncloud.io/)**  

  Cloud platform for data science and ML with Dask and GPU support.



- **[Domino Data Lab](https://www.dominodatalab.com/)**  

  Enterprise MLOps platform for model development, deployment, and governance.



- **[Lambda Stack](https://lambdalabs.com/)**  

  Pre-configured deep learning software stack for Lambda GPU workstations and cloud instances.



## Open-Source GitHub Projects



- **[Determined](https://github.com/determined-ai/determined)**  

  Open-source deep learning training platform with 3,240+ stars under Apache-2.0 . Provides distributed training for faster results, hyperparameter tuning for optimal models, resource management for cutting GPU costs, and experiment tracking for reproducibility . Centralized master + agent architecture with PostgreSQL metadata database . Supports PyTorch, TensorFlow, and Keras . **The de facto open-source alternative to vendor-specific stacks like NVIDIA Base Command Platform and AWS SageMaker** for operational orchestration of training compute . HPE acquired the company in 2021 and continues development as HPE Machine Learning Development Environment .



- **[Kubeflow](https://github.com/kubeflow)**  

  Kubernetes-native ML toolkit with 4.5/5 rating and 22+ reviews . Includes Kubeflow Pipelines for workflow orchestration, Katib for hyperparameter tuning, and Training Operator for distributed training jobs (PyTorch, TensorFlow, MPI, XGBoost). **Fully free and open-source** . Makes deployment of ML workflows on Kubernetes straightforward and automated .



- **[Ray](https://github.com/ray-project/ray)**  

  Open-source distributed computing framework with 4.7/5 rating and 391+ reviews . Provides Ray Train for distributed training, Ray Tune for hyperparameter search, Ray Data for data processing, and Ray Serve for model serving. Used by OpenAI for ChatGPT training, Cohere for TPU-based LLM training, and vLLM for multi-node inference . **Note**: Ray is a distributed compute framework, not a full training platform — it requires integration with KubeRay and workflow engines for production orchestration .



- **[KubeRay](https://github.com/ray-project/kuberay)**  

  Official Kubernetes operator for deploying and managing Ray clusters. Provides three CRDs: RayCluster (cluster lifecycle), RayJob (one-off jobs), and RayService (Ray Serve deployments). Supports heterogeneous compute nodes, autoscaling, and integration with queueing systems (Kueue, Volcano, YuniKorn) and observability tools (Prometheus, Grafana) . Managed support on Google Cloud (Ray on GKE) and Databricks .



- **[ClearML](https://github.com/allegroai/clearml)**  

  Open-source MLOps platform with experiment tracking, data management, pipeline orchestration, and GPU scheduling. Self-hosted or cloud deployment.



- **[Valohai](https://github.com/valohai)**  

  MLOps platform with pipeline orchestration and experiment tracking, emphasizing reproducibility.



- **[MLflow](https://github.com/mlflow)**  

  Open-source platform for the ML lifecycle including experiment tracking, model registry, and project packaging. Widely adopted standard for experiment metadata.



- **[Optuna](https://github.com/optuna/optuna)**  

  Hyperparameter optimization framework with pruning algorithms and distributed search support. Integrates with Determined and other training platforms for HPO.



### Additional Strong Open-Source Options



- **Determined Examples** — Example ML projects using the Determined library for reference .

- **devcluster** — Developer tool for running the Determined cluster locally .

- **HPE ML Dev Env** — Enterprise HPE distribution built on Determined with per-GPU licensing and managed deployment options .



**Frameworks for building custom distributed training solutions**: Combine **Determined** for a full-featured training platform with experiment tracking, HPO, and fault tolerance . Use **Kubeflow** for Kubernetes-native orchestration with Training Operator for distributed jobs . Deploy **Ray + KubeRay** for Python-native distributed compute with Ray Train and Ray Tune . Integrate **MLflow** or **ClearML** for experiment tracking, and **Optuna** for advanced hyperparameter search. For serverless multi-node training, **Modal** provides @clustered decorator with RDMA networking . Note that true enterprise distributed training platforms with managed infrastructure, enterprise SLAs, and compliance certifications (SOC 2, HIPAA) remain primarily commercial territory; open-source stacks provide strong scheduling, fault tolerance, and experiment tracking foundations that require integration for complete MLOps.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Distributed training tools must comply with data privacy regulations (GDPR, HIPAA), export controls for AI models, and applicable cloud security requirements.

- Self-hosted open-source solutions require proper infrastructure, GPU driver management, network configuration (RDMA/Infiniband), and ongoing maintenance. Checkpoint storage to durable object storage (S3, GCS, Azure Blob) is critical for fault tolerance . Ray's object store is in-memory and unencrypted by default — enable TLS for regulated data .

- The open-source ecosystem provides strong scheduling, fault tolerance, and experiment tracking foundations, but managed infrastructure, enterprise SLAs, and compliance certifications remain primarily commercial offerings.



---



**Made for ML engineers, platform teams, research scientists, and AI infrastructure architects.**  

Let's make distributed training more open, transparent, and efficient.
