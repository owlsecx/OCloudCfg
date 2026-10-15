# 🦉 OCloudCfg

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OScan-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OCloudCfg** — Cloud IaC & Config Security Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Offline cloud IaC & config security auditor (Terraform / CloudFormation / Kubernetes)

---

## ✨ Features

- Tolerant HCL-subset parser for Terraform .tf files (blocks, labels, attributes, lists, objects, heredocs, function calls) + native .tf.json support
- Terraform auditor — AWS / GCP / Azure misconfigs: public buckets & ACLs, open security groups / NSGs / firewalls, unencrypted volumes, buckets & databases, public RDS / SQL, IAM wildcards, missing logging, plaintext secrets in variables, locals and providers
- Own YAML-subset parser (block + flow, multi-document, block scalars, CloudFormation short-form !Tags)
- CloudFormation auditor (YAML / JSON templates)
- Kubernetes manifest auditor — privileged pods, host namespaces, root users, capabilities, hostPath, token automount, limits, :latest images, RBAC
- Dockerfile quick check (pass-through, basic)
- IaC secrets scanner with masked evidence
- Policy engine — rule packs mapped to CIS benchmarks, ignore by rule id / resource / inline comment
- Weighted score + A+…F grade, remediation per finding
- Export TXT / MD / JSON / CSV / SARIF + clipboard
- Full CLI mode (--path, --tf, --k8s, --fail-on, ...)

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OCloudCfg
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
