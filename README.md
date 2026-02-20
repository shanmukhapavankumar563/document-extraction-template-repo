# Document Extraction Service (Local-First)

This repository includes a completed local-first pipeline that:
1. Classifies each document as `invoice` or `packing_list`.
2. Extracts required fields from each document type.
3. Extracts line-item rows using OCR/text heuristics.
4. Writes outputs in `output/` as JSON and Excel (`.xlsx`, optional dependency).

Implementation is in `app/.donotdelete` (single-file script to satisfy your "no new files" request).

## Run
From repository root:

```powershell
python app/.donotdelete --input samples --output output --format both
```

Single-file run:

```powershell
python app/.donotdelete --input samples/invoices/invoice_1.pdf --output output --format json
```

## Dependencies
Install local libraries:

```powershell
pip install pdfplumber pytesseract pillow pdf2image openpyxl
```

System tools:
1. Install Tesseract OCR locally and add it to PATH.
2. Optional: install Poppler for PDF OCR fallback (`pdf2image`).

## Output
The script writes timestamped files to `output/`:
1. `extraction_YYYYMMDD_HHMMSS.json`
2. `extraction_YYYYMMDD_HHMMSS.xlsx` (if `openpyxl` is installed)

Each JSON document record contains:
1. `source_file`
2. `document_type`
3. `confidence`
4. `fields`
5. `line_items`
6. `notes`

## Required Extraction
Invoice:
1. Vendor Name
2. Invoice Number
3. Invoice Date
4. Table of Contents / Line Items

Packing List:
1. Order Number / PO Number
2. Ship-to Address
3. Table of Contents / Line Items

## Notes
1. If direct PDF parsing fails, OCR fallback is attempted.
2. If OCR dependencies are missing, the script records that in `notes`.
3. JSON output still works even if `.xlsx` dependency is unavailable.
