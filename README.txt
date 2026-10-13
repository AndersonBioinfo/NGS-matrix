NGS Matrix — local workspace update

Open index.html. Keep all JS, CSS and icons beside it.
Home: summary cards, run workflow columns, division shortcuts and all-run summary.
Run reports & QC: run summary filters and CSV export; detailed QC remains available.
Image vault & TRFs: multiple files/folders, sample-test or run linking, categories,
month, recorder, notes, downloads, image thumbnails and reversible archive/restore.
Categories include results, TRF, clinical history, QC and supporting images.
Uploaded Excel/CSV files are retained as attachments; their data is not automatically
parsed or matched. Sample-register CSV import remains in Import & setup.
Activity log: successful sample/QC/history/storage/transfer/result/staff edits,
uploads and CSV register imports, with manually selected staff identity and IST time.
User management: add/edit staff, intended role/division, active/inactive status.
Tera: receptivity result summary, large circular icons, individual results and CSV.

Records use existing browser localStorage. Files use IndexedDB, max 100 MB per file.
Do not clear browser data. Keep original document files; register backups and CSV
exports do not contain attachment binaries. Folder selection is available in Chromium.
These are prototype user-management and activity-history screens. No authentication,
role enforcement, shared storage, tamper-proof audit, or clinical approval is implemented.
A file upload never changes clinical history status or releases a report.
The application is not published. IT must add server storage and real staff login.

Verification: syntax; 15 page renders; filter and total logic; file validation;
sample-test/run attachment isolation; save/archive/restore; staff validation;
successful-change logging. Browser preview timed out; visual browser QA unavailable.

NGS CALCULATORS — user-supplied methods implemented
Open NGS Calculators in the navigation. Fourteen tools cover DNA mass/input volume,
dsDNA mass-molarity conversion, mass-to-pmol, nM/pM/total pmol, final-volume and
fixed-stock dilution, molecular pooling, reads/pairs vs Gb, usable run capacity,
coverage/raw bases, loading output/PF estimates, candidate loading concentration,
PF clusters/read output and cluster-density × imaged-area arithmetic.
Inputs begin blank. Load illustrative example is optional; replace example values
with actual measured data. The loading examples still require explicit confirmation
of comparable run conditions and a validated local range before calculation.
Patterned-flow-cell density estimators are disabled. No instrument loading limit,
denaturation protocol, QC cutoff, clinical target depth or empirical PF is assumed.
Save calculations by name with an optional run link. Saved inputs/results are copied,
time-stamped with staff identity, visible in Saved calculation history and exported
as CSV with formulas and assumptions. These records stay in localStorage and the
activity log; no result metrics are automatically overwritten by calculator outputs.
Exact counts are calculated without rounding until display (up to 6 decimal places).
Coverage is average. Pool distribution and loading output are estimates, not guarantees.
Validation checks included all user-note worked examples, unit directions, nonpositive
denominators, percentages, impossible dilutions, read/pair semantics, molecular pooling,
patterned-cell exclusions, saved-record history and CSV. Browser visual QA unavailable.

COMMON CALCULATIONS — FASTASeq S guide review
Eighteen tools are now available. Added percentage dilution (same percentage basis),
concentration after adding diluent, combined dsDNA library normalization, and mL/uL
conversion. Reviewed FASTASeq S quick-start guide pages 2–3. Existing molarity and
final-volume dilution tools already cover the general library arithmetic.
Instrument-specific reagent steps, wash volumes, loading ranges and timings are not
universal defaults. Percentage mixing uses nominal volumes; prepare the specified
final volume according to your laboratory SOP where volume additivity does not apply.
PATIENT PANEL: Sample registry Open now displays a patient/case panel grouped by
case ID and referring centre, with independent test timelines, QC, report summaries,
kit/lot/protocol, result files, storage and transfers. Click a stage to record staff
and timestamps. Refresh panel reads current browser records; shared real-time
tracking still requires the LAN backend. No completion dates are inferred.
