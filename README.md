# GovSec V2 — LOGOS Governance Systems

Governed AI infrastructure across build-time trust, runtime monitoring, and deployment authorization.

## Current Status

**Production-grade AI governance infrastructure** built over 12 months by U.S. Army combat-disabled veteran. Core components implemented, internally tested, and achieving **94.4% defense rate** against adversarial taxonomy. Full proofs and artifacts in this repo. Seeking seed funding to advance from internally validated MVP to first governed agent pilots.

## Three-Layer Architecture

| Module | Moment | Function |
|--------|--------|----------|
| **DEP.KEYSTONE** | Before execution | Supply-chain trust, CycloneDX SBOM verification, 31 internal passing tests |
| **Sentinel OverWatch v3.6** | During execution | Runtime boundary enforcement, BD1A v4.1 taxonomy, **94.4% block rate** (34/36 vectors blocked) - see `proofs/sentinel-v3.6-summary.md` |
| **GovMem V2** | Multi-turn detection | RL-enhanced session memory with 12-department tracking, semantic drift detection - see `proofs/govmem-v2-architecture.md` |
| **HAAP v2.0** | After execution + gates | Human-Agency Assurance Protocol with cryptographic intent tokens, immutable causal logging (provisional patent US 63/953,447) - see `proofs/haap-governance-summary.md` |

## Recent Milestones

**April 2026 Sprint:**
- ✅ Sentinel v3.6 hardening: **94.4% defense rate** (up from 72.2%)
- ✅ 63 SENT-* detection rules with unicode normalization
- ✅ GovMem V2 infrastructure: Multi-turn drift detection framework
- ✅ 12-department governance integration (EXE/ENG/PRD/SEC/LGL/FIN/OPS/REV/MKT/HR/DAT/GRC)

## How to Verify
```bash
git clone --recurse-submodules https://github.com/LogosGSInc/GovSec-V2.git
cd GovSec-V2

# Initialize submodule if needed
git submodule update --init --recursive

# Review DEP.KEYSTONE artifacts (submodule)
cd keystone
ls artifacts/ tests/ || echo "Inspect submodule contents for SBOM and test logs"

# Return to root and review proofs
cd ..
cat proofs/sentinel-redteam-summary.md
cat proofs/haap-governance-summary.md
Limitations & Roadmap

All testing internal/solo at this stage.
Gaps are documented transparently in the proofs/ folder.
Next (post-seed): external red-team, production hardening, first enterprise pilots.

Reviewer Path
See PROOF_INDEX.md for the full no-NDA diligence map.
Standards referenced: NTIA SBOM | EO 14028 | NIST AI RMF GOVERN 1.1 | SLSA Level 1
Proprietary — Copyright 2026 LOGOS Governance Systems Inc.
