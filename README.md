


###  fastener-catalog-pipeline/README.md

```markdown
# Fastener Catalog PDF → Excel ETL Pipeline

A complete end-to-end solution to extract product data from a Fastener Catalogue PDF, clean and normalise the data, flag duplicates, and save the result to Excel. Includes optional image-renaming logic.

## 📁 Project Structure
fastener-catalog-pipeline/
├── sources/
│ └── fastener_catalog.pdf
├── Output/
│ └── fastener_data_cleaned.xlsx
├── extract_and_clean_fasteners.ipynb
└── README.md


## 🛠️ Requirements

- Python 3.7+  
- pandas  
- pdfplumber  
- openpyxl  

Install dependencies:

pip install pandas pdfplumber openpyxl

🚀 Usage

1. Prepare

   - Place fastener_catalog.pdf in sources/

2. Run the Pipeline

   - python extract_and_clean_fasteners.ipynb

    This will:

     - Extract the table from page 1 of the PDF

     - Clean text (remove non-ASCII, collapse whitespace)

     - Forward-fill merged cells

      - Flag duplicate Item#

     - Save to Output/fastener_data_cleaned.xlsx

3.  Inspect
     - Open fastener_data_cleaned.xlsx for the final, cleaned dataset.

🔧 Customization

To extract from additional pages, adjust pdf.pages[<index>] or loop over pdf.pages.

Modify the cleanup function in the script to handle other edge cases.

📄 License
MIT © Oluwaleke










