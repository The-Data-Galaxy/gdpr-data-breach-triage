# Manifest

Publication tree for v0.1.2. Exact file membership and SHA-256 values are in CHECKSUMS.txt, covering every other file in this tree, including the immutable approved ZIP and SHA256SUMS.txt. CHECKSUMS.txt excludes itself to avoid a circular hash. The ZIP preserves the accepted candidate snapshot; its hash is in SHA256SUMS.txt. PUBLICATION.md records the approval and the status-only documentation updates made for repository display.

Installable directory: gdpr-data-breach-triage/. Ten runtime files plus LICENSE and THIRD_PARTY_NOTICES.md. Runtime is copied from the final development candidate without transformations.

Public auxiliary files: README.md, INSTALL.md, LICENSE, THIRD_PARTY_NOTICES.md, RELEASE_NOTES.md, VALIDATION.md, MANIFEST.md, CHECKSUMS.txt, PUBLICATION.md, SHA256SUMS.txt, gdpr-data-breach-triage-v0.1.2.zip, examples/ransomware-intake.md.

Excluded: development governance, private feedback, internal work items, historical benchmark inputs/expected answers and scoring files, local install paths, caches, credentials and real incident materials. The included demonstration is synthetic. The official EDPB DOCX is the only bundled binary.

Standard repository gate: .github/scripts/open-source-gate.sh and .github/workflows/open-source-gate.yml are reused unchanged from the existing DPA Review repository. They validate public packaging on commits/PRs and do not change Skill behavior or the approved download ZIP.
