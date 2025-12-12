# 🤖 Google Gemini CLI Container Image

## ✨ Intention and Overview

This repository provides a **ready-to-use Docker image** encapsulating the Google Gemini Command Line Interface (CLI). The primary intention is to establish a **consistent, isolated, and portable environment** for interacting with the Gemini API.

Using this container image allows you to:

- **Avoid Local Dependency Hassle:** Run the Gemini CLI without installing Python, the `google-genai` SDK, and all dependencies directly on your host machine.
- **Ensure Version Consistency:** Lock in a specific, tested version of the Gemini CLI, guaranteeing reproducible results across different projects and environments.
- **Simplify Setup:** Get up and running with a single `podman run` command, ideal for rapid prototyping, CI/CD pipelines, and project baselines.
- **Manage API Key Securely:** Easily pass your sensitive **GEMINI_API_KEY** to the container using standard Docker environment variables.

---

## 🚀 Quick Start

Follow these steps to quickly execute Gemini CLI commands using the Docker image.

### 1. Build the container image

You must have **Podman** installed on your system.

```bash
podman build -t [YOUR_CONTAINER_IMAGE_NAME]
```

### 2. Set Your API Key

The Gemini CLI requires your API key. For security, it's best practice to pass this as an environment variable (`-e` flag) during the Docker run.

> **Note:** Replace `YOUR_GEMINI_API_KEY` and `[YOUR_CONTAINER_IMAGE_NAME]` (or the custom tag you build) with the correct values.

### 3. Run the CLI Command

Use the following command structure to execute any Gemini CLI command inside the container.

```bash
 podman run \
  -e GEMINI_API_KEY="YOUR_GEMINI_API_KEY" \
  [YOUR_DOCKER_IMAGE_NAME] \
  -it /bin/bash
```
