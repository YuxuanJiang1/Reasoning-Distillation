# DRP · What to teach

**Distilled Reasoning Pruning with Mathematical Skill-aware Step Decomposition for Efficient Large Reasoning Models**
Yuxuan Jiang, Dawei Li, Francis Ferraro · **ACL 2026 Findings**

[Published paper](https://aclanthology.org/2026.findings-acl.196/) · [Implementation](https://github.com/YuxuanJiang1/DRP) · [Series overview](../README.md)

DRP refines reasoning traces through skill-aware decomposition and pruning, then distills the resulting paths into a student. Its place in this series is the **content and structure of supervision**.

## Workflow

```text
Reasoning trace → Skill-aware decomposition → Content pruning → Student distillation
```

On GSM8K, the published paper reports a reduction from 917 to 328 average tokens while accuracy rises from 91.7% to 94.1%. These numbers belong to the paper's specific experiment.

## Use the implementation

```bash
git clone https://github.com/YuxuanJiang1/DRP.git
cd DRP
```

Use the upstream README for dependencies and configuration. Entry points include `split_verify.py` for decomposition/pruning, `requirements/` for environment setup, and `eval/` for evaluation. Data release status is maintained in that repository.

DRP is presented here as a reasoning-distillation method; inclusion in the series does not imply that it uses the same on-policy training protocol as TOPD.
