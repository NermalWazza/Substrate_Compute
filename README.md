# Substrate_Compute
Baseline Azure VM substrate defined in Bicep, with immutable OS, persistent data disk, and clear separation between infrastructure and applications. Designed as a governed foundation for future workloads (e.g. OpenClaw).

# Governed_Substrate_VM

Baseline Azure VM defined via Bicep, treated as a **governed substrate node**:

- OS disk: reproducible, disposable (defined entirely in IaC)
- Data disk: persistent, attached to the VM for long-lived state
- Network: minimal VNet + NSG suitable for SSH from a controlled IP

This repo is **Good Enough / MVP** to:

- Demonstrate IaC skills (Bicep, Azure VM + networking)
- Show separation of concerns (infra vs. application)
- Provide a future host for applications (e.g. OpenClaw) while keeping infra clean

> **Note:** The VM currently deploys Ubuntu 22.04 LTS.  
> Xubuntu/desktop packages should be added via cloud-init or post-provisioning steps, not baked into this template.

