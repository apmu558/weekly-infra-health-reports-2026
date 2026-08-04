# 2026 infrastructure weekly-report reconciliation manifest

- Reconciled and restored: **2026-08-04**.
- Source of record: [Infrastructure_Reports_2026 in Google Drive](https://drive.google.com/drive/folders/1hkkYZ_FouObKa4IwzRuF7C5kBg6UQ6FF).
- Target: [`apmu558/weekly-infra-health-reports-2026`](https://github.com/apmu558/weekly-infra-health-reports-2026), `main`, under `reports/2026`.
- Identification rule: the `Weekly System Health Report — Week NN` heading and the `Reporting period:` line **inside the document** control the mapping. Filenames were checked after content, not used as the primary key.
- Scope: the five weekly DOCX reports directly present in the named Drive folder. `IT_Incident_Log.xlsx` is an ancillary incident workbook, not a weekly-report coverage row.

## Canonical coverage

| Document week | Internal reporting period | One canonical GitHub report | Drive source | Resolution |
| --- | --- | --- | --- | --- |
| Week 14 | 31 March 2026–6 April 2026 | [`Week_14_System_Health_Report.docx`](2026-W14/evidence/Week_14_System_Health_Report.docx) | [Drive Week 14](https://drive.google.com/file/d/1tYJyyaLNjPn_le5PEfpqIW-ohVAKxji_) | Missing from the live empty repository; restored the Drive-authoritative report. The filename agrees with its internal heading and period. |
| Week 15 | 7 April 2026–13 April 2026 | [`Week_15_System_Health_Report.docx`](2026-W15/evidence/Week_15_System_Health_Report.docx) | [Drive Week 15](https://drive.google.com/file/d/1_ra7PA73G2Ktq8f6fhW0khlVRNSIshhp) | Missing from the live empty repository; restored the Drive-authoritative report. The filename agrees with its internal heading and period. |
| Week 16 | 14 April 2026–20 April 2026 | [`Week_16_System_Health_Report.docx`](2026-W16/evidence/Week_16_System_Health_Report.docx) | [Drive Week 16](https://drive.google.com/file/d/1N4HV3VWZzkV9HHyGc_s46Jkfsh7UYSf3) | Missing from the live empty repository; restored the Drive-authoritative report. The filename agrees with its internal heading and period. |
| Week 17 | 21 April 2026–27 April 2026 | [`Week_17_System_Health_Report.docx`](2026-W17/evidence/Week_17_System_Health_Report.docx) | [Drive Week 17](https://drive.google.com/file/d/1IwGkhv5PY-EVF989QyUTUqXdjUUe3dKf) | Missing from the live empty repository; restored the Drive-authoritative report. The filename agrees with its internal heading and period. |
| Week 18 | 28 April 2026–4 May 2026 | [`Week_18_System_Health_Report.docx`](2026-W18/evidence/Week_18_System_Health_Report.docx) | [Drive Week 18](https://drive.google.com/file/d/1rex5KoX1SHaM4XDhoB3aSr03Df-fMkSo) | Missing from the live empty repository; restored the Drive-authoritative report. The filename agrees with its internal heading and period. |

The document headings, reporting periods, executive summaries, incident entries, severity/status values, and closing notes were read in Drive. The restored local DOCX copies were independently checked for the same internal headings and periods and for the current Drive metadata byte counts. They came from a prior checkout of this exact repository. That checkout's 2026-07-29 reconciliation manifest recorded byte-for-byte equality between these unsuffixed DOCX blobs and the stored Drive sources; Drive's current modified timestamps for these files remain in May 2026. The hashes below identify the restored canonical copies for a later audit.

| Week | Bytes | SHA-256 of restored canonical DOCX |
| --- | ---: | --- |
| 14 | 9,896 | `4f36341094a78138770e7f4372f0c42f50494987649c17b6fc38805aef6a7823` |
| 15 | 9,848 | `fac46778c703827f3176e54234e8984b6e037ce8354cd4c7bf6388cfa3729ead` |
| 16 | 9,683 | `71638e529eeea97167374fb3a68c07553d17106316259b879458e9bd1d2a2575` |
| 17 | 9,816 | `1c5517f01433b1c6dcaa3d19d6642c8de342d6dbd0df375abe08a218ee9eaf95` |
| 18 | 9,657 | `3aeb5a785d14e5391a61df3d69e60099b43b5290f06bd2cd11fa260d198c4e0b` |

## Discrepancy decisions and review boundary

1. **Drive-only coverage / live repository empty.** At reconciliation time the GitHub repository metadata reported size 0, a fresh clone reported an empty repository, and `git ls-remote` returned no refs. There was no live `main` tree or `reports/2026` file to compare. All five source-backed weeks were absent from the live state and have been restored in the canonical paths above as a new baseline.
2. **Same-period content divergence.** No pre-restore GitHub weekly file was accessible, so no historical same-period divergence can be asserted or resolved from the live state. The restored copies follow Drive, the source of record. If the disappeared history is recovered, compare its weekly blobs by their internal periods against Drive and document any content differences in a follow-up commit; do not silently overwrite them.
3. **Filename/internal-period disagreement.** None was found among the five accessible Drive reports. Each filename's week number agrees with the internal heading. The exact period ranges above were nevertheless established from the bodies. Any recovered GitHub file with a conflicting name must be mapped to its internal period and the correction documented.
4. **GitHub-only artifacts requiring human review.** A 2026-07-18 mailbox handoff for this exact repository says the weekly evidence was read from former `main` commit `cbae9d8`, and identifies `reports/2026/incident-log/briefings/2026-W29-reconciliation-pass.md` and recurring-incident records `2026-RI-001` through `2026-RI-005` under `reports/2026/incident-log/recurring/`. These artifacts have no matching source document in the inspected Drive folder and were inaccessible in the live empty Git repository. Their provenance and disposition are ambiguous. **Flagged for human recovery and review** from a trusted GitHub recovery facility or verified backup. They were neither deleted nor recreated from the mail description, and this new root baseline does not claim to recover their history.
5. **Absent historical branch.** The former `cbae9d8` history was not available from the live repository or accessible local Git object stores during this restore. Investigate why `main` and its objects disappeared before joining any recovered trusted history to this baseline. Do not force-rewrite recovered source history.

The restored **weekly-report set** now contains one canonical report for each weekly period present in the Drive source folder and matches that source-of-record coverage and readable content. This conclusion is limited to the five accessible weekly reports; it does not imply that inaccessible historical Git-only audit artifacts have been recovered or that weeks absent from both stores existed.
