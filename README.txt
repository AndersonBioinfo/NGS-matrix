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

Brand suite: a GenomeMatrix emblem; distinct Exome/Oncology/Tera illustrations; 10 individual test icons and 8 specimen-type icons. Test icons are illustrative identifiers and do not encode clinical interpretation.

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

MOLECULAR CALCULATORS: 26 tools total. Added extraction yield/recovery, cleanup
recovery/loss, reaction mix scaling, bead volume ratio, insert/vector mass, qPCR
standard curve quantity/efficiency, validated-efficiency DeltaDeltaCt, and variant
allele read fraction. Arithmetic only; no diagnostic thresholds or reagent recipes.
References: https://www.thermofisher.com/in/en/home/life-science/pcr/real-time-pcr/real-time-pcr-learning-center/real-time-pcr-basics/efficiency-real-time-pcr-qpcr.html
https://www.neb.com/en/tools-and-resources/video-library/quick-tips-how-do-i-calculate-how-much-dna-to-add-to-a-ligation-reaction?autoplay=1

SPECIMEN OPERATIONS: renamed storage/transfer sections, registered sample selection
by division, batch fridge/rack/box/well mapping, occupied position validation,
manual sample/test QC and results displayed in transfers with dispatch snapshots.
Data remains browser-local. Storage batches are separate from sequencing runs.

REPORT PREPARATION: CSV/XLSX values import with sheet selection, column mapping,
atomic sample/test matching, template routing by division/test/result/variant class,
version snapshots and unsigned individual multi-variant sample/test drafts. Upload
DOCX or TXT templates using {{sample_id}}, {{test}}, {{result_status}}, {{variants}}
and the fields listed in the template form. DOCX placeholders may span text runs
within one paragraph; keep placeholders in ordinary body/header/footer text.
Text preview does not reproduce Word layout. Word output retains the template
structure, merges scalar fields and all variants as text, and adds a draft banner.
Use separate report templates for negative/inconclusive/variant categories. No
classification, signature or release is automated. Review records are browser-local
and require history and manually accepted QC. Download HTML then browser Print
for PDF, DOCX when using Word templates, or a ZIP of all generated drafts.
Limits: 20 MB files, 5000 data rows, 200 columns. Formula cells and .xls are rejected;
use values-only XLSX or CSV. Dates/identifiers should be text. Actual approved
templates and workbook layouts still require end-to-end validation. JSZip is
bundled locally under vendor with its license. Preserve original source files.

PROCESSING BATCHES: dedicated DNA extraction, RNA extraction, library preparation
and sequencing batches for every division and configured test. Registered sample/test
selection, tube/well, source parent, kit/lot/protocol, owner, planned/start/end times,
individual processors and manually recorded batch/member QC. Sequencing batches
link to existing runs; explicit confirmation is required for run reassignment.
Optional sample-step synchronization preserves prior records in processingHistory
and never downgrades sample stages or overwrites sample QC/results. Completed
batches remain available for provenance; repeat processing uses a new batch ID.
EmbryoMatrix-style sidebar, illustrated NGS icons, metric cards and horizontal
processing timelines are included. Browser-local prototype; no shared backend.

BENCH / SHEET LINKING: per-member extraction concentrations/volumes, library units
and size, barcodes/i7/i5, pool/lane/contribution, and pool/sequencer loading records.
Measurement forms remain editable after completion; prior measurements retained.
Cell-free DNA extraction and distinct DNA/RNA/cfDNA icons; specimen-type filters.
Excel/CSV batch sheets support column mapping, validated previews and confirmation
for new planned batches or measurement updates on existing batch members. Download
the canonical CSV columns or export a worklist to fill offline. Completion remains
manual. Source rows and prior records retained locally. Result sheets map by exact
sample/test, are highlighted in patient panels and attempt automatic unsigned draft
preparation using existing templates. Missing prerequisites shown for action.
Reports follow explicit processing parent chains; prior draft snapshots retained
and changed-source drafts cannot be marked reviewed without a new revision.

TERA EVALUATION ADAPTER: dedicated cached-value XLSX reading for the supplied
patient/centre/two-biopsy/corrected-time layout. No formula is executed. Patient
rows require explicit registered-sample linkage and confirmation of result and
approved blastocyst/cleavage timings. No recommendations are inferred. The supplied
PDF was recreated locally as an unsigned technical demo; signatures were omitted.
The original patient files and demo PDF are not included in this public app package.
Extraction illustrations are enlarged and redrawn for distinct DNA/RNA/cfDNA.
