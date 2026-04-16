# GovSec V2 — LOGOS Governance Systems

Governed AI infrastructure across build-time trust, runtime monitoring, and deployment authorization.

## Current Status
MVP built solo over 12 months by a U.S. Army combat-disabled veteran.  
Core components implemented and internally tested.  
Full proofs and artifacts are in this repo.  
**Not yet production-deployed with external customers.** Seeking seed funding to advance from internally validated MVP to first governed agent pilots.

## Three-Layer Architecture

| Module                  | Moment              | Function |
|-------------------------|---------------------|----------|
| DEP.KEYSTONE            | Before execution    | Supply-chain trust, CycloneDX SBOM verification, 31 internal passing tests |
| Sentinel OverWatch v3.5 | During execution    | Runtime boundary enforcement, BD1A taxonomy, documented 72.2% internal block rate across 36 vectors (see proofs/sentinel-redteam-summary.md) |
| HAAP v2.0               | After execution + gates | Human-Agency Assurance Protocol with cryptographic intent tokens, immutable causal logging, revocation (provisional patent US 63/953,447; see proofs/haap-governance-summary.md) |

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
