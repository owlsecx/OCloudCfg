# 🦉 OCloudCfg

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OScan-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OCloudCfg** — Cloud IaC & Config Security Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OCloudCfg is an offline, static security auditor for cloud Infrastructure-as-Code and configuration, with no cloud API calls. It parses Terraform (HCL and .tf.json), CloudFormation, Kubernetes manifests and Dockerfiles using its own tolerant parsers, flagging public buckets, open security groups, unencrypted resources, IAM wildcards and plaintext secrets. A policy engine maps rules to CIS benchmarks with a weighted score, A+…F grade and per-finding remediation.

---

## ✨ Features

- Tolerant HCL-subset Terraform parser plus native .tf.json support
- Terraform AWS/GCP/Azure checks: public buckets, open SGs/NSGs, IAM wildcards, secrets
- CloudFormation (YAML/JSON) and Kubernetes manifest auditing
- Dockerfile quick check and masked IaC secrets scanning
- Policy engine with CIS-mapped rule packs and inline/id/resource ignores
- Weighted score, A+…F grade and export TXT/MD/JSON/CSV/SARIF

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OCloudCfg ./infra/
./OCloudCfg --path main.tf --tf --format sarif -o report.sarif --fail-on high
./OCloudCfg --path ./k8s/ --k8s --secrets
./OCloudCfg --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, bundled CPython version, and every bundled library with its exact
  version and license. Feed it to Grype, Trivy or Dependency-Track to audit
  our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

**No telemetry, no analytics, no licence check-in.** This tool does not phone
home. Verify that claim yourself:

```bash
sudo strace -f -e trace=network ./OCloudCfg --help   # watch every network call
firejail --net=none ./OCloudCfg --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
