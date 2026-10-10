NGS Matrix — workflow format v3

Extract the complete ZIP and open index.html in a modern browser.
Keep enhancements.js, enhancements.css, icons.js and the icons folder beside index.html.
For LAN preview, IT can serve this folder with a static web server.

New workflow features
- Clinical history is shared across all tests of a sample.
- Missing history opens an Overview alert and appears in a counselor queue.
- Download pending-history CSV with receiving date, sample/case ID, tests,
  division, sample type, client, physician, client contact, missing information,
  counselor, follow-up status, last/next follow-up and notes.
- Download is manual; this software does not contact clients or counselors.
- Record original-specimen, DNA/RNA/plasma/cfDNA/library storage and aliquots.
- Track dispatch and receipt; acknowledgment updates the container location.
- Run reports show sequencer, division, run date, QC, reads/read pairs,
  read configuration, yield in Gb, data size in GB, Q30 and pass-filter percent.
- Record sample-test QC, DNA/library concentration, reads, coverage and size.
- Run-report filters, CSV export and Print are available.
- Missing clinical history or failed sample QC blocks the demo report-release
  stage update. This is not a production approval system.
- v2 import template adds sample-level clinical/receiving/client fields.
  The original 8-column template is still accepted.

All example data is fictional. QC outcomes are entered manually; no laboratory
acceptance criteria are assumed. Temperature values are examples, not protocols.
Blank metrics mean not recorded, not zero. Reads and read pairs are separate;
Gb means gigabases and GB means decimal gigabytes of data files.

Data remains in this browser's local storage only, under the original demo key.
Existing demo records are migrated without deleting them. Reset restores examples.
Do not enter patient information. This prototype has no production login, shared
database, access controls, report approval or audit logging. Your IT team must add
these before production use. No changes were made to EmbryoMatrix on your LAN.

Version 3 adds 20 illustrated icons matching the EmbryoMatrix reference style, integrated into navigation, sample stages, run cards and dashboard metrics.

Additional personnel tracking: received-by name, individual processor, IST start/completion time, verifier and notes per sample-test step; downloadable processing logs. Names are manual prototype entries. Publication did not complete because terminal workflow input was rejected by automatic approval policy.
