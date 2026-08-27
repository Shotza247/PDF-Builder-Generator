# PDF Builder Generator

This project is a small PDF generator template. It creates a formatted PDF guide about self-hosted S3-compatible storage, MinIO, Parquet, and Delta Lake.

## Requirements

- Python 3.8 or newer
- `fpdf2`

## Setup

Create and activate a virtual environment, then install the project dependency:

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

If PowerShell blocks activation, run the script with the virtual environment's Python directly:

```powershell
.venv\Scripts\python.exe -m pip install -r requirements.txt
```

## Generate the PDF

Run:

```powershell
python generate_pdf.py
```

The script writes `self_hosted_s3_guide.pdf` to the project directory and replaces the previous file when run again.

## Customize the template

Edit `generate_pdf.py` to change:

- The document title in `header()`
- The footer and page numbering in `footer()`
- The guide content in `guide_text`
- The output filename in `pdf_output_file`

The examples inside the generated guide mention optional tools such as pandas, s3fs, pyarrow, and deltalake. They are reference content only and are not required to run this PDF generator.