# Qualitative Breach-Risk Factors

Use these factors to explain severity and likelihood. Do not convert them into a fixed numerical threshold.

## Core questions

1. What was affected: confidentiality, integrity, availability, or more than one?
2. What data was involved, and how sensitive is it alone or in combination?
3. How many people and records were affected, using estimates when clearly labelled?
4. How easily can the people be identified or linked to other information?
5. Who received, accessed, copied, exfiltrated, or may still possess the data?
6. What concrete consequences could occur: identity misuse, fraud, discrimination, reputational harm, physical or psychological harm, loss of access, or other material impact?
7. What is the likelihood of those consequences, given evidence of access, intent, propagation, public exposure, or continued attack?
8. Are children, patients, employees, or other vulnerable people involved?
9. Do the claimed mitigations actually work for this incident?

## Evidence discipline

For each risk-increasing or risk-reducing factor, record the evidence status:

- confirmed by a log, document, or reliable statement;
- estimated with a stated basis;
- disputed or incomplete;
- merely assumed.

Examples of mitigation that require verification include encryption with protected keys, pseudonymisation that prevents practical identification, a trustworthy recipient's prompt deletion with confirmation, reliable backups, rapid credential reset, and evidence that data was not accessed or propagated. A mitigation is not effective merely because someone asserts it.

## Decision language

Use calibrated conclusions:

- unlikely to result in risk;
- risk cannot currently be excluded;
- likely to result in risk;
- likely to result in high risk;
- insufficient facts, with a specified next review point.

Always explain what could change the conclusion.
