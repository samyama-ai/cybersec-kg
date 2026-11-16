# Data Provenance & License Clearance (`cybersec-kg`)

Every source entering `cybersec-kg` is cleared for public redistribution prior to ingestion (`redistributable` verdict required on export). Pipeline execution separates `fetch` (recording raw upstream SHA-256 digests and retrieval timestamps) from `etl` and `.sgsnap` export.

## Source Registry

| Source ID | Dataset | Canonical URI | License / Terms | Verdict | Required Attribution |
|---|---|---|---|---|---|
| `osv` | Open Source Vulnerabilities (OSV.dev) | `https://osv-vulnerabilities.storage.googleapis.com/` | `CC-BY-4.0` | `redistributable` | OSV.dev / Google Open Source Security Team (`CC-BY-4.0`) |
| `nvd` | NIST National Vulnerability Database (JSON 2.0) | `https://nvd.nist.gov/vuln/data-feeds` | US Public Domain (`17 U.S.C. § 105`) | `redistributable` | Data provided by NIST NVD (not endorsed by NIST) |
| `cisa-kev` | CISA Known Exploited Vulnerabilities Catalog | `https://www.cisa.gov/sites/default/files/feeds/known_exploited_vulnerabilities.json` | US Public Domain / `CC0-1.0` | `redistributable` | Cybersecurity and Infrastructure Security Agency (CISA) |
| `first-epss` | FIRST Exploit Prediction Scoring System | `https://epss.cyentia.com/` | Open Data (FIRST.org attribution) | `redistributable` | FIRST.org, Inc. EPSS (`https://www.first.org/epss`) |
| `mitre-cwe` | MITRE Common Weakness Enumeration | `https://cwe.mitre.org/data/downloads.html` | MITRE Royalty-Free License | `redistributable` | "© The MITRE Corporation. Reproduced and distributed with permission." |
| `mitre-capec` | MITRE Common Attack Pattern Enumeration and Classification | `https://capec.mitre.org/data/downloads.html` | MITRE Royalty-Free License | `redistributable` | "© The MITRE Corporation. Reproduced and distributed with permission." |
| `mitre-attack` | MITRE ATT&CK STIX 2.1 (`mitre/cti` / `attack-stix-data`) | `https://github.com/mitre-attack/attack-stix-data` | MITRE Royalty-Free License | `redistributable` | "© The MITRE Corporation. This work is reproduced and distributed with the permission of The MITRE Corporation." |
| `mitre-d3fend` | MITRE D3FEND Ontology & Mappings | `https://d3fend.mitre.org/ontologies/` | MITRE Royalty-Free License / `CC-BY-4.0` | `redistributable` | MITRE D3FEND™ (`https://d3fend.mitre.org`) |
| `sigmahq` | SigmaHQ Open Detection Rules (core rules) | `https://github.com/SigmaHQ/sigma` | Detection Rule License (DRL 1.1) / `Apache-2.0` | `redistributable` | SigmaHQ Contributors (preserve rule `author` & `license` fields) |
| `nist-oscal` | NIST SP 800-53 Rev 5 & NIST CSF 2.0 (OSCAL JSON) | `https://github.com/usnistgov/oscal-content` | US Public Domain (`CC0-1.0`) | `redistributable` | National Institute of Standards and Technology (NIST) |
| `opensecops-twin` | Synthetic Enterprise Cloud/K8s/OT Topology | Generated deterministically in `etl/twin.py` | `Apache-2.0` | `redistributable` | Samyama AI |

## Explicitly Excluded Sources (`local-only` / Non-Redistributable)

- **ISO/IEC 27001 / 27002 control text:** Copyrighted by ISO; never ingested.
- **CIS Benchmarks prose/PDFs:** Proprietary CIS terms; never ingested.
- **Commercial threat-intelligence feeds & customer telemetry:** Strictly prohibited in this repository.
